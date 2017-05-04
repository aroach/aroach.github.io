---
layout: post
title: Teaching My Kids Linux 
---

My kids liked the idea of learning programming, but they really weren't
making much progress and would lose interest pretty quickly.  

As a result, I turned my attention to something more tangible for them.
After brainstorming a bit, and figuring sysadmin skills are good to konw
as well, I decided to teach them some Linux skills.

The first project that we started with was installing Linux (we picked
Ubuntu even though I could've gone hardcore with Gentoo). We actually did
this twice: first, into a VM; second, on an actual PC.

When installing it on a PC, I asked them questions like, "How do you think
you can put a new OS onto the computer?"  Which led to learning about
updating the BIOS boot order, how to install a bootable linux onto a USB
stick (netbootin), and hard drives vs. memory.  We also learned about
hostnames and creating user accounts.

After installing the OS, we started exploring Linux.  They immediately
wanted to use the GUI, but I guided them to open Terminal. We used:

* `ls` and `ls -la`
* `touch`
* `cp`

Finally, we loaded a text editor.  Yes, we tried out `vi` (sorry my
`emacs` friends).

* `:w`
* `:q` and `:q!`
* `j` `k` `h` `l` for navigation

There ain't no keeping my kids away from Minecraft, and so the next stop
on our Linux adventure was to install a Minecraft Server.  Lots of fun
tools here to learn about:

* `wget`
* `useradd`
* `usermod`
* `passwd`
* `chmod`
* `chown`
* `apt-get`
* `sudo`
* `telnet`
* `ssh`

Of course, we didn't cover all of this is one day, but have split up these
exercises over many weekends.  

I plan to add more posts documenting our adventures with Linux.  Would
love to hear from other parents who might be trying to help their kids
with Linux literacy.
