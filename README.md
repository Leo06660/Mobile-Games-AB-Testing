# Mobile-Games-AB-Testing
<a href="URL_REDIRECT" target="blank"><img align="center" src="https://miro.medium.com/v2/resize:fit:786/format:webp/1*JzfrTY46fhRNOrM9K6u7OQ.jpeg" height="100" /></a>

## Project Description
<p><a href="https://www.facebook.com/cookiecatsgame">Cookie Cats</a> is a hugely popular mobile puzzle game developed by <a href="http://tactile.dk">Tactile Entertainment</a>. It's a classic "connect three"-style puzzle game where the player must connect tiles of the same color to clear the board and win the level. 
Here's a brief video showcasing the game demo: https://youtu.be/GaP5f0jVTWE.

As players progress through the game from one level to the next, they will occasionally encounter gates that force them to wait a non-trivial amount of time or make an in-app purchase to progress.

## Main Objective
Analyze an A/B test and determine if the gate should be moved from level 30 to level 40

## Data Source
The dataset is publicly available on Datacamp, which can be retrieved from https://www.datacamp.com/projects/184.
Feature|Type|Description
---|---|---
**userid**|_id_|A unique number that identifies each player.
**version**|_string_|Whether the player was put in the control group (gate_30 - a gate at level 30) or the group with the moved gate (gate_40 - a gate at level 40).
**sum_gamerounds**|_integer_|The number of game rounds played by the player during the first 14 days after install.
**retention_1**|_boolean_|Did the player come back and play 1 day after installing?
**retention_7**|_boolean_|Did the player come back and play 7 days after installing?

## Result
<div id="header" align="left">
  <strong>1-Day Retention</strong>
</div>
<div id="header" align="center">
  <img src="https://github.com/Leo06660/Mobile-Games-AB-Testing/blob/main/chart/1-Day%20Retention.png?raw=true"/>
</div>
<div id="header" align="left">
  <strong>7-Day Retention</strong>
</div>
<div id="header" align="center">
  <img src="https://github.com/Leo06660/Mobile-Games-AB-Testing/blob/main/chart/7-Day%20Retention.png?raw=true"/>
</div>

## Conclusion
<ul>
    <li>The bootstrap result tells us that there is strong evidence that 7-day retention is higher when the gate is at level 30 than when it is at level 40. The conclusion is: If we want to keep retention high — both 1-day and 7-day retention — we should not move the gate from level 30 to level 40.</li>
    <li>Close to 4,000 players (4.4%) did not play a single round after installation and more than 20,000 players (23%) played five rounds or less. We can try to collect player feedback, for example, through an in-app survey.</li>
</ul>
