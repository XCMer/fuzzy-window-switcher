# Fuzzy Window Switcher

A fuzzy window switcher for Ubuntu (GTK based, so should work in other distros too, but I haven't tested). It shows you a list of open windows and uses Python's difflib to sort them according to your input. Pressing enter opens the window at the very top.

## The initial release

The version previously in the repository had some bugs, primarily with the focusing issue and the choice of the activation shortcut. (This was still a WIP, and I wasn't aware that people have started playing around with it)

The focusing issue is fixed, and a configuration file is now used to override settings.

## Requirements

The application needs KeyBinder 3 installed, which you can install using your distro's package manager.

## Usage

After the application has started running (you can run it on startup), just press the hotkey  (`F11` by default) to show the list of applications currently open. Start typing some letters, and the most relevant window will rise to the top. Clicking `Enter` would now switch focus to that window. You can press `ESC` to cancel the operation and hide the `Fuzzy Windows` window again.

The hotkey is configurable (see the config section).

Apart from this, you can also double-click on any window to open it.

## Configuration

The default hotkey is `F11`. You can change this by creating a `.fuzzy-windows` file in your home directory. The contents would be something like:

    [Default]
    hotkey=F10

Certain windows are ignored and not shown to you, because they're common system specific ones. The default ones ignored are: 'XdndCollectionWindowImp', 'unity-launcher', 'Desktop', 'unity-panel', 'unity-dash', 'Hud', 'Guake!'

You can, however, override this as:

    [Default]
    hotkey=F10
    ignored_windows=
        unity-panel
        unity-dash

Notice that the list is newline separated.

## TODOs

Still thinking. Your suggestions are welcome. Just open a new issue here on GitHub.
