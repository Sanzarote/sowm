# sowm (*~~Simple~~ Shitty Opinionated Window Manager*)

<a href="https://raw.githubusercontent.com/Sanzarote/dotfiles/master/scr/sea.png"><img src="https://raw.githubusercontent.com/Sanzarote/dotfiles/master/scr/sea.png" width="43%" align="right"></a>

An itsy bitsy floating window manager (*220~ sloc!*).

- Floating only.
- Fullscreen toggle.
- Window centering.
- Mix of mouse and keyboard workflow.
- Focus with cursor.
- Rounded corners (*[through patch](https://github.com/dylanaraps/sowm/pull/58)*)
- Titlebars (*[through patch](https://github.com/dylanaraps/sowm/pull/57)*)

<a href="https://raw.githubusercontent.com/Sanzarote/dotfiles/master/scr/1337.png"><img src="https://raw.githubusercontent.com/Sanzarote/dotfiles/master/scr/1337.png" width="43%" align="right"></a>

- Alt-Tab window focusing.
- All windows die on exit.
- No window borders.
- [No ICCCM](https://web.archive.org/web/20190617214524/https://raw.githubusercontent.com/kfish/xsel/1a1c5edf0dc129055f7764c666da2dd468df6016/rant.txt).
- No EWMH.
- etc etc etc


<br>

Patches available here: https://github.com/dylanaraps/sowm/pulls

## Default Keybindings

**Window Management**

| combo                      | action                 |
| -------------------------- | -----------------------|
| `Mouse`                    | focus under cursor     |
| `MOD4` + `Left Mouse`      | move window            |
| `MOD4` + `Right Mouse`     | resize window          |
| `MOD4` + `f`               | maximize toggle        |
| `MOD4` + `c`               | center window          |
| `MOD4` + `q`               | kill window            |
| `MOD4` + `1-9`             | desktop swap           |
| `MOD4` + `Shift` +`1-9`    | send window to desktop |
| `MOD1` + `TAB` (*alt-tab*) | focus cycle            |

**Programs**

| combo                    | action           | program        |
| ------------------------ | ---------------- | -------------- |
| `MOD4` + `Return`        | terminal         | `st`           |
| `MOD4` + `d`             | dmenu            | `dmenu_run`    |
| `MOD4` + `p`             | scrot            | `scrot`        |
| `XF86_AudioLowerVolume`  | volume down      | `pamixer`      |
| `XF86_AudioRaiseVolume`  | volume up        | `pamixer`      |
| `XF86_AudioMute`         | volume toggle    | `pamixer`      |
| `XF86_MonBrightnessUp`   | brightness up    | `xbacklight`   |
| `XF86_MonBrightnessDown` | brightness down  | `xbacklight`   |


## Dependencies

- `xlib` (*usually `libX11`*).


## Installation

1) Copy `config.def.h` to `config.h` and modify it to suit your needs.
2) Run `make` to build `sowm`.
3) Copy it to your path or run `make install`.
    - `DESTDIR` and `PREFIX` are supported.
4) (Optional) Apply patch with `git apply patches/patch-name`
    - In case of applying multiple patches, it has to be done **manually**.

If you are using GDM, save the following to `/usr/share/xsessions/sowm.desktop`. It is still recommended to start `sowm` from `.xinitrc` or through
[your own xinit implementation](https://github.com/dylanaraps/bin/blob/dfd9a9ff4555efb1cc966f8473339f37d13698ba/x).

```
[Desktop Entry]
Name=sowm
Comment=This session runs sowm as desktop manager
Exec=sowm
Type=Application
```


## Thanks

- [2bwm](https://github.com/venam/2bwm)
- [SmallWM](https://github.com/adamnew123456/SmallWM)
- [berry](https://github.com/JLErvin/berry)
- [catwm](https://github.com/pyknite/catwm)
- [dminiwm](https://github.com/moetunes/dminiwm)
- [dwm](https://dwm.suckless.org)
- [monsterwm](https://github.com/c00kiemon5ter/monsterwm)
- [openbox](https://github.com/danakj/openbox)
- [possum-wm](https://github.com/duckinator/possum-wm)
- [swm](https://github.com/dcat/swm)
- [tinywm](http://incise.org/tinywm.html)
https://raw.githubusercontent.com/Sanzarote/dotfiles/master/scr/1337.png
