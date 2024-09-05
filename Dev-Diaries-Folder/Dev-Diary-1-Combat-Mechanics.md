**Dev Diary #1 - 05-Sep-2024**\
_LordMidas_

* [Reach](#reach)
* [Shields](#shields)
* [One-Handed Weapons](#one-handed-weapons)
* [Other Changes](#other-changes)

Battle Brothers: Reforged contains multiple new and reworked combat mechanics to create a more engaging experience. This dev diary gives an overview of our design philosophy for three of these mechanics: Shields, One-Handed Weapons and the brand new Reach mechanic.

# Reach
## Concept
In real-life melee combat, longer weapons generally grant the user an advantage against opponents with shorter weapons. This is known as “Reach Advantage” and is a very significant factor in melee combat. This is because, if your intent is to hit your opponent, you must get the opponent within range of your weapon - and if the opponent has a longer reach than you, they can hit you first. This makes it easier for that opponent to hit you, while making it harder for you to hit them.

While the combat system in Battle Brothers does a great job of depicting medieval combat, it lacks an appreciation of this fundamental concept. We believe that adding this nuance deepens the tactical layer of the combat - emphasizing positioning, match-ups, and crowd control. Therefore, in Reforged, we have designed a brand new “Reach” mechanic to reflect this aspect of melee combat.
 
## How It Works
<img src="https://user-images.githubusercontent.com/55047920/223836039-1c368b85-0815-4b51-b830-fb3ea29c3868.jpg" alt="Shows Reach Advantage giving extra chance-to-hit during an attack." align="right" width="35%"/>
Each character now has a “Reach” property which is an abstraction of the Reach Advantage concept. Characters with higher Reach gain or lose chance-to-hit during an attack depending on the difference in Reach between the attacker and defender. Reach can be modified by a character’s race, traits, perks, status effects and equipment (every weapon has its own Reach stat) etc.

* During a melee attack, chance-to-hit is increased when attacking opponents with shorter reach, and reduced against opponents with longer reach. Reach has diminishing returns so the first few points of Reach Advantage confer the greatest bonus.
* It only applies when attacking a target adjacent to you or up to 2 tiles away with nothing between you and the target (an abstraction of the idea that the two of you intend to reach and hit each other). 
* If the attacker has a Reach Disadvantage against the target, it is disabled after a successful attack, until the attacker waits or ends their turn. So, subsequent attacks after the first one are easier, but only during this turn.
* Characters with shields can, depending on the type of shield, ignore a certain amount of the attacker's Reach Advantage when defending. With the Duelist perk, they can ignore it even when attacking.
* Characters who are rooted have their Reach halved. Combatants without a melee attack have no Reach.

## Reach Display
<img src="https://raw.githubusercontent.com/wiki/Battle-Modders/mod-reforged/assets/images/Reach-CharacterScreen.png" alt="Reach Display on the character screen" align="right" width="25%"/>

<img src="https://raw.githubusercontent.com/wiki/Battle-Modders/mod-reforged/assets/images/TacticalTooltip-1.png" alt="Reach Display in an entity's tooltip during combat." align="right" width="23%"/>

A character's Reach is displayed in his tooltip on the battlefield right below the turn order. We decided to put this information in this prominent place because it is a key information for matchups during combat. You will also notice that the tactical tooltip in Reforged also contains a lot of other information which isn't present in vanilla, and we will explain that in a later dev diary.

The information consists of three numbers. The first one is the current Reach of this character. The two numbers in the parantheses depict the character's Offensive Reach Ignore and Defensive Reach Ignore respectively and represent the amount of Reach Disadvantage that this character can ignore when attacking or defending against an attack.

On the character screen on the world map, we have decided to replace the Morale bar with a bar that instead shows Reach. This is because the morale information provided by that bar was redundant on the world map, and in the battle map the information about a character's morale is directly available on that character's tactical tooltip or as an icon next to the character.

## Reach Values
### Races
Different races have different base reach:
* Goblins: 1
* Humans: 2
* Orcs: 3
* Beasts, depending on their size (e.g. Lindwurms have 11)

### Weapons
Two-handed weapons generally have longer reach than one-handed weapons. Long melee weapons that have 2-tile attacks have even longer Reach. Swords generally have longer Reach than their peers. Examples:
* Dagger: 1
* Fighting Axe: 3
* Noble Sword: 4
* Militia Spear: 5
* Longaxe: 6
* Zweihander: 7
* Pike: 7

## Perks and Traits
Various perks and traits have been designed to work with the Reach mechanic. Below are a few examples:
* **Formidable Approach:** shows that you have trained to both approach enemies and be approached by enemies while maintaining your advantage. Your Reach Advantage grants greater bonuses against enemies who have not hit you yet.
* **Sweeping Strikes:** Greatly increases your Reach temporarily after using an AOE attack while making it harder for those you attacked to reach you with their attacks.
* **Duelist:** In addition to other effects, gain additional Reach when using a two-handed weapon.
* **Huge trait:** In addition to previous effects, now grants +1 Reach.
* **Tiny trait:** In addition to previous effects, now grants -1 Reach.

## Implications
* Large two-handed weapons are now viable even in the early game (when your melee defense attribute is low) as they confer skill and defense advantage against enemies with shorter reach.
* Shields are important as they can help ignore the opponent’s offensive Reach Advantage.
* Fighting large opponents (e.g. large beasts) is now harder without large weapons (quite thematic).

## A Nod To Vanilla BB
To be fair, vanilla Battle Brothers *did* try to abstract Reach in a simple way. For example, spears have +20% chance-to-hit with Thrust, while swords have a higher chance-to-hit with Slash. However, this was a very basic interpretation - not enough to add the level of tactical depth that conforms to our vision. With our design of Reach, this concept is more nuanced and interacts dynamically with a character's positioning, situation, skills, and equipment. To account for the additional advantage from Reach, in Reforged we have reduced the bonus chance-to-hit of Thrust from +20% to +10% and of Slash from +10% to +5%.

# Shields
## Fixing Split Shield
We tried for months to achieve a balance with breaking shields where it would remain a viable tactic for the player, while also keeping shields themselves viable for use by the player. Unfortunately, the two things work against each other - if you incentivize breaking shields, you disincentivize their use by the player and if you make shields strong, you disincentivize breaking them.

Problems with the Split Shield mechanic:
- Split Shield with axes is probably one of the least used skills in Battle Brothers. It is only used in very particular situations such as when fighting Schrats.
- Split Shield with weapons other than axes is probably never used.
- There is no way for the player to counteract Split Shield or its effects.
- Splitting an enemy's shield is often the wrong tactical decision because they then gain the Double Grip bonus and become more dangerous.

From a thematic point of view, attacking someone's shield isn't something you want to do in a battle. You want to attack the person, or work around their shield. In most circumstances shields are very durable, and attacking someone's shield will probably end up damaging your weapon or making your weapon get stuck in the shield, hence disarming you, instead of doing much harm to the shield.

We believe this is one of those areas where the vanilla game's design is poor. However, improving this design requires some outside-the-box thinking. Our solution is as follows:

- Make shields virtually unbreakable. Most shields now have a very high durability. This solves the issue where players avoid shields because they are unreliable. We no longer have to worry about balancing shield reliability with incentivizing shield breaking.
- Instead we add an active tactical aspect to Split Shield with immediate gains, and ways to counteract it:
    - The defense provided by Shields now drops linearly as you build Fatigue, down to a minimum of 50% at maximum fatigue.
    - Split Shield has been renamed to Smash Shield and in addition to damaging the shield, now also inflicts significant Fatigue on the target. You now gain immediate benefit out of it by wearing out the shield user. This makes the skill useful even on non-axe weapons.
    - With the availability of Recover on all humans, which we will elaborate on in a future dev diary, shield users can use it to recover their shield defenses.

The above changes are a significant improvement to one of the most unused skills in the game and now makes it interact actively with other mechanics.

## New Mechanics
- Shield Expert: No longer reduces damage to shields. Instead reduces the maximum drop in shield-provided defenses from 50% to 25% at maximum fatigue.
- Axe Mastery: No longer increases damage to shields. Adds the Hook Shield skill to equipped axes.
    - New skill: Hook Shield: 3 AP, 15 Fatigue. Uses Melee Skill but ignores shield defense. If successful, applies the Hooked Shield effect on the target, which reduces the target's shield defenses by 75% until the start of their turn or until they use a skill. Removes Riposte and disables Rebuke while it is applied. Cannot be used against targets who are under the effects of Shieldwall.

These changes keep Axes relevant as an interesting choice of weapon against shields - except instead of breaking them you have a thematic and interactive skill to work against them. As a shield user, the player can protect themselves against Hook Shield by using Shieldwall preemptively. Hence, it provides mechanical possibilities to both the shield user and the attacker to work with the presence of the shield.

## Shield Identities
In the new design space for shields, the attributes of various shields have been tweaked to give them their own identity:
- Adarga: Now a light shield with decent defenses but is not so durable.
- Wooden Shield: Your standard shield. Not easy to break.
- Heater and Kite Shields: Better than wooden, but more fatiguing. Even harder to break.
- Sipar: The best standard melee shield with high melee but lower ranged defense. Very fatiguing to wear, almost impossible to break.
- Undead Shields: Not so durable and therefore easier to break.
- Craftable Lindwurm Shield: A very light shield with high defense and durability.
- Craftable Schrat Shield: Has a unique effect where it can spawn a sapling when hit.
- Craftable Kraken Shield: High defense and durability and now also reduces the Resolve of adjacent enemies.

# One-Handed Weapons
The vanilla game added Double Grip to one-handed weapons to give them a damage boost and perhaps try to make them competitive with two-handed weapons. Even so, the meta in vanilla still is mostly two-handed weapons. In our view, this design space can be improved. Especially in Reforged where we have several two-handed weapons with 4 AP attacks (in addition to the vanilla 2h cleavers), the design space is wider. In our vision the design should be:
- Two-Handed weapons do more damage and have Reach Advantage.
- One-Handed weapons do less damage, but are more versatile and easier to use, primarily coupled with a shield.

This means that the main strength of one-handed weapons is the fact that they can be coupled with a shield. So this combo should provide significant bonuses to make it competitive with 2h weapons without going the rather boring route of just trying to equalize damage.

- Duelist has been reworked:
    - Works with all melee weapons as long as the primary attack of the weapon has a base Action Point cost of 4 or less.
    - Gain +25% armor penetration with 1h weapons, +35% when using a shield, +15% with two-handed weapons.
    - Gain +1 Reach with two-handed weapons.
    - Shields now also ignore the target's Reach Advantage when attacking.

This change makes a shield user with Duelist able to ignore most Reach Disadvantage situations, while the +35% armor ignore offsets some loss of the double grip bonus.

- Rebuke is a perk on the shield perk group which grants you a passive chance to return a missed melee attack against you with a free attack of your own. It has a higher chance to trigger when using a shield. This makes Rebuke an interesting damage option for shield users as, coupled with high defenses, a shield user can continue to dish out damage during the off-turn.

- Exploit Opening: A perk that provides +10% chance-to-hit or ignores the target's shield defenses, whichever is greater, for the next attack. This makes Exploit Opening a possible perk for characters to counter shield users.

There are also other changes sprinkled here and there which provide a fresh take on using 1h and 2h weapons in Reforged and we hope that you will feel that the gameplay with both types of weapons feels immersive, effective and fun in its own way.

# Other Changes
- Throwing Spear: No longer does damage to shields.

We don't have a good solution for Throwing Spear in the current new rebalance. We will try to find a niche for it eventually, but for now we have removed its ability to take out shields - as we want shields to be reliable, while having more interactive ways to counter them. This means the identity of the Throwing Spear is currently a single-use, high damage throwing weapon.


