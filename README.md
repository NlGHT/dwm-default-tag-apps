default tag applications
========================
This repo is for the `default tag apps` patch as seen on [the official dwm.suckless.org patch list](https://dwm.suckless.org/patches/default_tag_apps/).  It is here to serve as an easy way to try dwm with the patch applied but also for submitting issues and pull requests.

If you are new to dwm, you can find out what it is and read more about how it works [here](https://dwm.suckless.org/).

Description
-----------
The patch's purpose is for those who dedicate each tag to certain general tasks.  Tag 1 might be the tag used for all terminal tasks, tag 2 might be for internet/browser things etc.  When you have these tags already mapped out, generally you open one application more than any other in each tag.  This patch aims at harnessing this workflow for improvement of speed and practicality.

Usage
-----
Setting a key to spawndefault will launch the default application set for the tag you are currently on.  You can set the applications to be run for each tag in `config.h` as seen here:

`*defaulttagapps[] = { "st", "librewolf", "onlyoffice-desktopeditors", "nautilus", NULL, "lutris", "krita", "ardour", "mirage" };`

The example keyboard shortcut included is `Mod+s` but of course feel free to change it to whatever you want.

Currently multi-monitor is supported up to 8.  You can change this by changing the size of `lastchosentag[8]` and `previouschosentag[8]` in `dwm.c`.

Additionally there is now support for instantaneously spawning a new app if there is nothing open on the given tag being switched to.  This behaviour is configured by the variable `spawnonviewchange` located at the top of `config.h`/`config.def.h`.

You can quickly try out the patch by compiling with `sudo make install` in the project directory.

Download
--------
Please see the repo [releases](https://github.com/NlGHT/dwm-default-tag-apps/releases) for the latest patch.  Alternatively you will find all the major patch versions on the [official suckless patch page](https://dwm.suckless.org/patches/default_tag_apps/).
