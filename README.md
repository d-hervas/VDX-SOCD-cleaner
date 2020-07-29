# W A R N I N G
- The latest version includes custom bindings for my hitbox - it won't work if you're trying to clean a normal XInput device (I mean, it will work, but your controls will be all messed up). *DELETE THE PARAGRAPH UNDER "CUSTOM HITBOX FUCKERY" IF YOU WANT THIS TO WORK FOR YOU*. Open an issue if you have any problems.

- VDX works in a different way now (the mappings are done in the header file). I've only re-mapped it for *PS4 EMULATION*. *CHOOSE DUALSHOCK 4 CONTROLLER, ELSE IT WON'T WORK*.

# VDX-SOCD-cleaner
Git patch for [Nefarius's VDX](https://github.com/ViGEm/VDX) that cleans Simultaneous Opposite Cardinal Directions, hitbox-style.

## A what for what?
VDX is a program that grabs XInput controllers and creates new XInput controllers via ViGEm - it's meant to be a sort of test of the gamepad emulation framework.

This patch will clean the XInput controller's inputs so that simultaneous opposite cardinal directions (that means, pressing back and forward or up and down at the same time) will be cleaned in the same way a hitbox would do it. This means:

U+D = U
B+F = N

## How to use
[Clone VDX](https://github.com/ViGEm/VDX.git) and apply this patch over it (git apply socd_cleaner.patch). Build VDX and there you go, your new controller's inputs will now be clean.
