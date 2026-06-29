---
description: Common Note tags in event such as offset and hitbox resizing
---

# Map Event Notetags

Here are some common plugin note tags used in events used in Omori.

<table><thead><tr><th width="320">Command</th><th width="305">Notes</th><th>Plugin</th></tr></thead><tbody><tr><td><pre><code><strong>&#x3C;Hitbox Up: x>
</strong><strong>&#x3C;Hitbox Left: x>
</strong><strong>&#x3C;Hitbox Right: x>
</strong><strong>&#x3C;Hitbox Down: x>
</strong></code></pre></td><td>Expand the hitbox upward, left, right, or down by x tiles. If used, makes the event immobile.<br><br>Commonly used in teleports and walls</td><td><a href="http://www.yanfly.moe/wiki/Event_Hitbox_Resize_(YEP)">Event Hitbox Resize (YEP)</a></td></tr><tr><td><p></p><pre><code>&#x3C;Sprite Offset X: +n>
&#x3C;Sprite Offset X: -n>
&#x3C;Sprite Offset Y: +n>
&#x3C;Sprite Offset Y: -n>
&#x3C;Sprite Offset: +x, +y>
&#x3C;Sprite Offset: -x, -y>
</code></pre></td><td>Offset sprite by n amount of pixels, in x or y direction.</td><td><a href="http://www.yanfly.moe/wiki/Event_Sprite_Offset_(YEP)">Event Sprite Offset (YEP)</a></td></tr><tr><td><pre><code>&#x3C;Copy Event: Map x, Event y>
&#x3C;Copy Event: mapId, eventId>
&#x3C;Copy Event: template>
</code></pre></td><td><p>Copies event, recommended to read more detail in wiki.</p><p><br>Commonly used in enemies.</p></td><td><a href="http://www.yanfly.moe/wiki/Event_Copier_(YEP)">Event Copier (YEP)</a></td></tr><tr><td><p></p><pre><code>&#x3C;Activation Square: x>
&#x3C;Activation Radius: x>
&#x3C;Activation Row: x>
&#x3C;Activation Column: x>
</code></pre></td><td><p>Give activation range, activating certain events from a distance.</p><p></p><p><strong>Square</strong>: x tiles from center in a <em>square</em> shape.</p><p><strong>Radius</strong>: x tiles from center in a <em>diamond</em> shape.<br><strong>Row</strong>: <em>Horizontal</em> bar to whole map, with x thickness.</p><p><strong>Column</strong>: <em>Vertical</em> bar to whole map, with x thickness.</p></td><td><a href="http://www.yanfly.moe/wiki/Event_Proximity_Activate_(YEP)">Event Proximity Activate (YEP)</a></td></tr></tbody></table>
