---
title: "Terminal is a Craze"
seoTitle: "Terminal Craze Takes Hold"
seoDescription: "Discover the journey from terminal noob to enthusiast with tools like NeoVim, iTerm, and custom scripts!"
datePublished: Mon Jul 29 2024 21:42:04 GMT+0000 (Coordinated Universal Time)
cuid: clz7ilg9200090ajsdh0wd8y7
slug: terminal-is-a-craze
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1722288839688/1f74df7c-ea08-406e-991f-10f1138b9891.png
tags: terminal, craze

---

Have you ever looked at the plain black terminal where you do `python3 hello.py` and results pops up. It looks so ugly when you see all those big lines of errors. You just want to avoid it.  
But then you have `unixporn` reddit where you look at people's terminal and you are like "ohh my gaaahhh"!!! Their terminals and setup makes you feel just like the name suggests, atleast for some people, the cool people!

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1722288956589/8fbdb115-a5d6-40aa-b2ae-4758223555a8.png align="center")

For me, terminal is a relaxation. Earlier I used to find it boring or useless I would say. But since that one day I was shown the train on terminal `sl`, my point of view changed and I went on a journey to discover how the hell a smoking train came into terminal! And that lead to the discovery of this world about Terminals, TUI's and CLI's and how I started to love it(well atleast so far).

## History

It all started back in January 2024. Databased Club (UG Computer Science Club of IISc) organised **Missing Semester** sessions based on the MIT's one to teach the students some basics of terminal, git, etc. At the time, here was my level of knowledge-

1. I did not know what is shell, shell scripting, bash. I just knew `bash hello.sh` or simply `./hello.sh` works.
    
2. My MacOS terminal was the one you get when you newly purchase Mac. Absolutely no configs. I did not know zsh, fish, powershelgl(yes even that).
    
3. Difference between terminal and shells. Forget about the word "Emulator".
    

I never even opened up Terminal, I used to use VS code terminal for all things(mainly python). So you can call this Level 0 - Noob Giga Max. Even my batchmates knew more than me(oh wait, FAAR more than me).

In the first few sessions, I learnt that `man` page is something to see info about commands, absolutely nothing about `git` and `trains` exist on terminal along with `cowsay`. That's when the sessions stopped and exams came. Fast forward ...

In March, I got some free time to look about `sl` and I discovered `Homebrew`, the god! And then I started watching `Josean Martinez`, `Typecraft` and `ThePrimeagen` videos about customising your terminal, changing your "Emulator" to iTERM(which I still use), about `Vim`, `NeoVim`, `Tmux`, `fzf` and much more. In April, in between the holidays I got for Math exam, by then my level of knowledge became LEVEL 3: Learning Vim (over Emacs) and that too NeoVim(noobs go for brand new fancy stuff), I was configuring my `NeoVim` by some Youtube videos. And then I never used it!

## Catalyst

In between I discovered "Edex-UI". OH!!! MY!!! GAAAAHH! That was the best thing I ever wanted to see. Although it took too much RAM that it ran slow on my small Mac, but it's fine. It gives me "chills" whenever I see it boot!

## Evolution

My end-sems of first year ended and by then I would say my knowledge was LEVEL 4: Learning Actual Vim (over Emacs). Sorry I heard way too many better reviews for Vim than Emacs. Cause the population for Emacs &lt;&lt; Vim(or Neovim) users that Emacs people need to shout "EMACS! EMACS! EMACS! EMACS!" many times to prove their point, unlike Vim users.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1722288970935/f607ac94-73e3-42c1-8e72-7ab9b2fe3aec.png align="center")

Anyways, I started my summer with a good Tmux, NeoVim configs and I dived into the world of terminal tools and how they work. I learnt you can make terminal tools using "ANY LANGUAGE". And that's why my bird brain went for "SHELL SCRIPTING" for my first `TERMINAL TOOL`!

## My Creations

### Cheatshh

