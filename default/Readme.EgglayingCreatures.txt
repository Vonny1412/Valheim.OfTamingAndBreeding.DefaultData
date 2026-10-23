EGG-LAYING CREATURES
====================

Purpose
-------

Egg-laying creatures require slightly different population rules from
creatures that produce offspring directly.

The standard OTAB data pack therefore separates two things that Vanilla may
treat as part of the same population limit:

    Egg production

and:

    Actual population growth

The central principle is:

    Laying an egg is reproduction,
    but an egg is not yet population growth.


EGGS AND MAX CREATURES
----------------------

In Vanilla, eggs can count towards the maximum creature population.

Hens are a good example.

With a maximum population of 10, Vanilla checks both:

    Hen
    ChickenEgg

An existing egg can therefore occupy one of the available population slots.

The standard OTAB data pack changes this behavior by explicitly defining
which prefabs count towards the population limit.

For Hens, the relevant population consists of:

    Hen
    Chicken

Eggs themselves are excluded.

The maximum population remains 10.

This means that:

    9 Hens + any number of Eggs = 9 / 10

while:

    9 Hens + 1 Chicken = 10 / 10

Eggs can therefore continue to be produced without allowing the resulting
creatures to bypass the actual population limit.


WHY EGGS ARE TREATED DIFFERENTLY
--------------------------------

OTAB includes an anti-exploit system intended to prevent creatures from
reproducing normally when they are simply confined in unsuitable enclosures.

This system is enabled by default, although it can be disabled through the
configuration.

Because reproduction is already restricted in this way, the standard data
pack is deliberately more permissive in how eggs interact with population
limits.

A properly maintained group of egg-laying creatures should be allowed to
continue producing eggs while the actual creature population remains below
its configured maximum.

For example, if 9 Hens are present in an enclosure with a maximum population
of 10, they may continue laying eggs while they are fed and all other
reproduction conditions are satisfied.

The eggs themselves do not consume the final population slot.


EGG PRODUCTION IS NOT AUTOMATIC POPULATION GROWTH
-------------------------------------------------

By default, OTAB uses:

    RequireEggsDroppedByPlayer = true

This creates an important distinction between an egg being produced and an
egg being intentionally allowed to develop.

An egg naturally dropped by a creature does not automatically begin growing
or hatching.

The player must first collect the egg and deliberately place it again.

The normal process is therefore:

    Creature lays Egg
            |
            v
       Egg can remain,
       accumulate or
       be collected
            |
            v
    Player places Egg
            |
            v
      Egg can develop
            |
            v
       New creature

This gives the player control over when egg production becomes actual
population growth.

It also prevents the exclusion of eggs from the population count from
automatically turning an enclosure into uncontrolled population growth.


CONFIGURABILITY
---------------

These rules describe the recommended behavior of the standard OTAB data
pack.

They are not mandatory rules imposed on every OTAB configuration.

Creature data can explicitly define which prefabs are considered when
checking the maximum nearby creature population.

Server administrators and custom data packs can therefore choose different
population rules.

Likewise, RequireEggsDroppedByPlayer can be disabled if naturally dropped
eggs should be allowed to develop without player intervention.

The standard data pack uses these options to provide a compromise:

    Egg production remains useful.

    The player decides which eggs should develop.

    Actual creatures still respect the population limit.

    OTAB's anti-exploit restrictions still apply to reproduction.


SUMMARY
-------

For egg-laying creatures, the standard data pack distinguishes between
producing potential offspring and actually increasing the creature
population.

Eggs do not occupy population slots.

Hatched creatures do.

Naturally laid eggs do not develop automatically by default.

The player decides which eggs are placed for development.

This allows egg-laying creatures to remain productive without allowing their
actual population to bypass the configured limits.