---
description: Functions and variables in texts
---

# Text Codes

## RPG Maker MV Text Codes

RPG Maker MV comes with text codes on it's own, being the following:

<table><thead><tr><th width="108">Code</th><th>Function</th></tr></thead><tbody><tr><td>\V[n]</td><td>Will be replaced with the value of the nth <strong>variable</strong>.</td></tr><tr><td>\N[n]</td><td>Will be replaced with the name of the nth <strong>actor</strong>.</td></tr><tr><td>\P[n]</td><td>Will be replaced by the <strong>name</strong> of the nth (arranged order) party member.</td></tr><tr><td>\G</td><td>Will be replaced by the <strong>currency unit</strong>.</td></tr><tr><td>\C[n]</td><td>Draw the subsequent text in the nth <strong>color</strong>. Text color conforms to the contents of the [Window.png] system image.</td></tr><tr><td>\I[n]</td><td>Draws the nth <strong>icon</strong>.</td></tr><tr><td>\{</td><td>Increases the text by 1 step.</td></tr><tr><td>\}</td><td>Decreases the text by 1 step.</td></tr><tr><td>\\</td><td>Replaced with the backslash character.</td></tr><tr><td>\$</td><td>Open the gold window.</td></tr><tr><td>\.</td><td>Wait for 1/4 second.</td></tr><tr><td>\|</td><td>Wait for 1 second.</td></tr><tr><td>\!</td><td>Wait for button input.</td></tr><tr><td>\></td><td>Display remaining text on same line all at once.</td></tr><tr><td>\&#x3C;</td><td>Cancel the effect that displays text all at once.</td></tr><tr><td>\^</td><td>Do not wait for input after displaying the next.</td></tr></tbody></table>

_Credit: Yanfly.moe Wiki_

{% hint style="info" %}
Beware of the slashes! Text code uses backslashes (\\) not normal slashes (/).
{% endhint %}

## TDS Text Effects

The following contains code related to text movements used in Omori.

<table><thead><tr><th width="154.5">Code</th><th>Function</th></tr></thead><tbody><tr><td>\SINV[n]</td><td>Makes the text shake vertically. When n is:<br>0 - Disable<br>1 - Normal wave<br>2 - Dense wave</td></tr><tr><td>\SINH[n]</td><td>Makes the text shake horizontally. When n is:<br>0 - Disable<br>1 - Enable</td></tr><tr><td>\QUAKE[n]</td><td>Makes the text wobble aggressively. When n is:<br>0 - Disable<br>1 - Intense quake<br>2 - Softer quake</td></tr><tr><td>\RAINBOW[n]</td><td>Adds an animated rainbow effect to the text. When n is:<br>0 - Disable<br>1 - Enable</td></tr></tbody></table>

## Archeia Text Codes

In the following the most used are common event text code. For example, to call shake screen common event. There are other codes but it isn't used at all in Omori

<table><thead><tr><th width="177">Code</th><th>Function</th></tr></thead><tbody><tr><td>\com[n]</td><td>Invokes the <strong>common event</strong> of ID <code>n</code></td></tr></tbody></table>

{% hint style="info" %}
Fun fact: Text Codes can be invoked when set as character name and the name is trying to be called.
{% endhint %}

## Useful Resources

* [http://www.yanfly.moe/wiki/Category:Text\_Codes\_(MV)](http://www.yanfly.moe/wiki/Category:Text_Codes_\(MV\))
* [https://github.com/Gilbert142/gomori/wiki/Text-Formatting](https://github.com/Gilbert142/gomori/wiki/Text-Formatting)
