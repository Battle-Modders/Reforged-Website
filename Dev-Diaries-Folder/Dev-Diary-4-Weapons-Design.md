**Dev Diary #4 - 07-Sep-2024**\
_LordMidas_

* [Vision](#vision)
    * [Double Grip Rework](#double-grip-rework)
    * [Weapon Specialization Progression](#weapon-specialization-progression)
    * [Hybrid Weapons](#hybrid-weapons)
* [Axes](#axes)
* [Bows](#bows)
* [Cleavers](#cleavers)
    * [Bleeding Rework](#bleeding-rework)
* [Daggers](#daggers)
* [Flails](#flails)
* [Hammers](#hammers)
* [Maces](#maces)
* [Polearms](#polearms)
    * [Crowded mechanic](#crowded-mechanic)
* [Spears](#spears)
* [Swords](#swords)
* [Throwing Weapons](#throwing-weapons)

## Vision
Our goal is to make every weapon type in the game competitive and viable. This does *not* mean that the weapons become equitable in terms of their damage output, but rather that they each feel useful and there are compelling reasons to use each weapon type in various circumstances. Far more builds and company setups can be created in Reforged with a variety of characters and weapons. This works in tandem with our dynamic perks system through which various perks from non-weapon perk groups provide opportunities for new combos and builds. At the same time each weapon type should have its own character and theme which makes it stand out from others. Our design for each weapon, and its associated perks, follows our vision about the theme of the weapon, how it would be used in real life, and what role it can fulfil within the game.

We achieve these goals through each weapon having access to certain weapon-type exclusive perks which unlock special mechanics. A core guiding principle in our design has been that the perks should be thematic and original, ideally unlocking new mechanics, instead of simple stat buffs. Finally, the power level of these perks is not necessarily symmetric across weapon types because the weapon types themselves have an asymmetric strength and that must be taken into account.

### Double Grip Rework
Unlike the universal Double Grip bonus of 25% more damage in vanilla, each weapon type in Reforged has a unique double grip bonus. This adds depth and character to each weapon type and fits better within our overall design space considering the Reach mechanic and our rework of the Duelist perk granting bonuses for certain two-handed weapons. In this new space, these asymmetric double grip bonuses give the one-handed weapons their own charm and competitive edge.

### Weapon Specialization Progression
Each weapon now has a 3-perk progression system where each perk unlocks special bonuses.
- The first perk may exist on tier 1 to tier 3 of the perk tree, depending on weapon type.
- The second perk exists on tier 4 and is the mastery perk.
- The third perk may exist on tier 5 to tier 7 of the perk tree, depending on weapon type.

The tier 4 mastery perks in particular have received special treatment in Reforged to make them more meaningful and truly represent mastery of that weapon type. This is achieved by unlocking special mechanics through these perks. The three perks of a weapon's perk group usually have synergies with each other, but you do not need to learn all 3 for every build.

### Hybrid Weapons
In vanilla, weapon mastery applies its bonuses to skills instead of weapons so for example the Batter skill of Axehammer gets the 25% Fatigue Cost reduction from Hammer Mastery whereas the Split Shield skill of the same weapon gets the fatigue cost reduction from Axe Mastery. This leaves hybrid weapons in a weird state.

In Reforged, each weapon has a list of Applicable Masteries and if you have any one of these masteries, all the skills of that weapon are considered mastered and receive the mastery benefits. We have also added several new hybrid weapons in Reforged e.g. the Kriegsmesser, Two-Handed Falchion and Halberd.

## Axes
Effective against both armor and flesh, axes deal a large amount of damage and can inflict debilitating injuries. The shape of their blade provides opportunites for certain clever techniques.

### Double Grip
When double gripped, axes deal more damage and more armor penetrating damage.

### Axe Perks

| Icon | Name | Description |
| :--: | :--: | :--: |
| ![[assets/images/perks/perk_rf_dismemberment.png]] | **Dismemberment** | Allows axes to deal severe injuries, while greatly testing the Resolve of the target. |
| ![[assets/images/perks/perk_mastery_axe.png]] | **Axe Mastery** | In addition to vanilla behavior, unlocks two new skills with axes: Hook Shield and Bearded Blade.<br>![[assets/images/skills/rf_hook_shield_skill.png]]<br>**Hook Shield**<br>Allows you to hook a target's shield until their next turn, greatly reducing their shield's effectiveness.<br>![[assets/images/skills/rf_bearded_blade_skill.png]]<br>**Bearded Blade**<br>Allows you to Disarm your opponents using the bearded blade of your axe, either when you attack them or when they attack you. |
| ![[assets/images/perks/perk_rf_dismantle.png]] | **Dismantle** | Allows attacks from axes to chop off pieces of the target's armor causing the target to receive more damage ignoring armor from all sources for the remainder of the combat. |

## Bows
Bows can deal a large amount of damage from afar and are much faster than their slower Crossbow cousins, but are fatiguing to use and require high skill.

### Bow Perks

| Icon | Name | Description |
| :--: | :--: | :--: |
| ![[assets/images/perks/perk_rf_target_practice.png]] | **Target Practice** | Makes it easier to hit exposed targets or to exert ranged supermacy over ranged enemies. |
| ![[assets/images/perks/perk_mastery_bow.png]] | **Bow Mastery** | In addition to vanilla behavior, unlocks the Arrow to the Knee skill.<br>![[assets/images/skills/rf_arrow_to_the_knee_skill.png]]<br>**Arrow to the Knee**<br>Debilitate a target's ability to move and defend themselves. |
| ![[assets/images/perks/perk_rf_trick_shooter.png]] | **Trick Shooter** | Unlocks the Hip Shooter and Flaming Arrows perks.<br>![[assets/images/perks/perk_rf_hip_shooter.png]]<br>**Hip Shooter**<br>Reduces the Action Point cost of Quick Shot but makes subsequent Quick Shots more fatiguing.<br>![[assets/images/perks/perk_rf_flaming_arrows.png]]<br>**Flaming Arrows**<br>Aimed Shot now shoots flaming arrows which deal additional burning damage and light the tile on fire. |

## Cleavers
Sharp, top-heavy blades specialized to slice through flesh and deliver deep cuts.

### Double Grip
When double gripped, cleavers deal more damage.

### Bleeding Rework
Bleeding in vanilla is in a weird place because applying it as a player on enemies doesn't feel good enough as the damage comes too late and it would've been better to simply use a higher damage weapon in the first place. And receiving Bleeding from enemies on your brothers is problematic because in certain cases the damage is too high at end of your next turn and you may not even have the opportunity to get that bro out of zone of control to use bandages.

In Reforged we have reworked Bleeding:
- Bleeding now stacks within a single instance of the effect on the character.
- Each stack of Bleeding does 1 damage, but does not expire (so it lasts the entire combat) unless bandaged.
- Each stack of Bleeding also reduces the character's Resolve and Initiative and this reduction is stronger at lower current Hitpoints.
- If you receive at least 3 stacks of Bleeding in a single turn, you immediately receive a Morale Check.

This allows players to inflict Bleeding on enemies and immediately benefit from it in terms of the enemy being more susceptible to dropping morale (reduced morale reduces their combat attributes). It also makes the character slower in Initiative so you have an opportunity to go before them in the next round. On the receiving end, players get a longer period of time to get the brother to a state where they can bandage the bleeding, and for minor bleeding perhaps even ignore it until the end of combat.

### Cleaver Perks

| Icon | Name | Description |
| :--: | :--: | :--: |
| ![[assets/images/perks/perk_rf_sanguinary.png]] | **Sanguinary** | Recover some Action Points up to two times per turn when you inflict fatalities - allowing you to continue the carnage. |
| ![[assets/images/perks/perk_mastery_cleaver.png]] | **Cleaver Mastery** | Similar to vanilla behavior except it now inflicts an additional stack of Bleeding instead of increasing the damage from Bleeding. Also grants the Bloodlust perk.<br>![[assets/images/perks/perk_rf_bloodlust.png]]<br>**Bloodlust**<br>Upon inflicting a fatality, Initiative, Resolve and Fatigue Recovery are greatly increased - slowly reducing over time. |
| ![[assets/images/perks/perk_rf_mauler.png]] | **Mauler** | Attacks from cleavers inflict additional bleeding and, when attacking targets who are sufficiently bleeding, inflict an extra injury ignoring any injury threshold. |

## Crossbows
Much easier, albeit slower, to use than Bows - crossbows are accurate and pack a punch.

### Crossbow Perks

| Icon | Name | Description |
| :--: | :--: | :--: |
| ![[assets/images/perks/perk_rf_power_shot.png]] | **Power Shot** | Attacks from crossbows have a chance to stagger the target. |
| ![[assets/images/perks/perk_mastery_crossbow.png]] | **Crossbow Mastery** | Reduces the AP cost of reloading Handgonne and Heavy Crossbow (which has a higher reload AP cost in Reforged). No longer has the +20% armor penetration as in vanilla (instead you get something like that from Bullseye now). Unlocks the Take Aim skill.<br>![[assets/images/skills/rf_take_aim_skill.png]]<br>**Take Aim**<br>Allows your next crossbow shot to ignore any penalty from blocked line of sight and your shot cannot go astray. For handgonnes allows you to choose to attack farther or to spray more tiles. |
| ![[assets/images/perks/perk_rf_iron_sights.png]] | **Iron Sights** | Increases the chance to hit the head with crossbows and handgonnes, and handgonnes now apply the Shellshocked effect upon a headshot. |

## Daggers
Primarily intended as sidearms, daggers represent the ideal weapon of choice to puncture through armored opponents. Owing to their small size, they are difficult to close the gap with, but once you get within the opponent's guard, you can quickly stab them to death.

### Double Grip
When double gripped, daggers deal more damage and you gain a portion of your Initiative as additional defense against opponents who act after you in a round.

### Daggers Perks

| Icon | Name | Description |
| :--: | :--: | :--: |
| ![[assets/images/perks/perk_rf_between_the_ribs.png]] | **Between the Ribs** | Deal more damage to surrounded opponents. |
| ![[assets/images/perks/perk_mastery_dagger.png]] | **Dagger Mastery** | In addition to vanilla behavior now allows you to ignore any Reach Disadvantage you may have when attacking an opponent who acts after you in the current round. |
| ![[assets/images/perks/perk_rf_swift_stabs.png]] | **Swift Stabs** | Reduces the Action Point cost of dagger attacks against the same target even further after having made a successful attack. |

## Flails
Confusing and unpredictable, the flail head can arrive at you from any direction. You better wear a sturdy helmet and have good luck.

### Double Grip
When double gripped, flails have additional chance to hit the head and deal more armor penetrating damage.

### Flail Perks

| Icon | Name | Description |
| :--: | :--: | :--: |
| ![[assets/images/perks/perk_rf_whirling_death.png]] | **Whirling Death** | Allows you to leverage your Reach to hit multiple opponents with the swinging head of your one-handed flail or to find a better chance to hit the head of your target with a two-handed one. |
| ![[assets/images/perks/perk_mastery_flail.png]] | **Flail Mastery** | In addition to vanilla behavior, grants the From all Sides perk.<br>![[assets/images/perks/perk_rf_from_all_sides.png]]<br>**From all Sides**<br>Targets you hit with your flail have temporarily reduced defenses, especially if you hit them on the head. |
| ![[assets/images/perks/perk_rf_flail_spinner.png]] | **Flail Spinner** | Your attacks have a chance to do an extra attack of the same type for free, albeit with reduced damage. |

## Hammers
Short in length but specialized to deliver painful blunt strikes - that are felt even through the thickest of armor.

### Double Grip
When double gripped, hammers deal more damage and skills build less fatigue.

### Hammer Perks

| Icon | Name | Description |
| :--: | :--: | :--: |
| ![[assets/images/perks/perk_rf_rattle.png]] | **Rattle** | Your attacks rattle the target to their bones, reducing their Reach temporarily. |
| ![[assets/images/perks/perk_mastery_hammer.png]] | **Hammer Mastery** | In addition to vanilla behavior, unlocks the Pummel skill and the ability to Dent Armor.<br>![[assets/images/skills/rf_pummel_skill.png]]<br>**Pummel**<br>Two-Handed hammers can attack, push back an opponent, and move into their tile, all in one action.<br>![[assets/images/perks/perk_rf_dent_armor.png]]<br>**Dent Armor**<br>Abilities which target armor e.g. Demolish Armor also apply the Dented Armor effect reducing the target's combat abilities for the remainder of the battle. |
| ![[assets/images/perks/perk_rf_deep_impact.png]] | **Deep Impact** | Allows you to target the most vulnerable parts of your opponent with a blunt strike that reduces their ability to deal damage for a turn. |

## Maces
Powerful blunt weapons that can truly knock the wind out of an opponent.

### Double Grip
When double gripped, maces deal more damage and apply the Dazed effect.

### Mace Perks

| Icon | Name | Description |
| :--: | :--: | :--: |
| ![[assets/images/perks/perk_rf_concussive_strikes.png]] | **Concussive Strikes** | Causes hits to the head to daze or stun opponents even with regular attacks. |
| ![[assets/images/perks/perk_mastery_mace.png]] | **Mace Mastery** | In addition to vanilla behavior, grants the Bear Down perk.<br>![[assets/images/perks/perk_rf_bear_down.png]]<br>**Bear Down**<br>You have increased chance to hit and chance to inflict injuries against targets suffering from negative status effects. |
| ![[assets/images/perks/perk_rf_bone_breaker.png]] | **Bone Breaker** | Attacks that stun a target or are already against stunned or rooted targets inflict a guaranteed injury on top of any injury inflicted by the attack. |

## Polearms
Long weapons to take out opponents whose last wish was to get closer to you. Note: Polearm perks, with the exception of Long Reach, work with all 2-tile weapons.

### Crowded Mechanic
Polearms are long weapons and difficult to use without sufficient space. Therefore melee attacks which can be used at 2 tiles now gain -5% chance to hit per ally next to you (ignoring the first 2 allies, so it starts from the 3rd ally onwards) and -10% per enemy next to you. This means polearm placement on the battlefield needs more thought and closing the gap with enemy polearms is an effective way of reducing their offensive capabilities.

### Polearm Perks

| Icon | Name | Description |
| :--: | :--: | :--: |
| ![[assets/images/perks/perk_rf_leverage.png]] | **Leverage** | Attacks against targets at 2 tiles distance have a higher chance to hit the head. |
| ![[assets/images/perks/perk_mastery_polearm.png]] | **Polearm Mastery** | In addition to vanilla behavior, reduces the AP cost of all 2 tile attacks irrespective of weapon type. Also grants the Bolster perk.<br>![[assets/images/perks/perk_rf_bolster.png]]<br>**Bolster**<br>Use your big weapon to make your allies feel stronger, based on how skilled you are with your weapon. Trigger positive morale checks for adjacent allies whenever you attack. |
| ![[assets/images/perks/perk_rf_long_reach.png]] | **Long Reach** | Enemies at 2 tile range are considered surrounded by you. |

## Spears
Considered by many to be the king of all weapons, the spear is an easy to use but highly effective weapon.

### Double Grip
When double gripped, spears have longer Reach and deal more damage and more armor penetrating damage. Thrust can be used on targets up to 2 tiles away but with reduced chance to hit if there's something in between.

### Spear Perks

| Icon | Name | Description |
| :--: | :--: | :--: |
| ![[assets/images/perks/perk_rf_through_the_gaps.png]] | **Through the Gaps** | The first attack each turn targets the body part with the lowest armor and deals additional damage ignoring armor. |
| ![[assets/images/perks/perk_mastery_spear.png]] | **Spear Mastery** | In addition to vanilla behavior, reduces the AP cost of Spearwall. Also the first attack each turn from a spear costs no Action Points and builds no Fatigue but deals reduced damage. |
| ![[assets/images/perks/perk_rf_king_of_all_weapons.png]] | **King of all Weapons** | Reduces the Action Point cost of all spear attacks and the first attack each turn deals increased damage. |

## Swords
Versatile and swift, fighting with a sword allows you to swiftly and gracefully move around the battlefield while skillfully punishing missed attacks against you.

### Double Grip
- Regular swords: When double gripped deal more damage and more armor penetrating damage and skills build less fatigue.
- Southern swords: When double gripped deal more damage.
- Fencing swords: When double gripped deal more armor penetrating damage.

### Sword Perks

| Icon | Name | Description |
| :--: | :--: | :--: |
| ![[assets/images/perks/perk_rf_tempo.png]] | **Tempo** | Build upon the advantage of going first in the flow of battle. Every attack increases your Initiative and when hitting those who act after you in a round, you recover Action Points. |
| ![[assets/images/perks/perk_mastery_sword.png]] | **Sword Mastery** | In addition to vanilla behavior, unlocks the Kata Step skill.<br>![[assets/images/skills/rf_kata_step_skill.png]]<br>**Kata Step**<br>Immediately after a successful attack you may move one tile ignoring zone of control as long as the tile being moved to is next to an enemy. |
| ![[assets/images/perks/perk_rf_en_garde.png]] | **En Garde** | Retain the double grip bonus with southern swords even with something in your offhand weighing less than 10. As long as you have at least 15 fatigue remaining, ending your turn will trigger Riposte for free if you have Riposte available. If you don't have Riposte and are wielding a two-handed sword you gain the Rebuke effect instead. |

## Throwing Weapons
Specialize as a thrower to deal high damage at short range, or train to become a hybrid fighter utilizing both throwing and melee weapons.

### Throwing Perks

| Icon | Name | Description |
| :--: | :--: | :--: |
| ![[assets/images/perks/perk_rf_hybridization.png]] | **Hybridization** | Gain a portion of your Ranged Skill as Melee Skill and of your Melee Skill as Ranged Skill. Also allows swapping to/from a throwing weapon for free once per turn. |
| ![[assets/images/perks/perk_mastery_throwing.png]] | **Throwing Mastery** | In addition to vanilla behavior, throwing attacks now apply unique status effects depending on the type of throwing weapon used. Some stun, others pin the opponent, yet others overwhelm them. |
| ![[assets/images/perks/perk_rf_opportunist.png]] | **Opportunist** | The first few throws in a combat cost fewer Action Points. When stepping over an enemy's corpse, recover ammo and Action Points. |
