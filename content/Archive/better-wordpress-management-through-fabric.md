---
title: "Better Wordpress Management through Fabric"
date: "2016-01-27"
updated: 2023-03-26
---

One of my goals in setting up a Wordpress site was to automate the deployment, configuration, and maintentance. More specifically, I wanted the following:

- Provider intependence. I should be albe to easily move my site to another hosting provider.
- Automanted restore. I couldn’t be in a posistion where restoring from backup meant manually tapping in SQL load statements.

There’s more I want to do long-term, but that’s the bare minimum. The easiest way I found was [Fabric](https://www.fabfile.org). Fabric has a low barrier to entry because it is straigtforwardly build on top of Python functions and the commands on the target machine.

If you need to run `apt-get -y install mysql-server` on the target host, the Fabric call for that is:

```python
run('apt-get -y install mysql-server')
```

To make the command available outside the script (e.g., from the command line), just add it in a function:

```python
def install_msql():
    run('apt-get -y install mysql-server')
```

Then from the shell you can run

```bash
$ fab install_mysql
```

and you computer will connect to the sever and run the `apt-get` call above.

There’s a little bit more to it in getting your hosts, user, and paswords or keys set up, but it’s all pretty straightforward. It works over SSH so there’s no agent to install on the server.

All your functions can be parameterized in pretty obvious ways. Your backup function might look like

```python
def backup(dbname, dbuser):
    run('mysqldump -u {0} {1} > $HOME/{1}.sql'.format(dbuser, dbname))
```

There are additional commands to upload and download files, to sync a directory, and other utilities.

There are drawbacks. One is that when I say “obvious,” I mean “obvious if you know Python.” It helps if you’re familiar with installing Python packages and some basic syntax.

Another drawback is the lack of [idempotence](https://lookup.computerlanguage.com/host_app/search?cid=C999999&term=idempotent). I can run `apt-get -y install mysql-server` multiple times without consequence. But if I run the Wordpress cli, `wp core install` installs wordpress the first time I call it. If I call it again (after the files are already there), it throws an error.

I can live with this for now. I really want the initial setup, which always starts with a clean slate. Extending it to modify an existing installation can wait for another day.
