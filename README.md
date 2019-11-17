# VDX-SOCD-cleaner
Git patch for [Nefarius's VDX](https://github.com/ViGEm/VDX) that cleans Simultaneous Opposite Cardinal Directions, hitbox-style.

## A what for what?
VDX is a program that grabs XInput controllers and creates new XInput controllers via ViGEm - it's meant to be a sort of test of the gamepad emulation framework.

This patch will clean the XInput controller's inputs so that simultaneous opposite cardinal directions (that means, pressing back and forward or up and down at the same time) will be cleaned in the same way a hitbox would do it. This means:

U+D = U
B+F = N

## How to use
[Clone VDX](https://github.com/ViGEm/VDX.git) and apply this patch over it (git apply socd_cleaner.patch). Build VDX and there you go, your new controller's inputs will now be clean.