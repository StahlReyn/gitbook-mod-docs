---
description: About files found in the www_decrypt/data/ subfolder.
---

# Data Files

**Disclaimer:** This is a very early-stage list. Files may contain more important data than mentioned here, so you're more than welcome to contribute details via the [mods.one Discord](https://discord.gg/Rxr5QfQnFd).

This page documents useful information about [decrypted](https://omori.wiki.mods.one/modding:getting_started#decrypting_the_game) files found in the **www\_decrypt/data/** subfolder. More info can be found [here](./).

#### Actors.json <a href="#actorsjson" id="actorsjson"></a>

Seems to store information on your team (Omori, Kel, Aubrey, Hero), which items they carry (initially), what level they have, and more.

#### Animations.json <a href="#animationsjson" id="animationsjson"></a>

Animation data for the individual sprites being rendered. Might best be edited by using RPG Maker instead of manually.

#### Armors.json <a href="#armorsjson" id="armorsjson"></a>

_<mark style="color:orange;">Important for Translation</mark>_

Charms/equipment descriptions, sprites, and properties.

#### Atlas.yaml <a href="#atlasyaml" id="atlasyaml"></a>

_TBA_

#### Classes.json <a href="#classesjson" id="classesjson"></a>

_TBA_

#### CommonEvents.json <a href="#commoneventsjson" id="commoneventsjson"></a>

Data for many different events (basically any action you can do). Seems to be on maps only (not in combat).

**Examples:** Opening Blackspace doors, horror effects (screen glitches), waking up animation, looking at photos, Kel throwing…

#### Enemies.json <a href="#enemiesjson" id="enemiesjson"></a>

_<mark style="color:orange;">Important for Translation</mark>_

Enemy names, sprites, and properties.

#### Items.json <a href="#itemsjson" id="itemsjson"></a>

_<mark style="color:orange;">Important for Translation</mark>_

Item names, descriptions, sprites, and properties.

#### MapXXX.json <a href="#mapxxxjson" id="mapxxxjson"></a>

_<mark style="color:orange;">Important for Translation</mark>_

Map files describe all places and rooms in OMORI. _displayName_: This field will be used when creating or overwriting a save file. _todo, there's a LOT more about these files_ For anything that goes beyond small modifications, you definitely want to use RPG Maker: [Mapping in OMORI using RPG Maker.](https://omori.wiki.mods.one/modding:mapping)

#### MapInfos.json <a href="#mapinfosjson" id="mapinfosjson"></a>

TBA

#### Notes.yaml <a href="#notesyaml" id="notesyaml"></a>

TBA

#### Quests.yaml <a href="#questsyaml" id="questsyaml"></a>

TBA

#### Skills.json <a href="#skillsjson" id="skillsjson"></a>

_<mark style="color:orange;">Important for Translation</mark>_

Skill names, descriptions, sprites, and properties.

#### States.json <a href="#statesjson" id="statesjson"></a>

_<mark style="color:orange;">Important for Translation</mark>_

State change names (emotions, dying, resurrection etc.), descriptions, and properties.

**Examples:** “X became TOAST!”, “X feels ECSTATIC!”, “X's SPEED fell!”

#### System.json <a href="#systemjson" id="systemjson"></a>

TBA

#### Tilesets.json <a href="#tilesetsjson" id="tilesetsjson"></a>

TBA

#### Troops.json <a href="#troopsjson" id="troopsjson"></a>

Enemy data. HP among other things.

#### Weapons.json <a href="#weaponsjson" id="weaponsjson"></a>

_<mark style="color:orange;">Important for Translation</mark>_

Weapon names, descriptions, and other properties.

#### Conflicted copies <a href="#conflicted_copies" id="conflicted_copies"></a>

Typically named _\[…] OMORI Dev's conflicted copy \[…].json_

These files are most likely unused and left there by accident.

{% hint style="info" %}
In later versions of OMORI, these file are removed since then. This might be important to old mods when using Bundletool to detect changes.
{% endhint %}
