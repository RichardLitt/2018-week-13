---
layout: page
title: "Fixing Bushwhich"
date: 2018-03-31T10:46:22Z
image: /assets/img/logo.png
---

This morning I am powering through all of my 300+ projects in my projects folder, and triaging and doing any next actions that take next than 5 minutes.

One of the first things to do was to fix [bushwhich](https://github.com/RichardLItt/bushwhich), my old choose-your-own adventure game where I bike around my old neighbourhood, Bushwick, in Brooklyn. I had moved it off of the domain it was on and to [https://richardlitt.github.io/bushwhich](https://richardlitt.github.io/bushwhich), but the assets weren't working. I set my timer to go.

It took me ten minutes, 30 seconds to fix the problem; BASE_PATH wasn't being used anywhere, and wasn't set in the config. I removed all of the hardcoded paths, set base path to the domain, and grepped for all `<a href="/">` and changed them to `<a href="{{ BASE_PATH }}">`. Upload, refresh, and it's working now. I've changed the link on my project on burntfen.com, too.

Not a bad amount of time to end a project. Ricardo asked me to blog about it, so here I am.

On to the next thing.