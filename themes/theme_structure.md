---
title: Theme Structure
layout: default
parent: Themes
nav_order: 1
has_toc: false
---

# Theme Folder Structure
For a theme to function as intended, you will need to use the proper folder structure containing all your files in the correct
place. Below is an example of the correct structure that you can replicate if you are creating/editing a theme.

```
.
├── credits.txt
├── font
│   └── default.bin
│   ├── header
|   │   └── default.bin
│   ├── footer
|   │   └── default.bin
│   ├── panel
|   │   └── default.bin
├── glyph
│   ├── muxlaunch
│   |   ├── explore.png
│   |   ├── favourite.png
│   |   ├── history.png
│   |   ├── apps.png
│   |   ├── info.png
│   |   ├── config.png
│   |   ├── reboot.png
│   |   ├── shutdown.png
├── image
│   ├── bootlogo.bmp
│   ├── overlay.png
│   ├── static
│   |   ├── muxlaunch
│   |   |   ├── explore.png
│   |   |   ├── favourite.png
│   |   |   ├── history.png
│   |   |   ├── apps.png
│   |   |   ├── info.png
│   |   |   ├── config.png
│   |   |   ├── reboot.png
│   |   |   └── shutdown.png
│   |   └── muxinfo.png
│   └── wall
│       ├── default.png
│       ├── muxtester.png
│       └── muxcharge.png
├── scheme
│   ├── default.txt
│   └── muxtester.txt
├── music
└── sound  
```
In the above example, there are some files here that are not necessary to have a *working* theme - however the elements included
above show off the amount of possible customisation available.
- **font** - Here is where you can place custom fonts compiled into a `.bin` format.  Fonts placed in the panel subfolder will override the font used for list items.  Fonts placed in the header subfolder will override the font used for the header.  Fonts placed in the footer subfolder will override the font used for the footer.
- **glyph** - Place png images for list item glyphs.  See [Theme Folder Structure Glyphs](#theme-folder-structure-glyphs) section for full list of names.
- **image** - Place all image assets of your theme here. Animated images are also supported (use `.gif`).
  - **static** - Images can be set to sit on top of other elements. They are named following their associated program.
  - **wall** - All backgrounds used sit here. Anything named `default.xxx` is applied on all programs without dedicated assets.
- **scheme** - The brain of the theme. This file will tell your device how windows and text should appear per program, and will also
               tell your device how to use the files you have dropped into your image folder.
- **music** + **sound** - These folders will contain files heard during your time in the muOS menus. Yet to be implemented.
  
# Theme Folder Structure Glyphs
The following images are used for populating the glyphs displayed in the headers, footers, and list items. 
<br><br>**Note:** If your theme does not supply images for the glyphs below then it will fall back to built in default images.  If you want to hide glyphs you will need to adjust the appropriate settings in your scheme file.  For example disable list item glyphs you would set these settings in your scheme file:
```
[list]
LIST_DEFAULT_GLYPH_ALPHA=0
LIST_FOCUS_GLYPH_ALPHA=0
```
```
.
├── credits.txt
├── font
├── glyph
│   ├── footer
│   |   ├── a.png
│   |   ├── b.png
│   |   ├── c.png
│   |   ├── menu.png
│   |   ├── x.png
│   |   ├── y.png
│   |   ├── z.png
│   ├── header
│   |   ├── bluetooth.png
│   |   ├── capacity_0.png
│   |   ├── capacity_10.png
│   |   ├── capacity_20.png
│   |   ├── capacity_30.png
│   |   ├── capacity_40.png
│   |   ├── capacity_50.png
│   |   ├── capacity_60.png
│   |   ├── capacity_70.png
│   |   ├── capacity_80.png
│   |   ├── capacity_90.png
│   |   ├── capacity_100.png
│   |   ├── capacity_charging_0.png
│   |   ├── capacity_charging_10.png
│   |   ├── capacity_charging_20.png
│   |   ├── capacity_charging_30.png
│   |   ├── capacity_charging_40.png
│   |   ├── capacity_charging_50.png
│   |   ├── capacity_charging_60.png
│   |   ├── capacity_charging_70.png
│   |   ├── capacity_charging_80.png
│   |   ├── capacity_charging_90.png
│   |   ├── capacity_charging_100.png
│   |   ├── network_active.png
│   |   ├── network_normal.png
│   ├── muxapp
│   |   ├── app.png
│   |   ├── archive.png
│   |   ├── dingux.png
│   |   ├── flip.png
│   |   ├── moonlight.png
│   |   ├── music.png
│   |   ├── portmaster.png
│   |   ├── ppsspp.png
│   |   ├── retroarch.png
│   |   ├── rgbcontroller.png
│   |   ├── task.png
│   |   ├── terminal.png
│   ├── muxarchive
│   |   ├── archive.png
│   |   ├── installed.png
│   ├── muxassign
│   |   ├── core.png
│   |   ├── default.png
│   |   ├── system.png
│   ├── muxconfig
│   |   ├── clock.png
│   |   ├── general.png
│   |   ├── language.png
│   |   ├── network.png
│   |   ├── service.png
│   |   ├── theme.png
│   ├── muxgov
│   |   ├── default.png
│   |   ├── governor.png
│   ├── muxinfo
│   |   ├── credit.png
│   |   ├── system.png
│   |   ├── tester.png
│   |   ├── tracker.png
│   ├── muxlanguage
│   |   ├── language.png
│   ├── muxlaunch
│   |   ├── apps.png
│   |   ├── config.png
│   |   ├── explore.png
│   |   ├── favourite.png
│   |   ├── history.png
│   |   ├── info.png
│   |   ├── reboot.png
│   |   ├── shutdown.png
│   ├── muxnetprofile
│   |   ├── profile.png
│   ├── muxnetscan
│   |   ├── netscan.png
│   ├── muxnetwork
│   |   ├── address.png
│   |   ├── connect.png
│   |   ├── dns.png
│   |   ├── enable.png
│   |   ├── gateway.png
│   |   ├── identifier.png
│   |   ├── password.png
│   |   ├── status.png
│   |   ├── subnet.png
│   |   ├── type.png
│   ├── muxoption
│   |   ├── core.png
│   |   ├── governor.png
│   ├── muxplore
│   |   ├── favourite.png
│   |   ├── folder.png
│   |   ├── history.png
│   |   ├── rom.png
│   ├── muxfavourite
│   |   ├── favourite.png
│   ├── muxhistory
│   |   ├── favourite.png
│   |   ├── history.png
│   ├── muxrtc
│   |   ├── day.png
│   |   ├── hour.png
│   |   ├── minute.png
│   |   ├── month.png
│   |   ├── notation.png
│   |   ├── timezone.png
│   |   ├── year.png
│   ├── muxstorage
│   |   ├── bios.png
│   |   ├── catalogue.png
│   |   ├── config.png
│   |   ├── content.png
│   |   ├── language.png
│   |   ├── music.png
│   |   ├── network.png
│   |   ├── save.png
│   |   ├── screenshot.png
│   |   ├── theme.png
│   ├── muxsysinfo
│   |   ├── capacity.png
│   |   ├── cpu.png
│   |   ├── device.png
│   |   ├── governor.png
│   |   ├── kernel.png
│   |   ├── memory.png
│   |   ├── service.png
│   |   ├── speed.png
│   |   ├── temp.png
│   |   ├── uptime.png
│   |   ├── version.png
│   |   ├── voltage.png
│   ├── muxtask
│   |   ├── backup.png
│   |   ├── clear.png
│   |   ├── ethernet.png
│   |   ├── junk.png
│   |   ├── network.png
│   |   ├── retroarch.png
│   |   ├── sdcard.png
│   ├── muxtheme
│   |   ├── theme.png
│   ├── muxtimezone
│   |   ├── timezone.png
│   ├── muxtweakadv
│   |   ├── accelerate.png
│   |   ├── brightness.png
│   |   ├── font.png
│   |   ├── led.png
│   |   ├── lock.png
│   |   ├── offset.png
│   |   ├── retrowait.png
│   |   ├── state.png
│   |   ├── storage.png
│   |   ├── swap.png
│   |   ├── theme.png
│   |   ├── thermal.png
│   |   ├── usbfunction.png
│   |   ├── verbose.png
│   |   ├── volume.png
│   ├── muxtweakgen
│   |   ├── advanced.png
│   |   ├── battery.png
│   |   ├── bgm.png
│   |   ├── brightness.png
│   |   ├── colour.png
│   |   ├── hdmi.png
│   |   ├── hidden.png
│   |   ├── interface.png
│   |   ├── shutdown.png
│   |   ├── sound.png
│   |   ├── startup.png
│   ├── muxvisual
│   |   ├── backgroundanimation.png
│   |   ├── battery.png
│   |   ├── bluetooth.png
│   |   ├── boxart.png
│   |   ├── clock.png
│   |   ├── counterfile.png
│   |   ├── counterfolder.png
│   |   ├── dash.png
│   |   ├── folderitemcount.png
│   |   ├── friendlyfolder.png
│   |   ├── name.png
│   |   ├── network.png
│   |   ├── thetitleformat.png
│   ├── muxwebserv
│   |   ├── browser.png
│   |   ├── ntp.png
│   |   ├── resilio.png
│   |   ├── shell.png
│   |   ├── sync.png
│   |   ├── terminal.png
├── image
├── scheme
├── music
└── sound
```

# Program Names
muOS has numerous programs, so they are individually named so that you Themers can set different properties for every single page if
you so wish to do so!
Anything named ```default.xxx``` in the above folder structure can be renamed to  ```mux...``` to apply ideas to single pages.

You can also set images to appear for individual list items (see the files above under `./image/static/muxlaunch/`. 
> *Caution - as muOS is a constantly updating system, there is a high chance that in time, list items will be added or removed
from sections. Be wary of this when creating graphics that show all the options for a program.*

Check out the updated naming conventions of all muxprograms below;

| Program Name | Function | List Item Names |
|:--:|:--|:--|
|muxcharge|Charging Screen|-|
|muxlaunch|Main Menu|explore / favourite / history / apps / info / config / reboot / shutdown|
|muxplore|Content Explore Page|*Use `/MUOS/catalogue` outside of themes to create list item wallpapers.*|
|muxassign|Shows when assigning a core to a folder.|-|
|muxfavourite|Favourites page|-|
|muxhistory|History page|-|
|muxapp|Dynamic applications page|*List item wallpapers named directly after application names. Default example here;* <br>Archive Manager / Dingux Commander / GMU Music Player / Moonlight / PortMaster / RetroArch / Simple Terminal / Task Toolkit|
|muxarchive|Archive Manager page|-|
|muxtask|Task toolkit page|-|
|muxinfo|Information page|tester / system / credit|
|muxtester|Input Tester|-|
|muxsysinfo|System details|version / kernel / uptime / cpu / speed / governor / memory / temp / service / capacity / voltage|
|muxconfig|Configuration page|general / theme / network / service / clock / device|
|muxtweakgen|General Settings|hidden / bgm / sound / startup / colour / brightness / hdmi / shutdown / battery / sleep / interface / storage / advanced|
|muxvisual|Interface Options (within General Settings)| battery / network / bluetooth / mux_clock / boxart / name / dash / counterfolder / counterfile|
|muxtweakadv|Advanced (within General Settings)|swap / thermal / font / volume / brightness / offset / lock / led / theme / retrowait / android / state / verbose
|muxtheme|Theme Picker page|-|
|muxnetwork|Wi-Fi Network Page|enable / identifier / password / type / address / subnet / gateway / DNS / status / connect|
|muxnetprofile|Network Profiles (within Wi-FI).|-|
|muxnetscan|Shows when scanning for networks.|-|
|muxwebserv|Web Services page|shell / browser / terminal / sync / ntp|
|muxrtc|Date and Time page|year / month / day / hour / minute / notation / timezone|
|muxtimezone|Timezone Selection|-|
|muxdevice|Device type page (will differ for muOS on RG28XX)|rg35xx-h / rg35xx-plus / rg35xx-sp / rg35xx-2024|
|muxpass|Passcode Lock Screen|-|
|muxstorage|Storage Preferences|bios / config / catalogue / fav / music / save / screenshot / theme|
