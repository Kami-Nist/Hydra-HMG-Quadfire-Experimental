Hydra HMG - Quadfire Experimental v0.1.7

Branch source: proven Hydra v0.1.2 architecture checkpoint.

HARD INVARIANT:
- 5 visible slots total.
- 4 ammunition slots remain in ONE primary ItemContainer (capacity=4).
- 1 flashlight/laser attachment slot remains in the original SubContainer (capacity=1).

EXPERIMENTAL CHANGE (ONLY FIRING MUTATION):
- Added an OnUse StatusEffect inside RangedWeapon targeting Contained items and invoking <Use />.
- Purpose: test whether one trigger event propagates use to all four occupied ammunition slots.
- Original RangedWeapon RequiredItems remains singular.
- Container topology is unchanged.

TEST:
Load one identical vanilla shotgun-ammo item into each of the four ammo slots. Fire one controlled trigger pull. Record projectile count and ammo consumption.

v0.1.2 remains the frozen clean architecture baseline.
v0.1.3 duplicated RequiredItems and remained Bang x1; that failed experiment is NOT inherited here.
v0.1.4 added Volleyfire function.
v0.1.5 was an attempt at making the rounds increment from max to min (12 -> 1)
v0.1.6 was an another implementation attempt from slots 0-3 rather from 1-4