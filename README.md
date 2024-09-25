# WinJump
This is a fork of [WinJump](https://github.com/widavies/WinJump) that aims to maintain a limited set of features. The primary focus is keyboard navigation of virtual desktops.

### Features
- Configure custom keyboard shortcuts to jump directly to virtual desktops
- See what virtual desktop you're current on in the system tray
- Configure number of "sticky desktops" to create on start

### Installation
> Note, you may receive a Windows smartscreen warning when you try to run WinJump. Click "More options" and click "Run anyway"
1. [Download](https://github.com/widavies/WinJump/releases/) `WinJump.exe`.
2. Press `Win+R` and type `shell:startup`
3. Move `WinJump.exe` to the shell startup folder
4. Double click `WinJump.exe` to run it manually

### Uninstall
1. Press `Win+R` and type `shell:startup`
2. Delete `WinJump.exe`

### Configuration
WinJump can be configured via the `config.json` file located in app data roaming folder.

You can access the file for editing quickly via the system tray icon. Right click and select "open config file".

You'll find these sections:
- `jump-to` lets you define shortcuts that jump directly to a desktop
- `sticky-desktops` lets you set an amount of virtual desktops to be created when WinJump starts (10 max)

<details>
  <summary>Default Configuration</summary>

  ```json
  {
   "sticky-desktops": 4,
   "jump-to": [
    {
      "shortcut": "alt+d0",
      "desktop": 10
    },
    {
      "shortcut": "alt+d1",
      "desktop": 1
    },
    {
      "shortcut": "alt+d2",
      "desktop": 2
    },
    {
      "shortcut": "alt+d3",
      "desktop": 3
    },
    {
      "shortcut": "alt+d4",
      "desktop": 4
    },
    {
      "shortcut": "alt+d5",
      "desktop": 5
    },
    {
      "shortcut": "alt+d6",
      "desktop": 6
    },
    {
      "shortcut": "alt+d7",
      "desktop": 7
    },
    {
      "shortcut": "alt+d8",
      "desktop": 8
    },
    {
      "shortcut": "alt+d9",
      "desktop": 9
    }
  ]
}
```
</details>

### How it works
WinJump uses the reverse engineered Windows Virtual Desktop API. This means that the API often changes between Windows releases. Please see the [reverse engineering guide](https://github.com/widavies/WinJump/blob/main/WinJump/Core/VirtualDesktopDefinitions/README.md) if you're interested in contributing reverse-engineering definitions for new Windows releases.

Please make contributions to the Virtual Desktop API on the main [WinJump](https://github.com/widavies/WinJump) repo so forks like mine can easily obtain the benefits of your work.