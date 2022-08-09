---
layout: post
title:  "Testing jquery versions"
date:   2022-08-09 14:28:00
categories: update
---
Testing jquery 2.x and 3.x for compatibility with leaveNotice and nist-header-footer.

Here is an off-site URL to test leaveNotice with:  [https://www.dell.com](https://www.dell.com)

The main issue is $.unload() was deprecated in 1.8 and removed in 3.0. leaveNotify changed that call to $.on('unload', function(){})
