---
layout: post
title:  CloudFlare front end has been added
tags: update
---
# CloudFlare implementation

OISM now routes all public web traffic through CloudFlare, then haproxy, then finally to our server.

This required changes in the web server configuration to find the original client IP addresses that CloudFlare puts in a different header than haproxy did, so client IPs were not being logged correctly. This also broke the deploy webhook endpoint which is locked to the github IP netblocks. This post is testing that that has now been fixed.
