---
title: Custom Fonts
layout: default
parent: Themes
nav_order: 3
has_toc: false
---

# Installing the font conversion script
For themes on muOS, you can implement custom fonts! To do this, you must first install the script that will convert your
`.ttf`, `.otf`, or `.woff` type font into a specific `.bin` file that muOS will accept. 

- You will first need node.js installed. Install a pre-built packaged version of this [here](https://nodejs.org/en/download/prebuilt-installer).
- Next, open up cmd (Windows) / Command Line (Linux) / Terminal (macOS), and paste this line of code to install the script;

`npm i lv_font_conv -g`

> For macOS users, you may need to run this command as an admin. Instead, type `sudo` and then paste the code to install this.
> You may need to type in your computer's admin password.

# Using the script
Paste this line of code, replacing the `example.ttf` with your font (by dragging and dropping it into your terminal window,
or pasting the file path), and you can convert your font to the right format.

`lv_font_conv --bpp 4 --size 20 --font "example.ttf" -r 0x20-0x7F --format bin --no-compress --no-prefilter -o ./bin`

This will typically place your font in your current user directory.
- Feel free to adjust the size value. 20 is a good size for most of the elements on screen.
- Where it states `0x20-0x7f` is the range of symbols in the font.
  - 0x7f is the standard range
  - 0xff is the extended range. Some fonts may fail to convert with the extended range, but try extended range first!
- bpp is used for smoothness.  4 is a good value for most fonts. You can change this to either 1, 2, 4, or 8.
Copy the compiled font into a folder called font once done!

# Install Custom Fonts
Within the `./font/` folder, you can drop in a compiled font here either named `default.bin` or `mux_example.bin` according
to whichever program you'd like that individual font to be used for. Check out the naming conventions in the Theme Structure page.