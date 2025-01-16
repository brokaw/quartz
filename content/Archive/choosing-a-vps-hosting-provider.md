---
title: "Choosing a VPS Hosting Provider"
date: "2016-02-09"
updated: 2023-03-26
categories:
  - "words"
---

I finally got my site up and running. I could have launched it a lot sooner, but I decided to take a detour in the realm of VPS providers. It makes sense that one of my first posts would summarize my findings.

If you’re in the market for a Virtual Private Server (VPS), there’s a good chance you’ve looked at [Amazon EC2](https://aws.amazon.com/ec2/), [Linode](https://www.linode.com/choosing-linode/), and [DigitalOcean](https://www.digitalocean.com/features). Amazon essentially defined the market. Linone is a longtime darling of the Hacker News crowd. DigitalOcean is the venture capitalist-funded upstart. All are worthy of your business. Here’s my unscientific, unquantified impression of their relative strengths and weaknesses.

## Amazon Web Services

Amazon Web Services (AWS) is a smorgasboard of services, of which EC2 is just one. All services are supported by a comprehensive API with client libraries in just about any language you’re likely to care about. The array of services is their greatest advantage and their greatest weakness. Amazon has the tools to build just about anything you can imagine. Way beyond virtual servers, they have globally distributed CDN, hosted NoSQL and SQL servers, persistant virtualized storage (EBS), a way to declare and instantiate all your services (CloudFormation), and authentication scheme to tie it all together. Even that just scratches the surface. Email, SMS, APNS…the list goes on. But where to start? It’s hard to get your head around it all, and it’s easy to get overwhelmed by the information. You have a site to launch; it’s better not to get too distracted.

EC2 has a reputation for being overpriced and slow. But this is all relative to your use case. EBS is blamed for much of the slowness. I can buy EBS-optimized EC2 instances, but then I’m in a $50/month/server scenario, and I’m looking at $10-$20 price range. If I had an infrastructure than could truly take advantage of the flexibility of EBS, and leverage the synergy of complementary AWS services, I’d probably be happy to pay the difference. In short, it feels like it is built for the likes of Netflix, not the small app builder or blogger.

Also, pricing can be hard to estimate. If you’re using Amazon’s pricing estimator, plug in a couple terabytes of outgoing data (the amount you get for free at DigitalOcean and Linode). Your cost just went up a couple of hundred dollars.

## Linode

Linode was doing VPS before it was cool. They have a dedicated following who praise their tech support. Their web UI is an eyesore but complete. And if you’re doing it right, you’re setting up your server with the API instead of the web UI.

Linode exposes their virtualization underpinnings more than others. Setting up a server is a multistsep process. Choose a distribution, initialize a disk, apply the image, boot the image. This reflects the reality, but sometimes I wonder if it would be better to present a more abstract interface.

Linode has a unique initialization process. It uses standard scripts (shell scripts, or python, etc., if you image has that installed). They have special syntax to collect variables via web form (so you can enter the MySQL password, for example), and to include (or “source”) other StackScripts. Stackscripts can be shared with the Linode community.

## DigitalOcean

DigitalOcean is slick and clean. They have a nice UI which feels simple and much less powerful than Linode. Again, you’re probably using an API instead of the web UI, so it is less important than it might seem.

DigitalOcean supports cloud-init for images that take advantage of it. You can provide a cloud-init configuration file as user data that is available to the image the first time it boots up. It’s no more functional that Linode’s stackscripts, but the configuration file is more delcarative, where the StackScript approach is more procedural. It’s really easy to declare, say, package requirements and let cloud-init take care of the process of installing the package.

DigitalOcean supports associating an SSH public key with your account and have any new image use that public key for login. Linode supports public key insofar as you can add it to a StackScript and put it in the right place, but it was nice to have it build into the deployment process.

If you’re a FreeBSD fan DigitalOcean has images for you.

## Conclusion

I decided that I was spending to omuch time reading documentatin with AWS. For the most part I had decided on DigitalOcean, and had built up a nice workflow to setup and manage a wordpress installation. My informal benchmarks didn’t show much of a difference between DigitalOcean and Linode. As it turns out, I don’t have much of a strong preference between the two. If the workflow offered by Linode fits your style better, I have no doubt you’d be pleased.
