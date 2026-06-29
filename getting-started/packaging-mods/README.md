---
description: A guide on how to package mods
---

# Packaging Mods

_Omori mods must be in a specific folder/zip format in order to properly run._

## Using Bundletool

{% embed url="https://mods.one/mod/bt" %}
Link to BundleTool on mods.one
{% endembed %}

After editing the game's data and assets from the "www\_decrypt\_xxxxxx" or "www\_playtest\_xxxxxx" folder, you can package your mod into a zip for use by running [Bundletool](https://mods.one/mod/bt). It is installed the same way other mods are installed. After installing, run the game and follow the on-screen prompts to properly package your mod.

1. Drag Bundletool zip file to the mods folder, [like how you install mods.](../installing-mods.md)
2. Run OMORI; Click "Use BundleTool"
3. Select folder of the mod you want to package. This is likely a folder named `www_decrypt` or `www_playtest` or similar
4. Enter mod details. Mod ID should ideally align with the mod ID you are going to upload in mods.one.
5. Select the files need changing. (Tip: Pressing the top header will select all for that category)
   1. **Ignore** means don't include the file in the package. This can be used to ignore some plugins only used in testing and don't want to appear in final product. For example: console, quick save and load, or better saves.
   2. **Delta** means only includes the changes, and does not replace it. This is good for compatibility, especially if the mod only changes small amount of things and don't want to replace entire file (which would break compatibility). For example, small single changes to some Skills in `skills.json`, as you don't need to replace everything, just change only one specific thing.
   3. **Include** means add the file to the package, this totally replaces the files. This is commonly for audio and image files, as delta can potentially cause strange changes.
   4. **Unique Name** is specific to plugins. It makes it so when multiple mods has the same plugin added or changed, it will simply make two of them for each mod and will not override the file entirely. As of current it may run into some bugs so it may be better avoided. \[NEEDS CHECKING]
6. Wait for the bundle process to finish. This can take a few minutes especially for bigger mods.
7. Select the location for where the final export will be.
8. You're finished!

## Delta or Include?

Sometime it gets confusing whether to do Delta or full Include. Here's a common rough use case for these, though this is a rough guideline, not strictly a rule.

**Key:&#x20;**<mark style="color:red;">**Red - Avoid;**</mark> <mark style="color:orange;">**Orange - Depends;**</mark> <mark style="color:green;">**Green - Likely**</mark>

<table><thead><tr><th width="132">Type</th><th width="305">Delta / Unique Name</th><th>Include</th></tr></thead><tbody><tr><td>Audio</td><td><mark style="color:red;"><strong>Rarely needed / Prone to breaking</strong></mark></td><td><mark style="color:green;">Likely to be full include than delta, due to tendency to break.</mark></td></tr><tr><td>Data</td><td><mark style="color:green;">This is <strong>better for  smaller mods</strong>. Small edits to database in RPGMV, such as skills or items. This is good for mods that only change a few things like singular skill balance change, or a new item.</mark></td><td><mark style="color:green;">This is <strong>safer bet for larger mods</strong> that may edit many things, especially if it interacts between each other a lot.</mark></td></tr><tr><td>Fonts</td><td><mark style="color:orange;">This could potentially be used in language mods that requires original Omori font to be altered to include special character.</mark></td><td><mark style="color:green;">If font is being changed at all, it's likely full include.</mark></td></tr><tr><td>Icon</td><td>Likely won't appear in most mod as it  remains unchanged.</td><td><mark style="color:green;">If icon is being changed at all, it's likely full include.</mark></td></tr><tr><td>Image (img)</td><td><mark style="color:orange;">Small edits to images. This is likely additional changes on top of pixel sprites or portraits.</mark> <br><mark style="color:orange;">For example:</mark> <br><mark style="color:orange;">- Shiba Kel (edits only hoodie on Kel)</mark><br><mark style="color:orange;">- Girlmori (edits pigtail on Omori portraits)</mark></td><td><mark style="color:green;">Safer to use full include than delta, due to tendency to break or unintended changes.</mark></td></tr><tr><td>Languages</td><td>Likely won't appear in most mod as it  remains unchanged.</td><td>Likely won't appear in most mod as it  remains unchanged.</td></tr><tr><td>Maps</td><td><mark style="color:orange;">Small edits to maps. Should ideally keep same Tiled versions unless you have Tiled compatibility.</mark></td><td><mark style="color:green;">Likely to be full include than delta, due to tendency to break.</mark></td></tr><tr><td>Movies</td><td><mark style="color:red;"><strong>Rarely needed / Prone to breaking</strong></mark></td><td><mark style="color:green;">Likely to be full include than delta, due to nature of video files.</mark></td></tr><tr><td>Plugins</td><td><mark style="color:orange;">Dependent on context, is prone to bugs currently.</mark></td><td><mark style="color:green;">Plugins you are sure you need to totally override, or totally new made up specific for the mod.</mark></td></tr></tbody></table>

For **Plugins**, you may want to **ignore** some plugins used only in testing the mod. Some common ones are:

* [Quick Load](https://mods.one/mod/quickload) - Called `VykosX-QuickLoadOnStart` which is sometime used to playtest fast, skipping the menu startup intro
* [Console](https://mods.one/mod/console) - Adds a plugin called `console`
* [Better Save and Load](https://mods.one/mod/saveloadplus) - Which alters `Omori Save & Load` plugin

## Bundletool Screen Examples

<div><figure><img src="../../.gitbook/assets/BundleTool Screen.png" alt="" width="489"><figcaption><p>The start up screen; click "use Bundletool"</p></figcaption></figure> <figure><img src="../../.gitbook/assets/BundleTool Folder Prompt.png" alt="" width="240"><figcaption><p>The prompt for finding www_playtest folder</p></figcaption></figure></div>

<div><figure><img src="../../.gitbook/assets/BundleTool Mod Details.png" alt="" width="489"><figcaption><p>Mod detail prompt</p></figcaption></figure> <figure><img src="../../.gitbook/assets/image (7).png" alt="" width="489"><figcaption><p>Example of selecting changes, using Reverie as example. In this case all files are included for change.</p></figcaption></figure></div>
