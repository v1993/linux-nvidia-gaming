# XConfig: cheap VSync for everyone

This section of guide describes a simple way to enable VSync system-wide. This is the only way to do so for some games, while others still benefit in form of icreased performance while still preventing tearing.

To begin, open NVIDIA X Server Settings (`nvidia-settings` if launched from terminal) and go to X Server Display Configuration tab.

Here, click on "Advanced..." button to reveal extra settings. Now, for each display you have (you probably have one, but who knows?) tick "Force Full Composition Pipeline". This essentially acts as a driver-driven (sorry) VSync, being very cheap compared to all other solutions.

If you have few displays and dislike layout for some reason, rearrange windows before proceeding (I won't describe it here, it's quite intuitive).

Now, click "Save to X Configuration File", enter `/etc/X11/xorg.conf` as path (if it isn't such already) and click "Save". You'll be prompted to enter your password to write config file, which you should do. Congratulations, you now have cheap VSync everywhere! You can go to OpenGL Settings tab and disable "Sync to VBlank" and then close NVIDIA configurator.

If using KDE, it's also time to disable its own VSync as outlined in [Configuring compositor](kde/compositor.md) article.

## Optional: enable overclocking and fan control

If you don't intend to overclock, you can skip this section. Or not. It won't hurt to have this enabled. Should you choose to skip it, don't forget to reboot anyways!

Now, it's time for some fine tuning. Open `/etc/X11/xorg.conf` in your favorite text editor (probably as root, unless you're using KDE's Kate) and find `Device` section. It should look like this:

```
Section "Device"
    Identifier     "Device0"
    Driver         "nvidia"
    VendorName     "NVIDIA Corporation"
    BoardName      "GeForce GTX 960"
EndSection
```

Add a single line

```
    Option "Coolbits" "28"
```

right before `EndSection` (they should be on separate lines, of course) and save file. Now reboot.
