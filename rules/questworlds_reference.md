# QuestWorlds Rules Reference

## Converting HeroQuest to QuestWorlds for The Red Cow

This document maps HeroQuest mechanics to QuestWorlds format for use in the interactive fiction conversion.

---

## Core Mapping

### Abilities vs. Keywords

| HeroQuest | QuestWorlds | Notes |
|----------|------------|-------|
| Ability Rating (1-20) | Ability Rating | Same scale |
| Keywords | Keywords | Group related abilities |
| Growth | Growth | Earn XP, improve abilities |

---

## QuestWorlds Contest System

### Standard Conflict Resolution

**Resolution**: Opposed roll using two d20s
- Character die: One player rolls their ability
- Resistance die: GM rolls an appropriate ability
- Compare results for narrative outcome

### Results Table

| Character Roll | Resistance Roll | Outcome |
|--------------|-------------|---------|
| Critical (20) | Any | Complete Victory |
| Success (11-19) | Fail | Victory |
| Success (11-19) | Success | Mixed Success |
| Fail (1-10) | Success | Mixed Defeat |
| Fumble (1) | Any | Complete Defeat |

### Target Numbers (Alternative)

For non-opposed tests:
- Simple: Roll ability or higher vs TN 11
- Challenging: TN 15
- Hard: TN 17
- Heroic: TN 19

---

## Combat Conversion

### HeroQuest Combat → QuestWorlds

| HeroQuest | QuestWorlds |
|----------|------------|
| Attack Strength | Weapon Ability |
| Defense | Shield/Protection Ability |
| Body Points | Endurance + Willpower |
| Mind Points | Willpower |

### Combat Procedure

1. **Declare Combatants**: Both name weapons/abilities
2. **Roll**: Attacker uses Weapon, Defender uses Defense
3. **Compare**: Standard contest resolution
4. **Apply Effects**:
   - Complete Victory: Full damage (see below)
   - Victory: Half damage
   - Mixed: No damage, exchange position
   - Defeat: Take half damage
   - Complete Defeat: Full damage taken

### Damage Guide

| Weapon Type | Damage Bonus |
|------------|------------|
| Unarmed | +0 |
| Dagger | +1 |
| Sword | +2 |
| Axe | +3 |
| Spear | +2 |
| Two-Handed | +3 |
| Bow | +2 |

---

## Ability Creation for Glorantha

### Storm Warrior Keyword

| Underlying Ability | Rating | Notes |
|-----------------|-------|-------|
| Spear Fighting | 17 | Primary weapon |
| Shield Wall | 16 | Defense |
| Battle Cry | 15 | Rally/Intimidate |
| Axe Mastery | 14 | Secondary |
| Fearless | 14 | Against magic/fear |

### Earth Cultist Keyword

| Underlying Ability | Rating | Notes |
|-----------------|-------|-------|
| Healing | 17 | Mending |
| Bless Crops | 16 | Fertility |
| Earth Magic | 15 | Communication |
| Midwifery | 14 | New life |
| Weather Sense | 12 | Reading sky |

### Storm Bull Champion

| Underlying Ability | Rating | Notes |
|-----------------|-------|-------|
| Berserker Rage | 17 | Fury ability |
| Wolf-Killing | 17 | Anti-Telmori |
| Chaos Sense | 15 | Detect corruption |
| Wild Hunt | 14 | Tracking |
| Iron Fury | 15 | Fight past wounds |

### Horse-Lord Keyword

| Underlying Ability | Rating | Notes |
|-----------------|-------|-------|
| Horse Mastery | 17 | All equestrian |
| Scout | 16 | Reconnaissance |
| Mounted Combat | 15 | Lance charges |
| Silent Movement | 15 | Stealth |
| Long Vision | 14 | Spotting |

### Sword Maiden Keyword

| Underlying Ability | Rating | Notes |
|-----------------|-------|-------|
| Sword Mastery | 17 | All blades |
| Truth Seeking | 16 | Detection |
| Severance | 15 | Breaking bonds |
| Dueling | 14 | Single combat |
| Disarm | 13 | Non-lethal |

---

## Faction Influence

### Using Factions in QuestWorlds

Factions provide narrative hooks:
- **Support**: Faction members may aid or hinder
- **Resources**: Access to faction wealth/contacts
- **Reputation**: Standing affects PC options

### Red Cow Factions Summary

| Faction | Resources | Requires | Blocks |
|---------|-----------|----------|--------|
| Free Sartar | Rebel network | Anti-Lunar | Moon Winds |
| Eye of the Hurricane | Peace, trade | Neutrality | Rebels |
| Conquering Storm | Warriors | Anti-Dinacoli | Dinacoli |
| Wolfskinners | Anti-wolf allies | Jomes alliance | Moon Winds |
| Moon Winds | Lunar favor | Imperial ties | Rebels |

---

## Monster/NPC Statistics

### Sample: Telmori Werewolf

| Attribute | Value |
|----------|-------|
| Combat Ability | 15 |
| Claw Attack | +2 |
| Tracking | 15 |
| Endurance | 14 |
| Armor | 0 (can be hit by enchanted) |

**Special**: Only enchanted weapons can harm in wolf form.

### Sample: Lunar Soldier

| Attribute | Value |
|----------|-------|
| Combat Ability | 14 |
| Spear | +2 |
| Shield | 14 |
| Discipline | 15 |

---

## Magic Conversion

### HeroQuest Runes → QuestWorlds Abilities

| Glorantha Rune | QuestWorlds Ability | Example |
|---------------|-------------------|--------|
| Air (Storm) | Weather Control | Storm Rider |
| Earth | Earth Magic | Stone Speaker |
| Water | Water Magic | Tide Walker |
| Death | Severance | Sword of Truth |
| Chaos | Chaos Resistance | Chaos Ward |

### QuestWorlds Magic (Abstract)

Magic is handled through **Ability contests**. No separate magic system.

- **Spellcasting**: Use Religious/Magical ability
- **Ritual**: Extended contest, multiple rolls
- **Divination**: Insight/Truth-seeking ability

---

## Campaign Resource Tracking

### Red Cow Clan Resources

| Resource | Starting | Notes |
|----------|----------|-------|
| Wealth (cattle) | 17 | Herd size |
| Warriors | 16 | Trained fighters |
| Magic | 15 | Temple strength |
| Reputation | 14 | Clan standing |
| Allies | 14 | Friend clans |

### Resource Tests

Each season, GM may call for Resource Tests:
- Roll appropriate ability for the Resource
- Failure: Resource decreases
- Success: Resource maintained

---

## Experience & Growth

### Earning Experience

- **Victory**: +1 XP
- **Major Success**: +2 XP
- **Learning**: +1 XP (failed attempt at new ability)

### Spending Experience

| Improvement | Cost |
|--------------|------|
| Increase ability by 1 | 3 XP |
| Learn new ability | 2 XP |
| New keyword slot | 4 XP |
| New flaw | 1 XP (benefits) |

---

## NPC Creation Guidelines

### Creating Red Cow NPCs

1. **Choose Role**: Thanage, Carl, Cottar
2. **Assign Keyword**: Based on role
3. **Set Primary Ability**: 13-15 for average, 16+ for exceptional
4. **Add Personalities**: 2-3 character abilities/flaws

### Sample NPCs

**Broddi Strong-Kin**: Chieftain
- Keyword: Orlanth Rex (16)
- Abilities: Command 16, Oratory 15, Loyalty 15

**Jogar Sog**: Telmori Warlord
- Keyword: Wolf Chief (16)
- Abilities: Wolf-Killing 16, Command 15, Barbarism 16