I saw people loved using cheatsheets and there were CLI's for the same purpose to store then locally for people to refer. So I noticed there was no CLI which used fzf to store groups of commands. So I made cheatshh! In shell script! Why? Cause I thought changing fzf preview would be easier like this.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1722289005680/058b39a6-85df-4890-932f-ffd89ab91f3e.png align="center")

It has the below features -

1. Add, edit and delete commands and groups
    
2. fzf wrapper for commands and groups with preview having TLDR and custom text
    
3. Bookmarking, changing some settings like if you want something else apart from TLDR, etc.
    

I did not understand the value of "Releases" and how Pypi and GitHub releases work. I made 4 releases within a month. Any new feature =&gt; RELEASE! But I realised that if I were to critique someone based on this, I would rate him poorly. So the next release, which actually deserved a released was made a month later.

Check it out at: https://github.com/AnirudhG07/Cheatshh

### Typeinc(+mini)

I had gotten fond of curses. In my sem, I made a lot of creative things with python turtle and curses library. And I wanted to make something COOL! I wanted to make a terminal of my own. I had designed a curses keyboard which would move a key up-down when you press a key. I thought simply make a box, input text there, subprocess run it and boom! done. But all hell broke loose and I coudn't do it. But I learn soo much that I made a Typing speed test. I just had to give premade text and use my experience to just color it character by character, design some scoring altos and you are done!

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1722289115393/b2b3c67f-3ef4-4c67-adb1-17dff51b0d50.png align="center")

This was my first curses based project and I started getting a hang of things after this. How Pypi publishing works, how to make Homebrew Tap and things started looking good.

Then I made a smaller version, with less UI for smaller screens since a friend of mine was having issues with all the components. This took me a day, cause I had to just remove stuff and get it work for my friend.

Check it out at: https://github.com/AnirudhG07/Typeinc

### morseet

This was I made just cause the UDEMY course I took on Python had an assignment, but I was not gonna stop on just converting text to morse, I made a whole python CLI which can do -

1. Text to morse and morse to text
    
2. SOS signals and configurations
    
3. Point 1 for an input file
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1722289174898/53edad88-5ba1-4b05-bd4f-96f9f173e1e4.png align="center")

See! Took my 2 days for everything, cause I know how and what to do.

Check it out at: https://github.com/AnirudhG07/morseet

### ntfyme

Again, same inspiration but now task was to "automate something in your life". I always wanted (since before January) a way, my code ends and I get a notification. I coudn't find one and if I did, didnt fit my expectations.  
I took this change to make `ntfyme`, which is a notification tool for your command, which will run and notify you with Output, Errors, Return Code, Time taken, Pid, etc. through local notification, Gmail, Telegram, etc.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1722289185589/12c1a18a-1a2b-4771-bf47-b645f6c136f3.png align="center")

  
This was an easy task to make and a bloody hard task to debug to make work for all platforms (MacOS, linux, windows and WSL). WSl was a pain to deal with, but at the end it works!

Check it out at: https://github.com/AnirudhG07/ntfyme

## Yazi

Yazi is my love! It is the best file manager EVER! Better than ranger, mc, lf, nnn, etc. I discovered Yazi when `Typecrft` used it in his video and ever since, I was in love! I made plugins for it, made some docs contributions and made `awesome-yazi` which is awesome repository for YAZI plugins!

Check it out at: https://github.com/AnirudhG07/awesome-yazi

## Forward ahead

I learnt so many things in my summer before 3rd sem starts. I learnt Vim motions, and I am actually using NeoVim for most work, tmux, LAZYGIT (another BANGER), Yazi, Taskwarrior(just very HANDY) and much more.

I will keep making more and more terminal tools. Not just python, but Go(learning) and hopefully JS, rust and more language in future.

My laptop just became Level 10 now. I love my configs(https://github.com/AnirudhG07/dotfiles) and sketchy bar, borders, iTERM, zsh, p10k and what not!

Terminal is a Craze, if you start loving it, it can become a dull shit to cool shit!