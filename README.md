# Mouse Tiler

<img align="left" style="margin-right: 20px" width="90" height="90" src="./assets/icon.png">

<pre>
KDE KWin Script for tiling windows.
Allows you to tile your windows with minimum effort by moving the mouse just a few pixels.
</pre>

* Compatible with KDE Plasma 5 (KWin 5.27+). Ported from the [upstream MouseTiler](https://github.com/rxappdev/MouseTiler) for KDE Plasma 6.

* Tested on:
    - Debian Trixie running Wayland with KDE Plasma 5.27 and KWin 5.27

[![kde-store](https://img.shields.io/badge/KDE%20Store-download-blue?logo=KDE)](https://store.kde.org/p/2334027)


# Table of contents
<ul>
<li><a href="#features">Features</a>
    <ul>
        <li><a href="#features_released">Released so far</a></li>
        <li><a href="#features_planned">Planned for v1.0.0 (and beyond)</a></li>
    </ul>
</li>
<li><a href="#how">How it works</a></li>
<li><a href="#installation">Installation</a>
    <ul>
        <li><a href="#store">From KDE Store (Recommended)</a></li>
        <li><a href="#file">From File</a></li>
    </ul>
</li>
<li><a href="#setup">Recommended setup</a></li>
</li>
<li><a href="#system-settings">Changing system settings</a></li>
<li><a href="#remove-settings">Manually erasing settings</a></li>
<li><a href="#troubleshooting">Troubleshooting</a>
    <ul>
        <li><a href="#commandline">Command line</a></li>
    </ul>
</li>
<li><a href="#compatibility">Compatibility</a></li>
<li><a href="#getintouch">Get in touch</a></li>
</ul>

## <p id="features"></p>Features

* Two mouse tiling modes - Popup Grid and Overlay ( similar to FancyZones ) - you can use one or both
* Virtual desktop management
* Auto tiling (carousel or stacking style)
* Manual text configuration of the modes or [web layout editor](https://rxweb.epizy.com/mousetiler/editor.html)
* Multi-monitor support
* Follow system theme or use one of pre-defined color themes
* Highly customizable, from tile size to grid position (over 20 settings)
* Tiling works using mouse, stylus, touch (including Wacom) - press Ctrl+Alt+I to toggle input modes, or change default input mode in settings

![](./assets/info_animation_v4.gif)<br>
**Feature Preview**

![](./assets/popup_tiler.png)<br>
**Grid Tiler Default**

![](./assets/popup_tiler_all.png)<br>
**Grid Tiler All Layouts**

![](./assets/overlay_tiler.png)<br>
**Overlay Tiler**

![](./assets/virtual_desktop_v1.gif)<br>
**Virtual Desktop Manager**

![](./assets/center_in_tile_v1.gif)<br>
**Center In Tile**

**Auto Tiling**
[See video overview of auto-tiling here](https://www.youtube.com/watch?v=wKhfUGHrgIw)<br>

### <p id="features_planned"></p>Planned for the future

The future features depend on you.

Read this for details:
[Planned features and donation goals](https://github.com/rxappdev/MouseTiler/blob/main/PLANNEDFEATURES.md)

Voting and current results:

[![poll](https://wakatime.com/polls/0e8054f0-e168-4f00-b31b-ed6c17bd51af.png)](https://wakatime.com/polls/0e8054f0-e168-4f00-b31b-ed6c17bd51af)


### Feature requests to investigate

* Add additional titlebar button ? - System Settings > Colours & Themes > Window Decorations > ... > Configure Titlebar Buttons... (currently I do not believe this is possible to do from a KWin Script, but if anyone knows something I don't, please let me know)
* Re-investigate single key shortcuts (Alt / Shift / Ctrl)

## <p id="how"></p>How it works

Use one of two mouse adapted tilers (or both). The Grid tiler lets you quickly place your window by moving the window a few pixels. The Overlay tiler is a classical full screen overlay that lets you place your window into one tile, or span multiple tiles. Define your own layouts or use some of the many predefined ones.

### Use auto tiling

If you like using auto-tiling, there is fairly advanced support for carousel and regular auto tiling. Switch between up to three auto-tilers on the fly (Ctrl+Alt+X and Ctrl+Alt+C). Scroll overflowing windows by using left and right screen edges (or Ctrl+Alt+Left and Ctrl+Alt+Right). Toggle auto-tiling with Ctrl+Alt+A.

### Manage your virtual desktops

You can add new virtual destkops, auto-remove empty destkops, move apps between desktops and more.

### Center in tile

If you want to keep a window size, but center it in a certain place, you can use the center in tile shortcut (Meta+Ctrl+C).

## <p id="installation"></p>Installation

### <p id="store"></p>From KDE Store (Recommended)

1) Open `System Settings` > `Window Management` > `KWin Scripts`.

2) Click the `Get New...` in upper right corner.<br>
![](./assets/get.png)<br>
3) Search for `Mouse Tiler` and click on it (step `1` applies only with small window size)<br>
![](./assets/search.png)<br>
4) Click `Install`<br>
![](./assets/download.png)<br>
5) Enable `Mouse Tiler`<br>
![](./assets/tick.png)<br>
6) Click `Apply`<br>
![](./assets/apply.png)<br>
7) Click the configure icon to change the settings to your liking<br>
![](./assets/configure.png)<br>

Please note that changing settings requires some additional steps to apply due to a KDE limitation - see `Changing settings` below for more information.

### <p id="file"></p>From File

You can download the `mousetiler.kwinscript` file and install it through **System Settings**.
1) Download the .kwinscript file.
2) Open `System Settings` > `Window Management` > `KWin Scripts`.
3) Click the `Install from File...` in upper right corner.<br>
![](./assets/install.png)<br>
4) Select the downloaded file and click `Open`
5) Enable `Mouse Tiler`<br>
![](./assets/tick.png)<br>
6) Click `Apply`<br>
![](./assets/apply.png)<br>
7) Click the configure icon to change the settings to your liking<br>
![](./assets/configure.png)<br>

