---
description: A tool helpful for debugging mods
---

# Dev Tools

## **Disclaimer**

This guide assumes that you are already familiar with OMORI mod development, and that you know where some files need to go. You should also already know [how to fix your OMORI installation](resetting-installation.md), in case you break it.

Furthermore, [some mods might not work in SDK mode.](#user-content-fn-1)[^1]

## **Installation**

To get [dev tools](https://flaviocopes.com/browser-dev-tools) in OMORI, which can be very helpful in debugging your mod, you need to do a few steps:

1. Download the SDK edition of the exact same NW.js version that OMORI is using&#x20;
   * For OMORI v1.0.8 - [nwjs-sdk-v0.29.0-win-x64.zip](https://dl.nwjs.io/v0.29.0)
2. Drag all your files into the OMORI folder and choose replace / overwrite
3.  Add this code to _www/js/main.js_ to disable SDK mode protection:

    ```javascript
    window.navigator.plugins.namedItem = function() {
        return null;
    }
    ```
4. Rename OMORI.exe to something else, like OMORI\_old.exe, and rename the new file nw.exe to OMORI.exe
5. Launch the game and press _F12_ to open the dev tools.

[^1]: _For example,_ [_Painful Bossrush_](https://mods.one/mod/painrush) _will check for SDK mode and stop working if detected._
