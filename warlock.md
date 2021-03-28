# Warlock

TODO:
[ ] Skill build
[ ] Equipment

## Content

- [Stats](#Stats)
- [Skills](#Skills)
- [Equipment](#Equipment)
- [References](#References)

## Stats

| `baseLvl` | 99 | 200 | `jobLvl` bonuses | 70 |
| --------- | -- | --- | :--------------: | -- |
| `STR`     | 1  | 1   | +                | 1  |
| `AGI`     | 1  | 90  | +                | 7  |
| `VIT`     | 60 | 90  | +                | 8  |
| `INT`     | 90 | 120 | +                | 15 |
| `DEX`     | 90 | 120 | +                | 8  |
| `LUK`     | 1  | 90  | +                | 4  |

> Note - To reach zero Variable Cast Time with stats only, the following formula has to be used:
>```
>DEX × 2 + INT = 530 
>```

## Skills

- [Skill simulator](https://irowiki.org/~himeyasha/skill4/wlk.html)
- [4th jobs](https://www.divine-pride.net/forum/index.php?/topic/4672-kro-fourth-class-jobs-skills-info-and-related-items-updated-16092020/&tab=comments#comment-8022)

### ![Radius](https://static.divine-pride.net/images/skill/2208.png) Radius

- Passive
- Max Level: 3

Increase the casting range of Warlock skills, and reduce their Fixed Casting Time as well.

- [Lv 1] : +1 Cell range, -10% Fixed Casting Time.
- [Lv 2] : +2 Cell range, -15% Fixed Casting Time.
- [Lv 3] : +3 Cell range, -20% Fixed Casting Time.

### ![Freezing Spell](https://static.divine-pride.net/images/skill/2232.png) Freezing Spell

- Passive
- Max Level: 10

Increase the number of Mind Slots available.

Mind Slots determine the amount of spells you can store using ![Reading Spellbook](https://static.divine-pride.net/images/skill/2231.png) Reading Spellbook.
You can find you total mind slots and currently held spells with the `@battlestats` command ingame.

- [Lv 1] : +8 Mind Slots.
- [Lv 2] : +16 Mind Slots.
- [Lv 3] : +24 Mind Slots.
- [Lv 4] : +32 Mind Slots.
- [Lv 5] : +40 Mind Slots.
- [Lv 6] : +48 Mind Slots.
- [Lv 7] : +56 Mind Slots.
- [Lv 8] : +64 Mind Slots.
- [Lv 9] : +72 Mind Slots.
- [Lv10] : +80 Mind Slots.

The formula to calculate mind slots is:

```
(Freezing Spell Level × 8) + Floor(Base Level ÷ 10) + Floor(Total INT ÷ 10)
```

Max you can have 7 spells in mind.

| `freezingSpell` | `baseLvl` | `INT` | Total | Superior (12) | Ultimate (22) |
| --------------- | --------- | ----- | ----- | ------------- | ------------- |
| 0               | 200       | 120   | 32    | 2             | 1             |
| 1               | 200       | 120   | 40    | 3 (+1)        | 1             |
| 2               | 200       | 120   | 48    | 4 (+1)        | 2 (+1)        |
| 3               | 200       | 120   | 56    | 4             | 2             |
| 4               | 200       | 120   | 64    | 5 (+1)        | 2             |
| 5               | 200       | 120   | 72    | 6 (+1)        | 3 (+1)        |
| 6               | 200       | 120   | 80    | 6             | 3             |
| 7               | 200       | 120   | 88    | 7 (+1)        | 4 (+1)        |
| 8               | 200       | 120   | 96    | 7             | 4             |
| 9               | 200       | 120   | 104   | 7             | 4             |
| 10              | 200       | 120   | 112   | 7             | 5 (+1)        |

### ![Reading Spellbook](https://static.divine-pride.net/images/skill/2231.png) Reading Spellbook

- Max Level: 1
- Target: Passive, Self
- SP Cost: 40
- Var. Cast Time: 5.0s
- Fixed Cast Time: 1.0s
- Cast Delay: 0.5s

Allows you to read Spell Books to store spells in your mind, letting you later use them with ![Release](https://static.divine-pride.net/images/skill/2230.png) Release to cast the spell instantly.

### ![Release](https://static.divine-pride.net/images/skill/2230.png) Release

- Max Level: 2
- Target: Enemy
- SP Cost:
  - (Lv 1) : 3
  - (Lv 2) : 20
- Range: 11

Allows you to release stored magic, or fling elemental balls at targets.

Elemental ball damage is increased based on the casters Base Level, and Job Level.

- [Lv 1] : Instantly cast a randomly selected spell that was stored with ![Reading Spellbook](https://static.divine-pride.net/images/skill/2231.png) Reading Spellbook. If there are no spells stored, use one elemental ball to strike a target.
- [Lv 2] : Release all summoned elemental balls to strike a target with magic damage of the elemental ball type.

### ![Summon Fire Ball](https://static.divine-pride.net/images/skill/2222.png) Summon Fire Ball

- Max Level: 2
- Target: Self
- SP Cost: 2 + (8 x Skill Level)
- Var. Cast Time: 2.0s

Summon a Fire elemental ball that will float around you, and continuously drain SP while active.
The Fire ball can later be thrown at an enemy using ![Release](https://static.divine-pride.net/images/skill/2230.png) Release, where it will deal Fire property magic damage to a single target.

A Maximum of 5 elemental balls can be summoned at a time.
These elemental balls can also be used for ![Tetra Vortex](https://static.divine-pride.net/images/skill/2222.png) Tetra Vortex to make one of the skills hits deal Fire property magic damage.

- [Lv 1] : Summons 1 elemental ball, Duration 120 seconds.
- [Lv 2] : Summons 5 elemental balls, Duration 280 seconds.

### ![Recognized Spell](https://static.divine-pride.net/images/skill/2206.png) Recognized Spell

- Max Level: 5
- Target: Self
- SP Cost: 80 + (20 x Skill Level)
- Var. Cast Time: 1.0s
- Fixed Cast Time: 1.0s
- Cast Delay: 1.0s
- Cool Down: 20s + (30 x Skill Level)

Increase you damage capabilities by always using the highest possible MATK variance, letting you deal the maximum amount of magical damage every time you cast a skill.
However, it also increases the SP Consumption of all skills by 25%.

- [Lv 1] : Duration 60 seconds.
- [Lv 2] : Duration 90 seconds.
- [Lv 3] : Duration 120 seconds.
- [Lv 4] : Duration 150 seconds.
- [Lv 5] : Duration 180 seconds.

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

- [Lv 1] : 1300% MATK.
- [Lv 2] : 1900% MATK.
- [Lv 3] : 2500% MATK.
- [Lv 4] : 3100% MATK.
- [Lv 5] : 3700% MATK.

Damage is based on the following formula:

```
Damage (MATK) = [{Base_Damage × (BaseLevel ÷ 100)}]%
```

### ![Comet](https://static.divine-pride.net/images/skill/2213.png) Comet
	
- Max Level: 5
- Target: Ground
- SP Cost: 400 + (80 x Skill Level)
- Var. Cast Time: 5s + (Skill Level)
- Fixed Cast Time: 2.0s
- Cast Delay: 1.5s
- Cool Down: 20.0s
- Range: 11

Drop a massive 13x13 Comet from the depths of space, dealing Neutral property magic damage to all enemies in range.
All targets hit will also receive 'Magic Intoxication' status for 20 seconds. While under this status targets will have -50% resistance to All Properties of attacks.

This skills damage is increased based on the casters Base Level.

- [Lv 1] : 3200% MATK.
- [Lv 2] : 3900% MATK.
- [Lv 3] : 4600% MATK.
- [Lv 4] : 5300% MATK.
- [Lv 5] : 6000% MATK.

Damage is based on the following formula:

```
Damage (MATK) = [(Base_Damage × Base_Level ÷ 100)]%
```

### ![Tetra Vortex](https://static.divine-pride.net/images/skill/2217.png) Tetra Vortex

- Max Level: 10
- Target: Enemy
- SP Cost: 90 + (30 x Skill Level)
- Var. Cast Time: 4s + (Skill Level)
- Fixed Cast Time: 2.0s
- Cast Delay: 2.0s
- Cool Down: 15.0s
- Range: 11

Strike a small area around a target with the power of the core elements. This damage is divided into 4 hits, each hit will take the elemental property from on of the consumed elemental balls used to cast the skill.

This spell requires you to have 4 elemental balls summoned, and consumes them all on cast.

You can mix the elements of this spell,
For example if you used Fire, Fire, Water, Wind element balls to cast the spell, it would deal Fire damage on the first and second hit, Water damage on the third, and Wind on the fourth hit.

- [Lv 1] : 1200% MATK per hit, 1x1 Area of effect.
- [Lv 2] : 1600% MATK per hit, 1x1 Area of effect.
- [Lv 3] : 2000% MATK per hit, 1x1 Area of effect.
- [Lv 4] : 2400% MATK per hit, 1x1 Area of effect.
- [Lv 5] : 2800% MATK per hit, 1x1 Area of effect.
- [Lv 6] : 3200% MATK per hit, 3x3 Area of effect.
- [Lv 7] : 3600% MATK per hit, 3x3 Area of effect.
- [Lv 8] : 4000% MATK per hit, 5x5 Area of effect.
- [Lv 9] : 4400% MATK per hit, 5x5 Area of effect.
- [Lv10] : 4800% MATK per hit, 7x7 Area of effect.

Each element of Tetra Vortex also has a chance to apply a different status effect on the target.

- [Fire Element] -- Burning status
- [Wind Element] -- Stun status
- [Water Element] -- Freezing status
- [Earth Element] -- Bleeding status

## Equipment

- [Temporal Boots](https://www.novaragnarok.com/wiki/Temporal_Boots)
- [Illusion Equipments and Enchants (17.1)](https://www.novaragnarok.com/wiki/Illusion_Equipments_and_Enchants_(17.1))
- [Automatic Equipments and Enchants (17.2)](https://www.novaragnarok.com/wiki/Automatic_Equipments_and_Enchants_(17.2))
- [Edda Bioresearch Laboratory Equip](https://www.novaragnarok.com/wiki/Bioresearch_Laboratory#Equipment)
- [Odin's Temple 4 / Odin's Past Equip (Soutanes)](https://www.novaragnarok.com/wiki/Odin%27s_Temple_4_/_Odin%27s_Past#Obtainable_Equipment)
- [Einbech Dungeon 3 Equip](https://www.novaragnarok.com/wiki/Einbech_Dungeon_3#Obtainable_Equipment)
- [Abyss Dungeon 4 Equip (Dragon Plates)](https://www.novaragnarok.com/wiki/Abyss_Dungeon_4#Obtainable_Equipment)
- [Sky Fortress Equip (Vicious Weapons)](https://www.novaragnarok.com/wiki/Sky_Fortress#Vicious_Weapons)
- [Fall of Glast Heim Equip (King Schmidt's Set)](https://www.novaragnarok.com/wiki/Fall_of_Glast_Heim#Equipment)
- [Tomb of the Fallen Equip (Old Classes' Headgears)](https://www.novaragnarok.com/wiki/Tomb_of_the_Fallen#Rewards_and_Equipment_Crafting)
- [Legacy of Glast Heim Equip (Temporal Stat Manteaus)](https://www.novaragnarok.com/wiki/Temporal_Stat_Manteaus)
- [Cards (17.2)](https://www.novaragnarok.com/wiki/Cards_(17.2))

## References

- General
	- [NovaRO wiki - Warlock](https://www.novaragnarok.com/wiki/Warlock)
	- [NovaRO wiki - Mayo's Warlock Guide](https://www.novaragnarok.com/wiki/Mayo%27s_Warlock_Guide)
	- [iRO wiki - Warlock](https://irowiki.org/wiki/Warlock)
	- [Skill Rebalance Patch](https://www.novaragnarok.com/forum/news/skill-rebalance-patch-100-r231/)
	- [3rd Job Improvement Patch](https://www.novaragnarok.com/forum/news/kro-job-improvement-patch-notes-155-r331/)
- Skills
	- [Skill simulator](https://irowiki.org/~himeyasha/skill4/wlk.html)
	- [4th jobs](https://www.divine-pride.net/forum/index.php?/topic/4672-kro-fourth-class-jobs-skills-info-and-related-items-updated-16092020/&tab=comments#comment-8022)
- Equipment
	- [Temporal Boots](https://www.novaragnarok.com/wiki/Temporal_Boots)
	- [Illusion Equipments and Enchants (17.1)](https://www.novaragnarok.com/wiki/Illusion_Equipments_and_Enchants_(17.1))
	- [Automatic Equipments and Enchants (17.2)](https://www.novaragnarok.com/wiki/Automatic_Equipments_and_Enchants_(17.2))
	- [Edda Bioresearch Laboratory Equip](https://www.novaragnarok.com/wiki/Bioresearch_Laboratory#Equipment)
	- [Odin's Temple 4 / Odin's Past Equip (Soutanes)](https://www.novaragnarok.com/wiki/Odin%27s_Temple_4_/_Odin%27s_Past#Obtainable_Equipment)
	- [Einbech Dungeon 3 Equip](https://www.novaragnarok.com/wiki/Einbech_Dungeon_3#Obtainable_Equipment)
	- [Abyss Dungeon 4 Equip (Dragon Plates)](https://www.novaragnarok.com/wiki/Abyss_Dungeon_4#Obtainable_Equipment)
	- [Sky Fortress Equip (Vicious Weapons)](https://www.novaragnarok.com/wiki/Sky_Fortress#Vicious_Weapons)
	- [Fall of Glast Heim Equip (King Schmidt's Set)](https://www.novaragnarok.com/wiki/Fall_of_Glast_Heim#Equipment)
	- [Tomb of the Fallen Equip (Old Classes' Headgears)](https://www.novaragnarok.com/wiki/Tomb_of_the_Fallen#Rewards_and_Equipment_Crafting)
	- [Legacy of Glast Heim Equip (Temporal Stat Manteaus)](https://www.novaragnarok.com/wiki/Temporal_Stat_Manteaus)
	- [Cards (17.2)](https://www.novaragnarok.com/wiki/Cards_(17.2))
	- Crostlock
		- [Equip](https://github.com/xrtt/novaro/blob/main/screenNovaRO068.jpg)
		- [Headgear (T)](https://github.com/xrtt/novaro/blob/main/screenNovaRO069.jpg)
		- [Headgear (T)](https://github.com/xrtt/novaro/blob/main/screenNovaRO070.jpg)
		- [Headgear (T)](https://github.com/xrtt/novaro/blob/main/screenNovaRO071.jpg)
		- [Headgear (M)](https://github.com/xrtt/novaro/blob/main/screenNovaRO072.jpg)
		- [Headgear (B)](https://github.com/xrtt/novaro/blob/main/screenNovaRO073.jpg)
		- [Armor](https://github.com/xrtt/novaro/blob/main/screenNovaRO074.jpg)
		- [Weapon](https://github.com/xrtt/novaro/blob/main/screenNovaRO075.jpg)
		- [Back](https://github.com/xrtt/novaro/blob/main/screenNovaRO076.jpg)
		- [Footgear](https://github.com/xrtt/novaro/blob/main/screenNovaRO077.jpg)
		- [Accessory (Left)](https://github.com/xrtt/novaro/blob/main/screenNovaRO078.jpg)
