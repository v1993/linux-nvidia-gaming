## Configuring compositor under KDE

KDE is highly configurable, including its compositor. Here, parts useful for performance improvements will be discussed.

### Disable compositor for some apps

There is a way to automatically disable compositor for some applications. For more on this, read [Window Rules](kde/windowrules.md).

### Compositor toggle hotkey

To quickly turn compositor off and on, use `Alt+Shift+F12` (adjust if you have Fn key accordingly). It is extremely useful as a quick shortcut for testing and when window rules don't work out nicely for some application.

### Tweaking compositor

To configure compositor, open `System Settings -> Hardware -> Display and Monitor -> Compositor` (or just search for compositor in main menu).

In some situations, compositor might get turned off. If this happens, visit this place again and click "Re-enable OpenGL detection" in additional section that will pop up. Afterwards, use compositor toggle hotkey twice to get compositor running again.

Below, options and their recommended values are outlined.

#### Enable compositor on startup - on

You probably want to have compositor turned on as it is by default most of the time, while switching it off only during some tasks by using methods outlined above.

In theory, you can disable compositor permanently if you're ok missing some neat graphical effects (and potentially having tearing issues, but not if you follow this guide for Nvidia).

#### Scale method - Accurate

I don't think this one needs much of discussion.

#### Rendering Backend - OpenGL 3.1

Any gaming (and many non-gaming) machines support OpenGL 3.1, which is optimal when it comes to performance of compositing.

#### Tearing Prevention ("vsync") - depends on driver

If you follow the NVidia part of this guide, this setting can be safely set to "never". Otherwise, use "Automatic" or do the research yourself.

#### Keep window thumbnails - whatever you prefer

Doesn't seem to considerably affect performane in any way.

#### Allow applications to block compositing - whatever you prefer

I personally prefer to keep this turned off and manually override setting for windows when required, but your preference may differ.
