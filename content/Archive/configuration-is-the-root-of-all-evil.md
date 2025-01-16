---
title: "Configuration is the Root of All Evil"
date: "2018-09-13"
categories: 
  - "words"
---

From the fish shell [design document](https://fishshell.com/docs/current/design.html):

> Every configuration option in a program is a place where the program is too stupid to figure out for itself what the user really wants, and should be considered a failure of both the program and the programmer who implemented it.

If any program could go wild with user configuration options, a shell program could. Its notable that fish explicilty tries to avoid this.
