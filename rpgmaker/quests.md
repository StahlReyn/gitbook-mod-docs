---
description: About setting up quests. Omori uses custom plugins to make quests.
---

# Quests

## Important Common Events

Many of the event dependent on <mark style="color:red;">**Variable 16**</mark> which is grabbed as **event ID**

<table><thead><tr><th width="81">ID</th><th width="174">Name</th><th width="349">Note</th><th>Uses</th></tr></thead><tbody><tr><td>47</td><td>★ Display New Quest</td><td><p>Displays the Lightbulb bubble that shows the quest is still Finished.</p><p>Alternative: <code>this.setEventIcon(eventid, 'quest', index);</code></p></td><td>Var 17</td></tr><tr><td>48</td><td>★ Display Ongoing Quest</td><td>Displays the Lightbulb bubble that shows the quest is still Ongoing.</td><td>Var 17</td></tr><tr><td>49</td><td>★ Display Quest Finish</td><td>Displays the Lightbulb bubble that shows the quest is still Finished.</td><td>Var 17</td></tr><tr><td>50</td><td>★ Erase Bubble</td><td></td><td>Var  17</td></tr><tr><td>300</td><td>-- Quest Accept</td><td>Plays Sound: <code>SYS_quest_get</code></td><td></td></tr><tr><td>301</td><td>-- Quest Complete</td><td>Plays Sound: <code>SYS_quest_complete</code></td><td></td></tr></tbody></table>

## Example - LEAFY's Quest

For bubble, set the <mark style="color:red;">Variable 16 "Quest Balloon ID</mark>" to the event ID that you want the bubble to be over.

Example used here is LEAFY's Quest in Map 105 -- TRAIN STATION WAITING AREA, Event 5 at 14,38. The event has ID of 5, so the variable is set to 5 accordingly to be used in other Event

<figure><img src="../.gitbook/assets/Balloon ID.png" alt=""><figcaption><p>The starting events of LEAFY's Quest</p></figcaption></figure>

* <mark style="color:red;">**Control Variables : #16:**</mark> to set Event ID, in this case LEAFY event is 5.
* <mark style="color:blue;">**Common Event : ★ Erase Bubble:**</mark> Removes existing bubble on event of <mark style="color:red;">**Variable 16**</mark>, like cleaning up before doing other bubbles.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption><p>LEAFY's Initial quest Accept later on.</p></figcaption></figure>

* <mark style="color:red;">**Control Switches : #1661:**</mark> Any switch to keep track for using in other events
* <mark style="color:red;">**Control Variables : #16:**</mark> to set Event ID, in this case LEAFY event is 5. (Technically redundant here as it's set already before at start, but for good measure.)
* <mark style="color:blue;">**Common Event : -- Quest Accept:**</mark> Plays Quest accept sound
* <mark style="color:blue;">**Common Event : ★ Display Quest Finish:**</mark> Quest is finished, in this case it's in case player already has slain 5 bunnies before interacting with LEAFY.
* <mark style="color:blue;">**Common Event : ★ Display Ongoing Quest:**</mark> Quest is Ongoing, the usual if the player has not finished yet, so therefore quest is still going on
* <mark style="color:red;">**Control Self Switch : A:**</mark> To toggle own event to another page, which in LEAFY's case cuts off intro and throws to more quest loop to kill more bunnies.
