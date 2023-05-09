# i3-supersize

![](https://github.com/moodboom/i3/raw/gaps-next-moodboom/docs/i3-supersize.gif)

## What is i3-supersize?

i3-supersize is a fork of [i3-gaps](https://github.com/Airblader/i3), which is a fork of [i3wm](https://www.i3wm.org), a tiling window manager for X11.

i3-supersize only has one feature added to its excellent upstream projects.  But for my use case, it is an essential feature addressing fatal flaws in i3's window management.  In my optimized workflow on a 4K monitor, I dynamically resize my tiled windows constantly, via keyboard, and need any window to grow and shrink without arbitrary constraints, except to stop shrinkage at a minimum useable width and minimum useable height.

A short video provides the simplest explanation.  See GIF above, or [download this hirez example](https://github.com/moodboom/i3/raw/gaps-next-moodboom/docs/i3-supersize.mp4).  Current i3/i3-gaps will fail miserably trying to do this, hitting arbitrary/buggy sub-container size constraints.

## How do I install, configure, etc.?

Install using the **gaps-next-moodboom** branch.

Please refer to the [i3-gaps](https://github.com/Airblader/i3) project for excellent documentation, including detailed [installation instructions](https://github.com/Airblader/i3/wiki/installation).

# History

I maintain this fork because I was unable to convince the authors to merge my changes.  The changes are minor, and I should be able to pull upstream changes on a regular basis.
