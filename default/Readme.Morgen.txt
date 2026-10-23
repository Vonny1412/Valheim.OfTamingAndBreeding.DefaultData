MORGEN
======

LORE AND DESIGN
---------------

Morgen are dangerous Ashlands creatures whose appearance and behavior make
ordinary domestication difficult to justify.

The Vanilla trophy suggests that only a twisted mind could summon one;
the heart description questions whether it ever truly beat. Putrid Holes
contain Asksvin carcasses and organic remains, and an Ashlands Dvergr warns
that a Morgen might smell a person and make them its dinner.

These are clues, not proof of how Morgen originate or what they eat. OTAB
uses them as inspiration for an unnatural creature with a dangerous appetite.

GROWTH
------

The ritual produces an already tamed Morgen at 25% scale. It grows through
50% and 75% to its normal size, provided it is fed.

Every 60 seconds of fed growth time, there is a 10% chance to advance
(9:1 weight for staying versus advancing). This averages 10 minutes per
stage, or 30 minutes overall, excluding pauses while hungry. Growth cannot
fail permanently or regress.

An earlier design required taming a wild offspring before it matured.
Simulations of that discarded setup gave roughly 100%, 88%, and 56% taming
success for zero-, one-, and two-star offspring. Combined with the rare
trophy and ritual cost, this was considered unnecessarily punitive.

A growing heart and the organic piles in Putrid Holes were also considered
as juvenile forms, but neither was convincing without custom models.
Vanilla does not identify the piles as Morgen offspring.

FEEDING
-------

Vanilla does not establish a Morgen diet. The available foods are inspired
by its appearance, the remains around its lairs, and the Dvergr's warning.

Each growing stage randomly selects ONE food from a weighted list. The
preference may change after growth. This makes feeding less predictable
without requiring every listed ingredient. The current food is shown in
the creature's hover text.

Asksvin carcass pieces found in the world were excluded because they are
finite resources, unlike replenishable food items.

HUNGER AND HOSTILITY
--------------------

A growing Morgen is tamed but may attack players after prolonged hunger.
This reflects the Dvergr's warning; it is not established Vanilla behavior.

Growth is checked at 10-second intervals, with a 60-second growth
cycle. The fed duration is deliberately set to 90 seconds to ensure
the final growth tick isn't missed due to feeding expiring first.
Player hostility begins after four times the effective fed duration
(360 seconds with a factor of 1.0).

Only growing Morgen use this hostility rule. The adult is commandable and
does not require feeding.
