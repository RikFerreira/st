
# Rik’s build of simple terminal (st)

<img src="images/st.svg" style="display: block; margin: auto;" />

## Overview

Simple terminal (st) is part of suckless tools for desktop. It aims to
be simple, extendable and lightweight, and this build is designed to
integrate my workflow.

## Features

-   Supports transparency (needs xcompgr or other compositor for X).
-   Supports ligatures.
-   Gapless drawings.
-   Customizable via `.Xresources`. Default theme is gruvbox.
-   Standalone scrollback terminal session history (up to
    1 ⋅ 10<sup>5</sup> lines).
-   Interacts with external scripts.
-   Usual behavior of `DEL` key.

## Hotkeys

-   `Alt+y`: Copy.
-   `Alt+p`: Paste.
-   `Alt+k`: Scroll up.
-   `Alt+j`: Scroll down.
-   `Alt+Shift+k`: Zoom in.
-   `Alt+Shift+j`: Zoom out.
-   `Alt+Shift+r`: Zoom reset.
-   `Alt+l`: Copy link.
-   `Alt+Shift+l`: Follow link.
-   `Alt+o`: Copy output.
-   `Alt+x`: Invert colorscheme.

## How to install

``` bash
git clone https://github.com/rikferreira/st.git
cd st
sudo make clean install
```

### Dependencies

These headers may appear in errors while trying to compile dwm:

``` c
#include <X11/Xlib.h>
#include <X11/Xft/Xft.h>
#include <X11/extensions/Xinerama.h>
```

The icons in the tag bar are from the `font-awesome` package.

#### Arch

``` bash
sudo pacman -S libx11 libxft libxinerama ttf-font-awesome
```

#### Debian

``` bash
sudo apt install libx11-dev libxft-dev libxinerama-dev fonts-font-awesome
```

Notice that are some bindings to scripts that aren’t in this repository.
You may want to remove those because they will look in your `$PATH` for
an executable with their names and it may not work as expected. I
reinforce that this is my personal build to this software and it is
designed to work with other elements of my desktop.
