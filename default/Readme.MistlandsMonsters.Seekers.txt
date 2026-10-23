THE SEEKER FAMILY
=================

Seekers, Seeker Soldiers and Seeker Broods are treated as different forms of
the same creature family.

Valheim already provides an important part of their lifecycle. Seeker Eggs
can hatch into Seeker Broods, which appear as small, immature forms of the
creatures found throughout the Mistlands.

The exact relationship between the adult forms is not explained.


Seeker Reproduction
-------------------

The Queen is strongly associated with the reproduction of the Seeker colony,
but using her for breeding would require treating a boss as part of the
taming system.

A different reproductive model is therefore used here.

Normal Seekers and Seeker Soldiers can reproduce together. One possible
interpretation is that they represent female and male forms of the species.

Valheim does not establish this.

Reproduction produces a custom Seeker Egg rather than an adult Seeker or a
Brood directly. The egg can be incubated near a fire under a sufficiently
covered roof. After hatching, it produces a tamed Seeker Brood.

This allows the Seeker family to participate in breeding without making the
Queen tameable.


Seeker Eggs
-----------

Seeker Eggs found in Infested Mines are normally environmental objects that
can hatch when a player approaches. This configuration makes the regular
SeekerEgg objects collectible, without removing their original hatching
behavior. Collecting an egg therefore requires reaching it before it hatches.

The SeekerEgg_alwayshatch variant is not made collectible by default. To
include it, remove the leading underscore from the configuration file:

    Misc/_SeekerEgg_alwayshatch.yml

Collected eggs yield the custom OTAB_SeekerEgg item. This item can also be
produced through breeding. It is incubated near a fire, under a roof with
at least 70% cover, and hatches after 1800 seconds under suitable conditions.

The resulting creature is a tamed OTAB_SeekerBrood.


Seeker Broods
-------------

Wild Seeker Broods are left unchanged. Instead, a separate custom prefab,
OTAB_SeekerBrood, is used for breeding and growth.

This distinction is particularly important because the Queen can produce
many wild Broods during her boss encounter. Adding taming and growth
components to all of them would create unnecessary runtime overhead during
an already demanding fight.

The custom Broods cannot be tamed or fed directly. They hatch already tamed
and grow into an adult after 1800 seconds.

A custom Brood can eventually develop into either:

    Seeker          90%
    Seeker Soldier  10%

Valheim does not establish that Broods develop into these two forms in these
proportions. The distinction is an interpretation of the different forms
found within the Seeker colony.


Royal Jelly
-----------

Royal Jelly is found in Infested Mines together with the Seeker colony.
Stores of it can be found in the same environment as Seeker Eggs, while
Seeker Broods themselves can also drop Royal Jelly.

Valheim does not explicitly explain this relationship.

These observations are interpreted here as Royal Jelly being associated with
the nourishment and development of Seeker young. The Royal Jelly found near
their nesting areas may therefore represent food stored for developing
Broods.

This interpretation is also consistent with the familiar biological
association between royal jelly and insect larvae, but it is not established
Valheim lore.

Royal Jelly is not required for growth in this configuration.


Sap
---

Adult Seekers and Seeker Soldiers are fed with Sap.

Sap is closely associated with the Mistlands and provides a suitable food
source for the large insect-like creatures.

Valheim does not state that Seekers naturally consume Sap. This is an
interpretation used to connect their feeding to their native environment.


Summary
-------

The Seeker family reproduces through collectible or bred eggs, which hatch
into custom, tamed Broods and eventually develop into Seekers or Seeker
Soldiers. Wild Broods remain unchanged, avoiding additional overhead during
the Queen encounter. Reproduction between Seekers and Soldiers remains an
interpretation used to make breeding possible without involving the Queen.
