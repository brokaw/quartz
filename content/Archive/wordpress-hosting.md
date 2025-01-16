---
title: "WordPress Hosting"
date: "2020-03-22"
updated: 2023-03-36
categories:
  - "words"
---

While I’m on the topic of WordPress, I found a new hosting provider. I run a small family site. Even though it’s small, it has a lot of specific needs:

- It’s very image-heavy, so it needs lots of storage space
- I need to send out email notifications at various events
- Users need to be able to post by sending email
- It needs to be robust and reliable, so I don’t spend a lot of time chasing down issues.

We’ve tried various hosted solutions. Wordpress.com was hosting it for a while. At some point, they made changes to their user profile settings, and some users were having issues I couldn’t help them with. I moved to self-hosted so that I had enough control to address these issues. Besides, our disk usage was growing and I was likely to get priced out of the free plan.

There are several shared plans that I looked into. They often come with an email serve I can use, but my experience with them hasn’t been great. Running a DigitalOcean droplet works great, until it doesn’t. Then it takes all Saturday to figure out what’s goin on. There is a next tier of plans that help you manage a VPS. [ServerPilot](https://serverpilot.io/) and [RunCloud](https://runcloud.io/) are a couple of examples. They help with the setup of the web server and database, but after that, you’re on your own. They don’t have a mail server, and only the foolhardy run their own mail server. Then I found [CloudWays](https://www.cloudways.com/en/). It does all the stuff ServerPilot and RunCloud do, but they also offer mail server add-on. For $1/month, I can add a RackSpace mailbox. I use this for incoming post-by-email traffic. Then for a few cents per 1000, they offer an outgoing SMTP server. I could (and have) patched this all together with a service like [Migadu](https://www.migadu.com/). But having it integrated with the server is a big plus.
