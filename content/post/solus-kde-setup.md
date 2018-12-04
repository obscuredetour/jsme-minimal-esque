---
title: "My Solus KDE Plasma Setup"
date: "2018-12-03"
time: "3"
image: "/images/kde-banner.png"
description: 'This is a collection of my notes on how I prefer my Linux systems to be setup. Regardless how specific, perhaps others will find my setup info useful.'
tags: ["solus", "linux", "kde"]
---

A blog post by [Andrew Crouthamel -- My KDE-Centric Linux Laptop Setup](https://andrewcrouthamel.wordpress.com/2018/11/28/my-kde-centric-linux-laptop-setup-part-1/) recently inspired this post.

# Introduction

This is a collection of my notes on how I prefer my Linux systems to be setup. This is notably specific to my desktop, a multi-monitored workstation that I use mainly for web development and educational purposes. Regardless how specific, perhaps others will find my setup info useful.

## My system

My system is currently running [Solus KDE Plasma](https://getsol.us/) which can be downloaded [here](https://mirrors.rit.edu/solus/images/Solus-Plasma-Testing-v1.iso). I have been running this install for ~6 months without issues. Read the recent [Solus blog post — Shiny Delights](https://getsol.us/2018/10/24/shiny-delights/) about their KDE Plasma flavor. My humble system specs for the curious are below.

### System specs

- **Motherboard:**  Asus ROG Strix X470-F
- **CPU:**  AMD Ryzen 5 2600
- **RAM:**  G.SKILL TridentZ RGB Series 16GB (2 x 8GB) DDR4 3200 (PC4 25600) F4-3200C14D-16GTZR
- **GPU:**  AMD Radeon HD 7790
- **HDD:**  ADATA SU800 128GB

{{< figure class="image fit" src="/images/desktop-neofetch_20181203-sm.png" alt="Desktop-main display, neofetch screenshot">}}[Full resolution](/images/desktop-neofetch_20181203.png)

## Software

Solus is commendable (for me) in the sense that I have little to do to get my system where I want. Other distros may involve more or less steps depending on pre-installed applications, packages, and various configurations.

##### Current Software Versions

- **Solus:**  3.9999
- **KDE Plasma Version:**  5.14.4
- **KDE Frameworks Version:**  5.52.0
- **Qt Version:**  5.11.2
- **Kernel Version:**  4.19.5-101.current

Most of these applications can be found in Solus' repositories. You can install via CLI or the Software Center. 

##### CLI Instructions

`sudo eopkg install packagename`

### System
[Git](https://git-scm.com/) - this is mainly used for web development purposes. Also used for software retrieval from various git repositories.

+ `sudo eopkg install git`
	
[Grsync](http://www.opbyte.it/grsync/) - a GUI utility for rsync. I use this to backup my `/home` directory to a network drive.

+ `sudo eopkg install grsync`

[Neofetch](https://github.com/dylanaraps/neofetch) - display system information.

+ `sudo eopkg install neofetch`

### Desktop
[Latte Dock](https://github.com/KDE/latte-dock) - fantastic desktop widget capable of great customization. I use it as my taskbar, my Latte Dock config can be downloaded [here](/images/obd-latte-config.layout.latte). See above [screenshot](/images/desktop-neofetch_20181203.png) for visual representation.

+ `sudo eopkg install latte-dock`
+ Additionally, add the Color Picker Plasma widget. This is pre-installed on Solus and visible in the existing widget list. Just need to add it to a dock/panel/desktop.

[Redshift](http://www.opbyte.it/grsync/) - a utility for adjusting screen temperature based on time of day. This reduces eye strain.

+ `sudo eopkg install redshift plasma-redshift-control`
+ Additionally, install the [Redshift Control](https://store.kde.org/p/998916/) Plasma widget. The above command installs both packages.

##### Desktop Themes
- In the KDE's 'Desktop Theme' application select 'Breeze - Dark'. If on Solus, this should already be installed (and maybe the default theme).
- Additionally, in KDE's 'Icons' application select the 'Get New Themes...' button. Look and search for 'Newaita-dark' and click install, wait and then click use.

### Multimedia
[Google Play Music Desktop Player](https://www.googleplaymusicdesktopplayer.com/) - An awesome cross-platform desktop application capable of playing Google Play Music.

+ `sudo eopkg install google-play-music-desktop-player`

[Gravit Designer](https://designer.io/) - Cross-platform design tool. The closest application Linux users get to Sketch, Illustrator, or Affinity Designer. Completely usable in a browser, but read on for a standalone app.

  + For standalone app, visit [https://designer.io/#download](https://designer.io/#download) and download the respective file. Extract these files into a directory where Gravit Designer should reside. I typically place extra apps in an '**apps**' subdirectory within my user directory like so: `/home/USERNAME/apps`.
    + For Gravit Designer it would look like this path:<br>`/home/USERNAME/apps/gravit-designer/`
    + Once all files are extracted and in a folder open the file 'Installation-Guide.html' and follow the instructions.
	
[Audacity](https://www.audacityteam.org/) - A fabulous cross-platform audio editing software. I edit audio occasionally.

+ `sudo eopkg install audacity`
	
[Kdenlive](https://kdenlive.org/en/) - For the occasional video edit.

+ `sudo eopkg install kdenlive`
	
[SimpleScreenRecorder](http://www.maartenbaert.be/simplescreenrecorder/) - A great and simple to use screen recorder. Great for tutorials and explaining UI/UX concepts.

+ `sudo eopkg install simplescreenrecorder`
	
### Tools & Productivity

[Notion](https://www.notion.so/?r=8e7e0aeafa67404e91ce132df72d8e51) - All-in-one workspace. I absolutely love Notion. It is capable of a little or a lot. Notes, docs, knowledge base, wikis, tasks, project management, spreadsheets & databases. Please note my shameless and obligatory affiliate link. Fully usable in a browser, but I like to have a standalone app even if it is simply electron wrapped. Luckily, someone has created an [electron app of Notion.so](https://github.com/sysdrum/notion-app).

- Standalone [Notion](https://www.notion.so/?r=8e7e0aeafa67404e91ce132df72d8e51) app on Linux requires git. Navigate on your system where you would like the app to reside. I use an **'apps'** subdirectory within my user directory, eg. `/home/USERNAME/apps`.
  -  Open a terminal window in this directory and run the command `git clone https://github.com/sysdrum/notion-app.git`. This will copy the app and create a directory named **'notion-app-master'**.
  -  Navigate inside this new directory `cd notion-app-master` and run `./create_desktop_file.sh`. This will place a **'Notion.desktop'** file in your `.local/share/applications` folder.

[Visual Studio Code](https://code.visualstudio.com/) - An excellent code editor that I have come to prefer.

+ `sudo eopkg install vscode`
	
[Google Chrome](https://www.google.com/chrome/) - While not my main browser, I still use it for Google services and testing. You won't find this in Solus' repositories because it is closed sourced. However, within Solus' Software Center, under the Third Party section Google Chrome can be installed. Alternatively, the CLI commands are below, taken from [here](https://getsol.us//articles/software/third-party/en/#google-chrome).

+ `sudo eopkg bi --ignore-safety https://raw.githubusercontent.com/getsolus/3rd-party/master/network/web/browser/google-chrome-stable/pspec.xml`
+ `sudo eopkg it google-chrome-*.eopkg;sudo rm google-chrome-*.eopkg`

[Gitkraken Git Client](https://www.gitkraken.com/git-client) - An amazing cross-platform Git client that has an unprecedented visual git representation. This is installed via Solus' Software Center, under the Third Party section. Alternatively, the CLI commands are below, taken from [here](https://getsol.us//articles/software/third-party/en/#git-kraken). This can also be installed via [Gzip](https://www.gitkraken.com/download/linux-gzip) or [Snap package](https://snapcraft.io/gitkraken).

- `sudo eopkg bi --ignore-safety https://raw.githubusercontent.com/getsolus/3rd-party/master/programming/gitkraken/pspec.xml`
- `sudo eopkg it gitkraken*.eopkg;sudo rm gitkraken*.eopkg`

[Discord](https://discordapp.com/) - Text & voice chat application.

  - `sudo eopkg install discord`

## Conclusion

The Linux desktop has come a long way in the last decade. Things are pretty easy. I could have avoided the command line for most of this. Additionally, because of Solus I did not have to install many applications like Libre Office, Gimp, and Inkscape to name a few. If you aren't using some Linux flavor by this point, you should.