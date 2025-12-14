# How to use my desktop
How you can run the desktop, what are the wrapper commands, etc.
## Navigation
- **[How to run the Desktop](#run-desktop)**
- **[Fix Slow APT/PKG install speed](#slow-speed)**
- **[Run Applications using CPU instead of GPU](#app-cpu)**
- **[Run apps from PRoot on Desktop](#proot-on-native)**
- **[Daily-life Storage Cleaner](#cleaner)**
- **[How to stop the desktop](#stop-desktop)**
- **[In-built Command to know all of these](#huh)**

<br>

## How to run the desktop <a name=run-desktop></a>
For running the XFCE4 desktop environment 

You need to run:
```
termux-xfce4
```
It will automatically start the desktop environment with Hardware Acceleration.

---
<br> 

## How to fix slow APT/PKG download Speed <a name=slow-speed></a>
Sometimes due to slow or poor mirror your download Speed drops even though your internet speed is fine. 

Like when you run `pkg install glmark2` is takes hour to download but progress (installation) is fast. 

To fix it run:
```
termux-fastest-repo
```
And just enter to following questions, it will choose the fastest mirror available in the world

> [!WARNING]
> Some mirrors may have delay synchronisation, meaning upgrades of all of the packages may get delay. And sometimes rarely due to delay synchronisation packages gets broken (due to dependency version incompatiblity)
> So switch to official Termux mirror for reliable, synced, safe installation, and switch to fastest mirror when installing something big

---
<br>

## Run app using CPU <a name=app-cpu></a>
Sometimes few app crashes because of few missing extensions on HWA

To fix that, you can run application using CPU, by running the following command:
```
apphwa llvmpipe appname
```

For an example:
```
apphwa llvmpipe chromium --no-sandbox
```
Yes, you can also add arguments like `--no-sandbox` it will work. And it will run using CPU instead of the GPU

---
<br> 

## PRoot apps on Native <a name=proot-on-native></a>
After running `termux-xfce4` it runs the desktop on Termux native. And you can't run PRoot applications. To fix that, I've made up a script.

Assume, you have Vesktop (a Discord client) installed inside your Debian PRoot environment, and you want to run it on your Native Termux Desktop.

To do this, run:
```
proot_program Vesktop --no-sandbox
```
Yes, arguments are supported, and it's needed to run the Vesktop. It will run inside PRoot, but will show up on your Termux native desktop

At the same way, you can execute CLI commands inside PRoot from Termux native, though it's not recommended.

--- 
<br>

## Storage cleaner <a name=cleaner></a>

If your Termux gets messy with storage, you can use this command daily to free up some storage

To do that, run:
```
native_cleaner
```

---
<br>

## Stop the desktop <a name=stop-desktop></a>
There's no In-built wrapper to stop the desktop. Although you can use `kill` command.

In order to stop, you have to go to app settings of Termux, and click on *Force Stop* to completely stop Termux and its desktop from running.

---
<br>

## In-built Command for these all commands <a name=huh></a>
If you want to memorize or see these commands, you don't've to visit this website again you can run `desktop-help` on your terminal, to see every commands and its usage.
