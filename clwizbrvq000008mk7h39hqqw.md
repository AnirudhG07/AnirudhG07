---
title: "An easy way to remember all your Commands for your Terminal"
seoTitle: "Terminal Cheatsheet"
seoDescription: "Cheatshh is your command line cheatsheet manager, written in shell script. Now you don't need to remember all the commands. Read more."
datePublished: Thu May 23 2024 08:16:47 GMT+0000 (Coordinated Universal Time)
cuid: clwizbrvq000008mk7h39hqqw
slug: an-easy-way-to-remember-all-your-commands-for-your-terminal
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1716405075876/aa671190-6036-4ea4-b7c1-00aef5602e39.png
tags: terminal, cheatsheet, terminal-command

---

For developers, the usage of Terminals is an essential need. Some of them need the Terminal for running programs, for testing purposes, maybe just showing off, while some of them live in the Terminal by using NeoVim, Tmux and custom magical keybinding setups, etc. The terminal becomes a must for everyone going in the field of coding and dev.

But remembering all the commands, the git and the docker commands, all the amazing TUI's and CLI's present in your machine, the aliases you made is simply impossible. Even if you do remember them, it is impossible to remember all the functionalities that you need.

### Cheatsheets are the solution!

Just like you make cheatsheets before your exam to remember historical events(or maybe math formulae, etc.), you need cheatsheets to store all your commands, their functionalities and your personal comments on them. Good thing is, nobody cares if you remember them or not as long as you get the work done. There are various cheatsheets available for each application, and multiple tools too. But I would like to share a tool which I made for just this purpose.

### Cheatshh - A command-line cheatsheet manager

Cheatshh is a fuzzy-finder based solution to your command line cheatsheet, written in shell script for Unix. You don't need to search for the long-lost commands you once used years ago, just add them to cheatshh and forget about them. You don't need to type large commands either, just put it on cheatshh and copy it directly!

With `Cheatshh` you can

* Add commands to your cheatsheet and have personal comments for them
    
* Make your own groups of commands
    
* View TLDR and Man pages for each command in fzf preview
    
* Edit groups and commands
    
* Delete commands from specific groups
    
* Bookmark grouped commands
    
* Just press Enter on a command and copy it to your clipboard
    
    and many more functionalities...
    

You can visit [https://github.com/AnirudhG07/cheatshh](https://github.com/AnirudhG07/cheatshh) to see more information.

It is a user-friendly and a very handy tool.

```bash
$ cheatshh
```

You get the list of a groups, commands that you set with their personalised description and tldr in the fzf preview. You can enter in any group and see the descriptions of the commands in them.

![A group command list image of cheatshh](https://cdn.hashnode.com/res/hashnode/image/upload/v1716405403912/1b2ef768-2c73-4e6b-91f7-9ad045816dfa.png align="center")

Now you won't have a hundred commands lined up, but just sort them out as groups and you are done.

### Features

Let's dive into some of the feature of Cheatshh in detail and get to know how they can help us -

### 1\. Grouping commands

Your cheatsheet would have lots of command, some of them maybe for git, productivity, networking etc. while some maybe just for show off. And having a big cheatsheet is sometimes messy. Thus grouping them is a better way to segregate them and access them faster.

The benefit of grouping is not just to maintain neatness, but a reminder of your other tools that may perform similar functions. Often you have a ton of tools to use, yet you use a few of your favourites. Getting to know all your tools can sufficiently increase your productivity.

### 2\. Bookmarking

The bookmarking feature, as the name suggests allows you to mark commands with a `bookmark` tag which enables it be visible in the main preview apart from your main group preview. This helps you to reach your favourite tools faster and also put them in its respective group.

### 3\. Deleting commands & groups

Sometimes you have created an alias which you never need again, or you have some tools which are deprecated/you deleted them. You might want to delete them from your cheatsheet too. Thus you can simply delete the command. Since cheatsheet allows unique commands, thus it will remove that command from every group and the database.

However deleting command will result in the deletion of the group but some common commands present in many groups will not be deleted. This is really helpful and allows you to play around with groups without fearing the loss of a command.

Cheatshh has various more basic features like adding and editing, but these are as the name suggests, simply adding and editing groups and commands. Play around with different cheatshh functions and get comfortable in them.

### More tools for Cheatsheets

Developers have made various open source projects like tldr, cheats.sh, etc. to just call it through your terminal like -

```bash
tldr ls # tldr <command>
```

This prints out the top most used functionalaties for the command which makes our life so much easier than racking our heads reading the MAN pages. Oh boy!

Github also has a variety of repositories containing various cheatsheets for different applications. There are also various Terminal user interfaces for cheatsheet managements like Navi.

### Summary

For developers, using Terminals is essential, but remembering all commands, aliases, and functionalities is challenging. Thus using cheatsheets for commands is a must. Cheatshh is a command-line cheatsheet manager written in shell script for Unix. Other tools like tldr and cheats.sh also help by providing quick command references. The whole idea is to be fast and productive, just don't waste your time finding the docs of same commands again and again, use cheatsheets!