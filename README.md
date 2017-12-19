# The Last Grapple

The very last grapple mod you're going to need!  Infinite ammo and durability!  Faster!  And no grapple bug!

## Source
https://github.com/LaoArchAngel/TheLastGrapple

## What It Does
Provides a new crossbow (Grapple XBow) used solely for grappling.  It has a configurable length, pull, and drop speed.  It has unlimited ammo and shoots faster.  Furthermore, it is immune to the "grapple bug".

## Features
* Clean and completely stackable.
* Grapple XBow has unlimited durability.
* Unlimited grapple ammo.
* Configurable max rope length.
* Configurable pull speed / strength. *Set this high enough, pull yourself to the ground, and kill yourself, parachute be damned! :D*
* Configurable drop speed.  For those who want a little more granual control of how far you drop with a click of the right-mouse button!


## The Grapple Bug / Glitch
One of the most annoying issues with most other infinite-ammo, fast-action grapple guns or crossbows came when it was accidentally (or due to lag) shot twice in quick succession.  This, at first, would cause no issue.  However, if the shooter were to get on a dino and rode far enough away from where the grapple hit (usually render distance), their screen would immediately start "jumping" back and forth, as if being pulled by the grapple.  Hitting "C" would provide immediate relief, but the bug would re-appear the next time they got off their dino far enough away from the grapple.  One available, more permanent solution was to use beds to teleport from one place to another (usually two beds side by side).  This would clear the glitch.  At least until they shot the grapple twice in quick succession again.

## Configuration
**RopeLength** :: Float. Multiplies the default rope length.  Default is 1.0.
**PullSpeed** :: Float. Multiplies the default pull speed / force.  Beware!  Set this too high and it WILL kill you when pulling down..  Default is 1.0.  About 1.5 - 2.0 is nice.
**DropSpeed** :: Float. Multiplies the default drop speed.  Default is 1.0.  I like 0.5.
**GrappleSpeed** :: Float.  Multiplies the default speed of the grapple projectile.  Default is 1.0.  I like 1.5.
```
[LastGrapple]
RopeLength=1.5
PullSpeed=1.5
DropSpeed=0.5
GrappleSpeed=2.5
```

## Technical Details
**Mod ID**
1210379301

**Item Class**
`TLGItem_WeaponCrossbow_C`

**Engram Class**
`EngramEntry_TLG_Crossbow_C`

**Spawn Code**
`cheat giveitem "Blueprint'/Game/Mods/TheLastGrapple/Items/TLGItem_WeaponCrossbow.TLGItem_WeaponCrossbow'" 1 1 0`

**Engram Override**
`OverrideNamedEngramEntries=(EngramClassName="EngramEntry_TLG_Crossbow_C",EngramLevelRequirement=0,EngramPointsCost=0,EngramHidden=False,RemoveEngramPreReq=False)`

**Crafting Cost Override**
`ConfigOverrideItemCraftingCosts=(ItemClassString="TLGItem_WeaponCrossbow_C",BaseCraftingResourceRequirements=((ResourceItemTypeString="PrimalItemResource_Thatch_C",BaseResourceRequirement=1.0,bCraftingRequireExactResourceType=True)))`
