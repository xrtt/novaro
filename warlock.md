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

To reach zero Variable Cast Time with stats only, the following formula has to be used:

```
DEX × 2 + INT = 530 
```

## Skills

- [Skill simulator](https://irowiki.org/~himeyasha/skill4/wlk.html)
- [4th jobs](https://www.divine-pride.net/forum/index.php?/topic/4672-kro-fourth-class-jobs-skills-info-and-related-items-updated-16092020/&tab=comments#comment-8022)

### ![Reading Spellbook](https://static.divine-pride.net/images/skill/2231.png) Reading Spellbook

Max Level: 1
Target: Passive, Self
SP Cost: 40
Var. Cast Time: 5.0s
Fixed Cast Time: 1.0s
Cast Delay: 0.5s

Allows you to read Spell Books to store spells in your mind, letting you later use them with ![Release](https://static.divine-pride.net/images/skill/2230.png) Release to cast the spell instantly.

## Equipment

## See also

- [NovaRO wiki - Warlock](https://www.novaragnarok.com/wiki/Warlock)
- [NovaRO wiki - Mayo's Warlock Guide](https://www.novaragnarok.com/wiki/Mayo%27s_Warlock_Guide)
- [iRO wiki - Warlock](https://irowiki.org/wiki/Warlock)
