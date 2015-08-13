---
layout: post
title:  "Networking issues may be resolved?"
date:   2015-08-13 15:01:10
categories: jekyll update
---
# Networking Issues Resolved?

The morning after the seemingly successful activation, I found pages was broken again.
Accesses were failing and nothing was getting logged from the attempt.  GitHub pushes
were failing with timeouts.

Turned out this was due to two factors:

1. a faulty load balancer, which was offline during the initial roll-out. When Carl
started it up later that night, things broke. This was fixed this morning.

2. we had proxy_protocol enabled on the http listener which was apparently incorrect.

This post is partially to try another push and make sure All's Well with the GitHub pushes,
but right now we seem to be working well with both load balancers enabled.

Carl says there is still a potential issue when both load balancers are up but one of them
loses network connectivity with our server, and they're working on a solution for that.
