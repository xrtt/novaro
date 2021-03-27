# Warlock

TODO:
[ ] Skill build
[ ] Equipment

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

To reach zero Variable Cast Time with stats only, the following formula has to be used:

```
DEX × 2 + INT = 530 
```

## Skills

- [Skill simulator](https://irowiki.org/~himeyasha/skill4/wlk.html)
- [4th jobs](https://www.divine-pride.net/forum/index.php?/topic/4672-kro-fourth-class-jobs-skills-info-and-related-items-updated-16092020/&tab=comments#comment-8022)

### ![Reading Spellbook](https://static.divine-pride.net/images/skill/2231.png) Reading Spellbook

- Max Level: 1
- Target: Passive, Self
- SP Cost: 40
- Var. Cast Time: 5.0s
- Fixed Cast Time: 1.0s
- Cast Delay: 0.5s

Allows you to read Spell Books to store spells in your mind, letting you later use them with ![Release](https://static.divine-pride.net/images/skill/2230.png) Release to cast the spell instantly.

### ![Summon Fire Ball](https://static.divine-pride.net/images/skill/2222.png) Summon Fire Ball

- Max Level: 2
- Target: Self
- SP Cost: 2 + (8 x Skill Level)
- Var. Cast Time: 2.0s

Summon a Fire elemental ball that will float around you, and continuously drain SP while active.
The Fire ball can later be thrown at an enemy using ![Release](https://static.divine-pride.net/images/skill/2230.png) Release, where it will deal Fire property magic damage to a single target.

A Maximum of 5 elemental balls can be summoned at a time.
These elemental balls can also be used for ![Tetra Vortex](https://static.divine-pride.net/images/skill/2222.png) Tetra Vortex to make one of the skills hits deal Fire property magic damage.

[Lv 1] : Summons 1 elemental ball, Duration 120 seconds.
[Lv 2] : Summons 5 elemental balls, Duration 280 seconds.

### ![Crimson Rock](https://static.divine-pride.net/images/skill/2211.png) Crimson Rock

- Max Level: 5
- Target: Enemy
- SP Cost: 50 + (10 x Skill Level)
- Var. Cast Time: 5.0s
- Fixed Cast Time: 1.0s
- Cast Delay: 0.5s
- Cool Down: 5.0s
- Range: 11

Call forth a large meteor to strike a target and all enemies in a 7x7 surrounding area, dealing Fire property magic damage.
All targets hit by the meteor will be knocked back 3 cells.


This skills damage is increased based on the casters Base Level.

[Lv 1] : 1300% MATK.
[Lv 2] : 1900% MATK.
[Lv 3] : 2500% MATK.
[Lv 4] : 3100% MATK.
[Lv 5] : 3700% MATK.

Damage is based on the following formula:

```
Damage (MATK) = [{Base_Damage × (BaseLevel ÷ 100)}]%
```

## Equipment

- [Illusion Equipments and Enchants (17.1)](https://www.novaragnarok.com/wiki/Illusion_Equipments_and_Enchants_(17.1))
- [Automatic Equipments and Enchants (17.2)](https://www.novaragnarok.com/wiki/Automatic_Equipments_and_Enchants_(17.2))
- [Cards (17.2)](https://www.novaragnarok.com/wiki/Cards_(17.2))
- [Edda Bioresearch Laboratory Equip](https://www.novaragnarok.com/wiki/Bioresearch_Laboratory#Equipment)
- [Odin's Temple 4 / Odin's Past Equip](https://www.novaragnarok.com/wiki/Odin%27s_Temple_4_/_Odin%27s_Past#Obtainable-Equipment)
- 

## See also

- [NovaRO wiki - Warlock](https://www.novaragnarok.com/wiki/Warlock)
- [NovaRO wiki - Mayo's Warlock Guide](https://www.novaragnarok.com/wiki/Mayo%27s_Warlock_Guide)
- [iRO wiki - Warlock](https://irowiki.org/wiki/Warlock)
