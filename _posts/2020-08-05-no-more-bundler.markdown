---
layout: post
title:  "Breaking change: no more bundler"
date:   2020-08-05 14:28:00
categories: jekyll update
---
# BREAKING CHANGE

As of today there have been some major implementation changes.

Bundler support has now been disabled. Sites will now be processed directly
by the system install of jekyll with the approved and managed versions of
plugins whitelisted by GitHub.

Gemfile and Gemfile.lock are now completely ignored on the server.

Timestamps have been added to logging to aid with debugging.
