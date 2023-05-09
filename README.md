# i3-supersize

![](https://github.com/moodboom/i3-supersize/raw/next/docs/i3-supersize.gif)

## What is i3-supersize?

i3-supersize is a fork of [i3wm](https://www.i3wm.org), a tiling window manager for X11.

i3-supersize only has one feature added to its excellent upstream project.  But for my use case, it is an essential feature addressing fatal flaws in i3's window management.  In my optimized workflow on a 4K monitor, I dynamically resize my tiled windows constantly, via keyboard, and need any window to grow and shrink without arbitrary constraints, except to stop shrinkage at a minimum useable width and minimum useable height.

A short video provides the simplest explanation.  See GIF above, or [download this hirez example](https://github.com/moodboom/i3-supersize/raw/next/docs/i3-supersize.mp4).  Current i3/i3-gaps will fail miserably trying to do this, hitting arbitrary/buggy sub-container size constraints.

## How do I install, configure, etc.?

Install using the **next** branch.  A quick Ubuntu example to get you kickstarted:

```
sudo apt install -y libxcb1-dev libxcb-keysyms1-dev libpango1.0-dev libxcb-util0-dev libxcb-icccm4-dev libyajl-dev libstartup-notification0-dev libxcb-randr0-dev libev-dev libxcb-cursor-dev libxcb-xinerama0-dev libxcb-xkb-dev libxkbcommon-dev libxkbcommon-x11-dev autoconf libxcb-xrm0 libxcb-xrm-dev automake libpango1.0-dev libyajl-dev xutils-dev
cd ~/apps
git clone https://github.com/Airblader/xcb-util-xrm
cd xcb-util-xrm
git pull
git submodule update --init
./autogen.sh --prefix=/usr
make
sudo make install
cd ..

cd ~/apps
git clone git@github.com:vivien/i3blocks.git
cd i3blocks
git pull
./autogen.sh
./configure
make
sudo make install
cd ..

git clone git@github.com:moodboom/i3-supersize.git
cd i3-supersize
git checkout next
rm -rf build/
mkdir -p build && cd build/
meson ..
ninja
i3-msg restart
```

Please refer to the [i3wm](https://www.i3wm.org) project for official documentation.

# History

I maintain this fork because I was unable to convince the authors to merge my changes.  The changes are minor, and I should be able to pull upstream changes on a regular basis.
