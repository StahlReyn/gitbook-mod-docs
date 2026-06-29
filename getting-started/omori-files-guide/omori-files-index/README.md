---
description: List of top-level directories and files in the OMORI game directory
---

# Omori Files Index

This page lists the top-level directories and files in the OMORI game directory, which is usually `C:\Program Files (x86)\Steam\steamapps\common\OMORI` if you installed OMORI on your `C:` drive with Steam.

Useful page when working with OMORI files:

{% content-ref url="../common-file-types.md" %}
[common-file-types.md](../common-file-types.md)
{% endcontent-ref %}

### data/ <a href="#data" id="data"></a>

This is a directory with encrypted files that's 100% identical with _www/data_. The reason for this clone is not known, but you can probably ignore it.

{% content-ref url="data-files.md" %}
[data-files.md](data-files.md)
{% endcontent-ref %}

### locales/ <a href="#locales" id="locales"></a>

Seems to contain language data for the NW.js runtime. This is different from the language data or dialogue used by the game running inside NW.js, so you can definitely ignore these.

### pnacl/ <a href="#pnacl" id="pnacl"></a>

_todo_

### swiftshader/ <a href="#swiftshader" id="swiftshader"></a>

_todo_

### tools/ <a href="#tools" id="tools"></a>

_todo_

### www/ <a href="#www" id="www"></a>

Directory with mostly encrypted game assets.\
To inspect and modify these files, you need to [decrypt](https://omori.wiki.mods.one/modding:getting_started#decrypting_the_game) them, which will create a directory like _www\_decrypt\_abcd1234_, which has the same structure as _www_, but with all files decrypted. We'll be referring to this directory as _www\_decrypt_ for simplicity.

### www\_decrypt/ <a href="#www_decrypt" id="www_decrypt"></a>

This directory will be created when [decrypting](https://omori.wiki.mods.one/modding:getting_started#decrypting_the_game) the game files.

#### audio/ <a href="#audio" id="audio"></a>

Contains background music, sound effects, and more.\
Contents and details: [www/audio](https://omori.wiki.mods.one/modding:www-audio)

#### data/ <a href="#data1" id="data1"></a>

_<mark style="color:orange;">Important for Translation</mark>_

Contains item, map, and event data like names, descriptions, values and more.\
Contents and details: [www/data](https://omori.wiki.mods.one/modding:www-data)

#### fonts/ <a href="#fonts" id="fonts"></a>

_<mark style="color:orange;">Important for Translation</mark>_

Contains the fonts used by the game.\
If you're making a translation mod, you might need to modify the font files to support characters that might be missing from the original font, like ä, á, ß and more.\
Contents and details: [www/fonts](https://omori.wiki.mods.one/modding:www-fonts)

#### icon/ <a href="#icon" id="icon"></a>

Contains a single _icon.png_. This file is used by _package.json_ as data for NW.js. Maybe it's the icon in the window title bar in the top left.

#### img/ <a href="#img" id="img"></a>

_<mark style="color:orange;">Important for Translation</mark>_

Contains all the sprites, background, and other graphics for the game.\
Contents and details: [www/img](https://omori.wiki.mods.one/modding:www-img)

#### js/ <a href="#js" id="js"></a>

Contains the game's code.

* libs/
  * Contains library files that the game is using. You can probably ignore these.
* plugins/
  * (T)
  * Contains all the plugins in the game, which seems to be all the code that OMORI has that's not part of core RPG Maker MV. They are less “plugins” in a conventional sense, and more like normal JavaScript files that overwrite or extend existing classes and functions.
  * For translation projects, these files contain certain UI and battle text.
  * [Info on how to work with .js files](https://omori.wiki.mods.one/modding:file-types#js_-_javascript)
  * Contents and details: [www/js/plugins](https://omori.wiki.mods.one/modding:www-js-plugins)
* main.js
  * The entrypoint for the game. You can probably ignore it.
* plugins.js
  * Plugin map generated through RPG Maker. Don't edit this file, OneLoader manages this when you develop mods.
* rpg\_\[…].js
  * RPG Maker runtime files. Don't touch these unless you know what you're doing.

#### languages/ <a href="#languages" id="languages"></a>

_<mark style="color:orange;">Important for Translation</mark>_

Contains the different languages the game natively supports. As of now (OMORI v1.0.8), there's only the normal English files, and a single file for an upcoming official Japanese translation (Omocat tweeted a long time ago about it).\
For translation projects, YAML files get patched on top of the _en_ directory by OneLoader.\
Contents and details: [www/languages/en](https://omori.wiki.mods.one/modding:www-languages-en)

#### maps/ <a href="#maps" id="maps"></a>

Seems to contain the actual map data, unlike the triggers/actions/events that [www\_decrypt/data/MapXXX.json](https://omori.wiki.mods.one/modding:www-data#mapxxxjson) files seems to contain.

#### movies/ <a href="#movies" id="movies"></a>

_<mark style="color:orange;">Important for Translation</mark>_

Video files used by the game in cutscenes.\
Contents and details: [www/movies](https://omori.wiki.mods.one/modding:www-movies)

#### save/ <a href="#save" id="save"></a>

Save data. Also contains some OneLoader data.\
Contents and details: [www/save](https://omori.wiki.mods.one/modding:www-save)

#### editor.json <a href="#editorjson" id="editorjson"></a>

_todo_

#### index.html <a href="#indexhtml" id="indexhtml"></a>

Entry point for the game. OMORI uses RPG Maker MV, which in turn uses NW.js, which uses a web browser for the graphics. This HTML file loads all the assets, core libraries, plugins, and finally the start script for the game (main.js). This file, and by extension, the game, doesn't work in a normal browser like Google Chrome out of the box, because the game is using NW.js APIs that don't exist there. There have been successful attempts at running OMORI in a normal browser which we won't go into detail about here.

#### package.json <a href="#packagejson" id="packagejson"></a>

Contains some metadata about the game and configuration for NW.js, like the window title, icon, CLI arguments, and file to load (index.html).

#### steam\_appid.txt <a href="#steam_appidtxt" id="steam_appidtxt"></a>

Contain's the game's ID on Steam. This can tell Steam which game you're playing (shown in friends list), and is also used for [DRM](https://en.wikipedia.org/wiki/Digital_rights_management) checks in other games (not in OMORI).
