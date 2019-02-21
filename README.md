# XRootGIF [![xrootgif](https://img.shields.io/aur/version/xrootgif.svg)](https://aur.archlinux.org/packages/xrootgif/)
A simple program to display GIFs as X root, targeting performance

# Usage
``` text
Usage: ./xrootgif d:S:s:apt:Th [image]
  -d | --display [display]
       X-Display to use (:0), if none, use default display
  -S | --screen [num]
       X-Screen to use, if none, use default screen
  -s | --speed [float]
       Playback speed as float
  -a | --anti-alias
       Use anti-aliasing
  -p | --performance
       Performance mode - scale framerate to 5 (default)
  -t | --target-fps [float]
       In performance mode, set target framerate
  -T | --test-pattern
       A little test pattern used for developing
  -h | --help

```

# Performance
This Program grew out of the pain, that most GIF-Viewer consume quiet
some CPU time, so having a GIF as wallpaper somewhat drained the battery.
XRootGIF tries to minimize CPU time used to display fancy GIFs,
by pre rendering all frames and allocating them in the X-Display instance.
Some GIFs may still make your PC heat your room, but this can be
avoided by using the performance mode, which will simply downscale
the framerate.

# Planned features

- multi screen
- more image fitting modes
- configuration files
- daemon mode
- other animation formats (webm, apng, ...)

# Building
The following libraries are used by XRootGIF:

- libx11
- giflib
- imlib2

Tools:

- gcc
- make

To compile, simply run

``` sh
make
```

