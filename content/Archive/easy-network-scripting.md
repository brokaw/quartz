---
title: "Easy Network Scripting"
date: "2016-01-27"
categories: 
  - "words"
---

I just learned about nc and was so excited I had to write about it. From the man page:

> The nc (or netcat) utility is used for just about anything under the sun involving TCP or UDP. It can open TCP connections, send UDP packets, listen on arbitrary TCP and UDP ports, do port scanning, and deal with both IPv4 and IPv6. Unlike telnet(1), nc scripts nicely, and separates error messages onto standard error instead of sending them to standard output, as telnet(1) does with some.

It also communicates with UNIX Domain Sockets easily. I have been using Python for that, but this is easier for simple and one-off tasks.
