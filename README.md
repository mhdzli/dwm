# mz-dwm
## My fork of dwm

Included [patches](https://github.com/mhdzli/dwm/tree/master/patches):

+ [actualfullscreen](https://dwm.suckless.org/patches/actualfullscreen/)
+ [alpha](https://dwm.suckless.org/patches/alpha/)
+ [alternativetags](https://dwm.suckless.org/patches/alternativetags/)
+ [barpadding](https://dwm.suckless.org/patches/barpadding/)
+ [centeredmaster](https://dwm.suckless.org/patches/centeredmaster/)
+ [dwmc](https://dwm.suckless.org/patches/dwmc/)
+ [fullgaps](https://dwm.suckless.org/patches/fullgaps/)
+ [pertag](https://dwm.suckless.org/patches/pertag/)
+ [savefloats](https://dwm.suckless.org/patches/save_floats/)
+ [scratchpad](https://dwm.suckless.org/patches/scratchpad/)
+ [sticky](https://dwm.suckless.org/patches/sticky/)
+ [xrdb](https://dwm.suckless.org/patches/xrdb/)

## Key bindings:

You can find them in `config.h` but they are mostly similar to may `swaywm` bindings in my dotfiles (You can find a help at the end of `sway config` file).

## Install `libxft-bgra`

Due to a feature in dwm which can not handle color emojis there was a temporary solution (an unofficial patch that I used to add to dwm.c):

+ [ignoreXfterrorswhendrawingtext](https://github.com/mhdzli/dwm/blob/master/patches/ignoreXfterrorswhendrawingtext.diff)

You can read more about this issue in [here](https://groups.google.com/forum/#!topic/wmii/7bncCahYIww).

`FcBool iscol` function was added to drw.c to prevent this issue. So I removed the `ignoreXfterrorswhendrawingtext` from this source.

Since there is a new patch for `libxft` and an [Aur package](https://aur.archlinux.org/packages/libxft-bgra/) for handling color emojis this build of dwm does non block color emojis anymore so you must install [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra/) witch fixes the libxft color emoji rendering, otherwise dwm will crash while trying to render one.

Watch a brief [screencast](https://open.lbry.com/@mzeinali:c/dwm:7)

Example screenshot:

![https://github.com/mhdzli/dwm/blob/master/patches/dwm-01.png](https://github.com/mhdzli/dwm/blob/master/patches/dwm-01.png)
![https://github.com/mhdzli/dwm/blob/master/patches/dwm-02.png](https://github.com/mhdzli/dwm/blob/master/patches/dwm-02.png)
![https://github.com/mhdzli/dwm/blob/master/patches/dwm-03.png](https://github.com/mhdzli/dwm/blob/master/patches/dwm-03.png)

 
