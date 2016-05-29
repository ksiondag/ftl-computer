# FTL Computer #

You know how in some sci-fi, including Star Trek, there's a computer that has
data on events and stuff and maybe even gives a likelihood of what will happen
based on that data?

Yeah, let's add that to FTL.

This will start as an outside-game, webapp tool that, once properly fleshed
out, will maybe be modded into the game itself properly.


## Why? ##

I don't like using the [FTL Wiki](http://ftl.wikia.com/wiki/FTL:_Faster_Than_Light_Wiki)
to know what to do, and as of the advanced edition, the number of stuff that
happens is too large to keep properly in my head. Further, planning ahead for
various events is just something I don't do because I don't have good data on
what to expect.

Enter the FTL Computer. Use it to log the events that have happened so far, and
use that data during future events to decide what to do. It will log how often
an event happened, how often a choice was picked, and what happened and why.

This hopefully gains the positives of the wiki, but also maintains and
hopefully improves the explorative aspect of the game. As an actual mod, it
adds another trope of sci-fi to the game (the computer, and percentage chance
of things happening).

### Use-Case ###

Consider the following [actual event](http://ftl.wikia.com/wiki/Large_asteroid_field)
from the game:

"Scans reveal a large asteroid field nearby. Short-range scanners may discover
useful materials while we wait for the FTL to recharge."

This event can happen in any sector. So ideally, a record of this event will
show a random distribution of this event happening in basically every sector,
with enough data showing it happening with equal likelihood in any non-nebula
location in any given sector.

The choices available and their possible outcomes:

1. Explore the asteroid field
  * A brief exploration yields nothing of interest
    * Nothing happens
  * Scans reveal a number of asteroids with useful compositions. You extract
    some fuel.
    * You receive a large amount of fuel
  * You discover the remains of a ship embedded into an asteroid. It still has
    some functional missles.
    * You receive a medium amount of scrap and missles.
  * You happen upon an abandoned mining site. A few mining drones were left
    behind and could be repurposed.
    * You receive a medium amount of scrap and drone parts.
  * The asteroid field proved more dangerous than expected. Some asteroids
    managed to get through your ship's defenses.
    * Your ship takes 5 hull damage.
  * A pirate ship hiding behind one of the larger asteroids attacks you!
    * The environment changes to an Asteroid Field. Fight the ship (default
      rewards).
1. Too dangerous. We'll just wait for the FTL to charge.
  * Nothing happens.
1. (Scrap Recovery Arm) Attempt to mine the asteroids.
  * You carefully extract as much usable material as possible from the nearest
    asteroids while waiting for the FTL to charge.
    * You receive a high amount of scrap.

Now, the FTL Computer would:

* notify the user what special blue events triggered in previous occurances of
  the event (in this case only the Scrap Recovery Arm).
* show how often this event happened
  * in which sectors
  * on what type of area (areas not always mutually exclusive)
    * nebula
    * regular
    * ship present
    * asteroid field
    * ion storm
    * incomplete (area knowledge sometimes requires long-range scanners or
      equivalent)
* show how often a choice was taken
  * show frequency of results of event

Some graphs and stuff would be neat, too.

## Roadmap ##

### 0.x.0 ###

Quick and dirty mock-up webapp.

1. A means of entering events and results into a database of events
  * Event text
  * Options
  * Nested result event/options
  * Difficulty level
2. Incrementing count of events/results
3. Special circumstances (what causes blue options)
4. Sector event happened in
5. Area-type event happened in
6. Reward/risk scaling tracking
7. Ship status stat tracking

### 1.x.0 ###

Prettier webapp.

1. CSS
2. User-signup
3. Import/Export/Merge event database
4. Graphs

### 2.x.0 ###

In-game mod?!?!?!?!?!?

1. A means of entering events and results into a database of events
2. Incrementing count of events/results
3. Special circumstances (what causes blue options)
4. Sector event happened in
5. Area-type event happened in
6. Reward/risk scaling tracking
7. Ship status stat tracking

### 3.x.0 ###

Prettier in-game polish?!?!?!?

1. Styling
2. Import/Export/Merge event database
3. Graphs? (are there graphs in-game already?)

