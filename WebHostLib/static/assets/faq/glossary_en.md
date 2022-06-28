# Multiworld Glossary

There are a lot of common terms used when playing in different game randomizer communities and in multiworld as well.
This document serves as a lookup for common terms that may be used by users in the community or in various other
documentation.

## Item
Items are what get shuffled around in your world or other worlds that you then receive. This could be a sword, a stat 
upgrade, a spell, or any other potential receivable for your game.

## Location
Locations are where items are placed in your game. Whenever you interact with a location, you or another player will
then receive an item. A location could be a chest, an enemy drop, a shop purchase, or any other interactable that can
contain items in your game.

## Check
A check is a common term for when you "check", or pick up, a location. In terms of Archipelago this is usually used for
when a player goes to a location and sends its item, or "checks" the location. Players will often reference their now
randomized locations as checks.

## Slot
A slot is the player name and number assigned during generation. The number of slots is equal to the number of players,
or "worlds", created. Each name must be unique as these are used to identify the slot user.

## World
World in terms of Archipelago can mean multiple things and is used interchangeably in many situations.
* During gameplay, a world is a single instance of a game, occupying one player "slot". However, 
Archipelago allows multiple players to connect to the same slot; then those players can share a world 
and complete it cooperatively. For games with native cooperative play, you can also play together and
share a world that way, usually with only one player connected to the multiworld.
* On the programming side, a world typically represents the package that integrates Archipelago with a
particular game. For example this could be the entire `worlds/factorio` directory.

## RNG
Acronym for "Random Number Generator." Archipelago uses its own custom Random object with a unique seed per generation,
or, if running from source, a seed can be supplied and this seed will control all randomization during generation as all
game worlds will have access to it.

## Seed
A "seed" is a number used to initialize a pseudorandom number generator. Whenever you generate a new game on Archipelago
this is a new "seed" as it has unique item placement, and you can create multiple "rooms" on the Archipelago site from a
single seed. Using the same seed results in the random placement being the same.

## Room
Whenever you generate a seed on the Archipelago website you will be put on a seed page that contains all the seed info
with a link to the spoiler if one exists and will show how many unique rooms exist per seed. Each room has its own 
unique identifier that is separate from the seed. The room page is where you can find information to connect to the
multiworld and download any patches if necessary. If you have a particularly fun or interesting seed, and you want to 
share it with somebody you can link them to this seed page, where they can generate a new room to play it! For seeds 
generated with race mode enabled, the seed page will only show rooms created by the unique user so the seed page is 
perfectly safe to share for racing purposes.

## Logic
Base behavior of all seeds generated by Archipelago is they are expected to be completable based on the requirements of
the settings. This is done by using "logic" in order to determine valid locations to place items while still being able
to reach said location without this item. For the purposes of the randomizer a location is considered "in logic" if you 
can reach it with your current toolset of items or skills based on settings. Some players are able to obtain locations
"out of logic" by performing various glitches or tricks that the settings may not account for and tend to mention this
when sending out an item they obtained this way.

## Progression
Certain items will allow access to more locations and are considered progression items as they "progress" the seed.

## Trash
A term used for "filler" items that have no bearing on the generation and are either marginally useful for the player
or useless. These items can be very useful depending on the player but are never very important and as such are usually
termed trash.

## Burger King / BK Mode
A term used in multiworlds when a player is unable to continue to progress and is awaiting an item. The term came to be 
after a player, allegedly, was unable to progress during a multiworld and went to Burger King while waiting to receive
items from other players.

* "Logical BK" is when the player is unable to progress according to the settings of their game but may still be able to do
things that would be "out of logic" by the generation.

* "Hard / full BK" is when the player is completely unable to progress even with tricks they may know and are unable to
continue to play, aside from doing something like killing enemies for experience or money.

## Sphere
Archipelago calculates the game playthrough by using a "sphere" system where it has a state for each player and checks
to see what the players are able to reach with their current items. Any location that is reachable with the current
state of items is a "sphere." For the purposes of Archipelago it starts playthrough calculation by distributing sphere 0
items which are items that are either forced in the player's inventory by the game or placed in the `start_inventory` in
their settings. Sphere 1 is then all accessible locations the players can reach with all the items they received from
sphere 0, or their starting inventory. The playthrough continues in this fashion calculating a number of spheres until
all players have completed their goal.

## Scouts / Scouting
In some games there are locations that have visible items even if the item itself is unobtainable at the current time.
Some games utilize a scouting feature where when the player "sees" the item it will give a free hint for the item in the
client letting the players know what the exact item is, since if the item was for that game it would know but the item
being foreign is a lot harder to represent visually.
