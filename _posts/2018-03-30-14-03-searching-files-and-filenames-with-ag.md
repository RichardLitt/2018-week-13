---
layout: page
title: "Searching files and filenames with ag"
date: 2018-03-30T14:03:14Z
image: /assets/img/logo.png
---

I use a folder called `projects` for holding my GTD projects, in Markdown files. I wanted a way to search for the occurrence of a word - say, `fritz` if I wanted to message my friend [@fritzvd](https://twitter.com/fritzvd) - but also to find that word if it was in a filename. I use [the silver searcher (`ag`)](https://github.com/ggreer/the_silver_searcher) because it is faster than `grep`, but I couldn't find a way in the man files to combine both `-i` for ignore case and `-g` for finding patterns in filenames. A short trip to my `~.bash_profile` later, and I've got this:

```sh
function aga() {
  ag -i $1
  ag -ig $1
}
```

Maybe not the most convenient, but it should work for now.

Ironically, I had to use `grep` to find that command in my `.bash_profile`, because `ag` doesn't have the `-n5` command I wanted. Let's fix that.  
...  
A quick trip to the `man ag` files later, and I've got this: `cat ~/.bash_profile | ag 'ag' -C5`. Glad I won't have to see that problem again.
