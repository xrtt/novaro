# Warlock

> TODO:
> [ ] Skill build
> [ ] Equipment

## Content

- [Mind slots](#Mind-slots)
- [Stats](#Stats)
- [Skills](#Skills)
- [Equipment](#Equipment)
- [See also](#See-also)

## Mind slots

```math
mindSlots = freezingSpell * 4 + floor(baseLvl / 10) + floor (INT / 10)
```

> In NovaRO, `freezingSpell` has `x8` mod.

Max you can have 7 spells in mind.
`Crimson Rock` requires 12 slots,
`Comet` and `Tetra Vortex` both require 22 slots.
So we need `12 * 7 = 84` or `22 * 4 = 88` slots.

| `freezingSpell` | `baseLvl` | `INT` | Total |
| --------------- | --------- | ----- | ----- |
| 0               | 200       | 120   | 32    |
| 5               | 200       | 120   | 72    |
| 6               | 200       | 120   | 80    |
| 7               | 200       | 120   | 88    |
| 10              | 200       | 120   | 112   |

## Stats

| `baseLvl` | 99 | 200 |
| --------- | -- | --- |
| `STR`     | 1  | 1   |
| `AGI`     | 1  | 90  |
| `VIT`     | 60 | 90  |
| `INT`     | 90 | 120 |
| `DEX`     | 90 | 120 |
| `LUK`     | 1  | 90  |

`jobLvl` bonuses:

| `jobLvl` | 70 |
| -------- | -- |
| `STR`    | 1  |
| `AGI`    | 7  |
| `VIT`    | 8  |
| `INT`    | 15 |
| `DEX`    | 8  |
| `LUK`    | 4  |


## Skills

- [Skill simulator](https://irowiki.org/~himeyasha/skill4/wlk.html)
- [4th jobs](https://www.divine-pride.net/forum/index.php?/topic/4672-kro-fourth-class-jobs-skills-info-and-related-items-updated-16092020/&tab=comments#comment-8022)

Skill	Type	Properties	Description
2205.png Marsh of Abyss	Support	
Max Level: 5
Target: Enemy
SP Cost: 38 + (2 x Skill Level)
Var. Cast Time: 2.5s
Fixed Cast Time: 0.5s
Cast Delay: 1.0s
Range: 11
Curse a target for 30 seconds to reduce their Movement Speed, DEF, and Flee.

The reduction of DEF and Flee are increased based on the caster's Job Level and INT.
This skill will remove 29.png Increase Agility, 383.png Wind Walk, and ASPD potions.

[Lv 1] : -50% Movement Speed.
[Lv 2] : -60% Movement Speed.
[Lv 3] : -70% Movement Speed.
[Lv 4] : -80% Movement Speed.
[Lv 5] : -90% Movement Speed.
2208.png Radius	Passive	
Max Level: 3
Increase the casting range of Warlock skills, and reduce their Fixed Casting Time as well.

[Lv 1] : +1 Cell range, -10% Fixed Casting Time.
[Lv 2] : +2 Cell range, -15% Fixed Casting Time.
[Lv 3] : +3 Cell range, -20% Fixed Casting Time.
2222.png Summon Fire Ball	Support	
Max Level: 2
Target: Self
SP Cost: 2 + (8 x Skill Level)
Var. Cast Time: 2.0s
Summon a Fire elemental ball that will float around you, and continuously drain SP while active.
The Fire ball can later be thrown at an enemy using 2230.png Release, where it will deal Fire property magic damage to a single target.


A Maximum of 5 elemental balls can be summoned at a time.

These elemental balls can also be used for 2217.png Tetra Vortex to make one of the skills hits deal Fire property magic damage.


[Lv 1] : Summons 1 elemental ball, Duration 120 seconds.
[Lv 2] : Summons 5 elemental balls, Duration 280 seconds.
2223.png Summon Lightning Ball	Support	
Max Level: 5
Target: Self
SP Cost: 2 + (8 x Skill Level)
Var. Cast Time: 2.0s
Summon a Lightning elemental ball that will float around you, and continuously drain SP while active.
The Lightning ball can later be thrown at an enemy using 2230.png Release, where it will deal Wind property magic damage to a single target.


A Maximum of 5 elemental balls can be summoned at a time.

These elemental balls can also be used for 2217.png Tetra Vortex to make one of the skills hits deal Wind property magic damage.


[Lv 1] : Summons 1 elemental ball, Duration 120 seconds.
[Lv 2] : Summons 5 elemental balls, Duration 280 seconds.
2224.png Summon Water Ball	Support	
Max Level: 5
Target: Self
SP Cost: 2 + (8 x Skill Level)
Var. Cast Time: 2.0s
Summon a Water elemental ball that will float around you, and continuously drain SP while active.
The Water ball can later be thrown at an enemy using 2230.png Release, where it will deal Water property magic damage to a single target.


A Maximum of 5 elemental balls can be summoned at a time.

These elemental balls can also be used for 2217.png Tetra Vortex to make one of the skills hits deal Water property magic damage.


[Lv 1] : Summons 1 elemental ball, Duration 120 seconds.
[Lv 2] : Summons 5 elemental balls, Duration 280 seconds.
2229.png Summon Stone	Support	
Max Level: 5
Target: Self
SP Cost: 2 + (8 x Skill Level)
Var. Cast Time: 2.0s
Summon an Earth elemental ball that will float around you, and continuously drain SP while active.
The Earth ball can later be thrown at an enemy using 2230.png Release, where it will deal Earth property magic damage to a single target.


A Maximum of 5 elemental balls can be summoned at a time.

These elemental balls can also be used for 2217.png Tetra Vortex to make one of the skills hits deal Earth property magic damage.


[Lv 1] : Summons 1 elemental ball, Duration 120 seconds.
[Lv 2] : Summons 5 elemental balls, Duration 280 seconds.
2230.png Release	Damage	
Max Level: 2
Target: Enemy
SP Cost:
(Lv 1) : 3
(Lv 2) : 20
Range: 11
Allows you to release stored magic, or fling elemental balls at targets.

Elemental ball damage is increased based on the casters Base Level, and Job Level.

[Lv 1] : Instantly cast a randomly selected spell that was stored with 2231.png Reading Spellbook. If there are no spells stored, use one elemental ball to strike a target.
[Lv 2] : Release all summoned elemental balls to strike a target with magic damage of the elemental ball type.
2231.png Reading Spellbook

## Equipment

## See also

- [NovaRO wiki - Warlock](https://www.novaragnarok.com/wiki/Warlock)
- [NovaRO wiki - Mayo's Warlock Guide](https://www.novaragnarok.com/wiki/Mayo%27s_Warlock_Guide)
- [iRO wiki - Warlock](https://irowiki.org/wiki/Warlock)
