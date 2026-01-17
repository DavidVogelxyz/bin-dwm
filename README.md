bin-dwm
=========

`bin-dwm` is a collection of Bash scripts that should be on all Linux machines running dwm. This repo is often deployed in conjuction with [my dotfiles](https://github.com/DavidVogelxyz/dotfiles).

Usage
-----

Within the root of this project (`bin-dwm`) is a directory named `bin-dwm`. Create a symlink at `${HOME}/.local/bin/bin-dwm` that points to the *subdirectory* named `bin-dwm`.

Table of contents
-----------------

- [Usage](#usage)
- [Scripts](#scripts)
    - [backlight-check](#backlight-check)
    - [dimmer](#dimmer)
    - [dmenuunicode](#dmenuunicode)
    - [recompile-wm](#recompile-wm)
    - [renew-dwmblocks](#renew-dwmblocks)
    - [renew-wm](#renew-wm)

Scripts
-------

### backlight-check

Date created: 2025 Oct 5, Sun

`backlight-check` was written to address an issue with some machines (laptops) that boot at a brightness that is less than the screen's maximum brightness.

`backlight-check` makes it extremely easy, on any laptop, to quickly check if the brightness is maxed. If it's not, then the script will adjust the brightness to max. This is especially useful on laptops for which the brightness keys are not correctly configured.

### dimmer

Date created: 2025 Feb 19, Wed

`dimmer` was written to give `dwm` a "night light" feature.

`dimmer` was heavily inspired by a similar script written by YouTuber BreadOnPenguins. This repo includes an example cronjob for scheduling the night light functions. The script accepts up to 2 arguments: the screen brightness (as a percent, divided by 10) and a second (optional) argument to specify "night" colors.

### dmenuunicode

Date created: 2026 Jan 17, Sat

`dmenuunicode` was written in order to provide a user with a menu from which to copy emojis into the user's clipboard.

`dmenuunicode` is a rewrite of an identically named script by LukeSmithxyz. It provides the same functionality, but is written for Bash. Despite this, this version of `dmenuunicode` is also POSIX-compliant.

### recompile-wm

Date created: 2025 Oct 17, Fri

`recompile-wm` was written to quickly update `dwm` related software.

`recompile-wm` pairs well with `git_package_manager` (from [bin-linux]()). If updates are made to `dwm` related repositories, they can be quickly fetched and pulled with `git_package_manager`. Then, `recompile-wm` can be run to recompile all software. An additional benefit is the standardization aspect -- by running two simple scripts (that can be added to `PATH`), the user ensures that all software is updated, without worrying about "forgetting to update a repo", or "updating, but forgetting to recompile".

### renew-dwmblocks

Date created: 2025 Oct 24, Fri

`renew-dwmblocks` was written to allow the user a quick and easy way to restart `dwmblocks`.

`renew-dwmblocks` is useful when `dwmblocks` has been recompiled during the same session, but `dwm` has not. Therefore, the script enables the user to renew `dwmblocks` without renewing `dwm`.

### renew-wm

Date created: 2025 Oct 24, Fri

`renew-wm` was written to allow the user a quick and easy way to restart `dwm`, separate from the `sysact` script.

`renew-wm` enables the user to restart `dwm` from the command line. While it is likely faster to perform this operation using `sysact`, this script was largely at attempt to recreate the same functionality in a separate script.

`renew-wm` is useful when `dwm` has been recompiled during the same session, as "renew" restarts the window manager without closing all the programs that are currently running.
