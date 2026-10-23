UNDEAD AND DEMONS
=================

Purpose
-------

Undead and Demons have an unusual relationship in Valheim.

Despite belonging to different factions, wild Undead and wild Demons do not
normally consider each other enemies.

Because OTAB can modify hostility relationships for tamed creatures, this
raises an important question:

    Should this relationship survive taming?

The answer used by these data files changed during development.


THE VANILLA RELATIONSHIP
------------------------

Vanilla treats Undead and Demons as separate factions, but its hostility
logic contains a special relationship between them.

Wild Undead do not consider Demons enemies, and wild Demons do not consider
Undead enemies.

This is part of Vanilla's hostility behavior and not something introduced by
OTAB.


THE ORIGINAL APPROACH
---------------------

Originally, the creature data preserved this relationship even after a
creature became tamed.

The reasoning followed an important design principle:

    Tamed is a state, not a new creature identity.

A tamed Skeleton is still undead, and a tamed Demon is still a demon.

It therefore seemed appropriate for their existing relationship to remain
intact rather than being overwritten by the tamed state.


THE ASKSVIN PROBLEM
-------------------

The Asksvin revealed a problem with this approach.

Asksvins are Demons, are naturally encountered in the Ashlands, and can
already be tamed in Vanilla.

The Ashlands are also populated heavily by Undead and Demons.

Vanilla allows a tamed Asksvin to fight these creatures even though a wild
Asksvin would normally consider them allies.

Forcing the wild Undead/Demon relationship to persist after taming would
therefore make tamed Asksvins considerably less useful against the enemies
of their own biome.

More importantly, this would be a restriction introduced by these data files
rather than behavior preserved from Vanilla.

The same reasoning applies to other tamed Undead and Demons. A ritual
Skeleton may therefore fight wild Undead or Demons just as other tamed
creatures can be used against creatures they would not normally fight.


THE REVISED APPROACH
--------------------

The Undead/Demon relationship is preserved where it naturally exists:

    between wild creatures.

It is not forcibly preserved after taming.

A wild Skeleton and a wild Demon can remain allies.

A tamed Skeleton may fight wild Undead and Demons on behalf of the player.

Likewise, a tamed Demon may fight wild Undead and Demons.

This preserves the Vanilla relationship without overriding Vanilla's normal
treatment of tamed creatures.


IDENTITY AND ALLEGIANCE
-----------------------

This change does not contradict the principle:

    Tamed is a state, not a new creature identity.

Instead, it introduces an important distinction:

    Creature identity and creature allegiance are not the same thing.

A tamed Skeleton remains undead.

A tamed Demon remains a demon.

Taming does not need to change what a creature is in order to change whose
side it is on.


SUMMARY
-------

Wild Undead and Demons do not normally consider each other enemies in
Vanilla.

The original creature data extended this relationship beyond taming, but the
Vanilla behavior of tamed Asksvins demonstrated why doing so was undesirable.

The relationship is therefore preserved among wild creatures but is not
forced upon their tamed counterparts.

Taming does not have to change what a creature is.

It can change whose side it is on.