Please note that changing settings requires some additional steps to apply due to a KDE limitation - see `Changing settings` below for more information.

## <p id="system-settings"></p>Changing system settings

### **`IMPORTANT`**

Due to a bug in KDE, changing user configuration requires reloading the script. (A reboot works too.)

To make setting changes effective, **reload the script as follows**:

1) In `System Settings` > `Window Management` > `KWin Scripts`, untick `Mouse Tiler`<br>
![](./assets/untick.png)<br>
2) Click `Apply`<br>
![](./assets/apply.png)<br>
3) Tick `Mouse Tiler`<br>
![](./assets/tick.png)<br>
4) Click `Apply`<br>
![](./assets/apply.png)<br>

### <p id="remove-settings"></p>Manually erasing settings

If there is ever need to manually erase user data (do not do this unless you are a developer or really need it).

The application/window data is stored in `~/.config/kde.org/kwin.conf` under the key `...`.

The system user settings data is stored in `~/.config/kwinrc` under `[Script-mousetiler]`.

## <p id="troubleshooting"></p>Troubleshooting

### Remove screen edge highlight

To remove the visual screen edge highlighting when using the auto-tiler go to:

`System Settings` > `Window Management` > `Desktop Effects`

And disable "`Highligt Screen Edges and Hot Corners`".

### <p id="commandline"></p>Command line

In case there are any issues (such as a crash - which should never happen but just in case), this is how to disable the script from command line (open a console with `Ctrl+Alt+F5`):

```
kwriteconfig6 --file kwinrc --group Plugins --key mousetilerEnabled false
qdbus org.kde.KWin /KWin reconfigure
```

If the mouse tiler configuration contains corrupted data, it can be manually deleted in the file: `~/.config/kde.org/kwin.conf` under key `TBD`.

## <p id="compatibility"></p>Compatibility ##

Compatible with:
* <a href="https://github.com/rxappdev/RememberWindowPositions">Remember Window Positions</a> - use the Mouse Tiler to move your windows into position, and restore them next time you start the application. Ultimate combo. (Originally Remember Window Positions was meant to be part of the Mouse Tiler).

## <p id="support"></p>Support the project

MouseTiler for Plasma 5 is a port of the [upstream project](https://github.com/rxappdev/MouseTiler) by [@rxappdev](https://github.com/rxappdev). Consider [sponsoring the original author](https://github.com/rxappdev/MouseTiler) if you find the tool useful.

## <p id="getintouch"></p>Get in touch ##

For issues related to this Plasma 5 port, open an issue on the [GitHub repository](https://github.com/mlynar-czyk/MouseTiler).