**Dev Diary #3 - 06-Sep-2024**\
_Uberbagel_

* [Introduction](#introduction)
* [Perk Tree Creation](#perk-tree-creation)
* [Perk Group Categories](#perk-group-categories)

## Introduction
While vanilla Battle Brothers hosts a reasonable slew of perks that are well-balanced and interesting, each brother has access to the exact same ones. This offering ultimately leads to certain meta builds and brothers that, after a few campaigns, start to feel not all that unique anymore. Battle Brothers: Reforged endeavors to build upon this system by adding more than 100 new perks, improving vanilla perks where necessary and creating dynamically generated perk trees for each and every brother. Perks allocated to a brother's tree are influenced by many factors, including Talent Stars, Character Traits, Character Background and more. Our primary goal is a system where every brother feels unique with many viable build paths and interesting choices to make when leveling.

## Perk Tree Creation
<p align="center">
<img src="https://github.com/Battle-Modders/mod-reforged/wiki/assets/images/Perk-Tree.jpg" alt="A visual of a character's perk tree in Battle Brothers: Reforged."/>
</p>

In Reforged, perks are contained within Perk Groups which are divided into different Perk Group Categories. There is a baseline number of perk groups of each category allocated to a character on perk tree generation. These numbers can change, however, based on the background of the character in question. Generally speaking, backgrounds with more combat experience or those born into an advantageous life will receive more categories and therefore have larger perk trees. This results in more-expensive recruits not necessarily being better than those that are cheaper but having the unique advantage of more flexibility in perk choice and development.

The perk groups themselves have been meticulously designed to adhere to a certain theme, while granting unique offensive and defensive capabilities for a myriad of builds.

During a character's creation, the character-specific perk tree is created by weighted random rolling. This is a deep and complex process and is intended to create thematic perk trees for each character and give each character his own identity. An overview of the process is as follows:

1. First of all any Exclusive perk groups assigned to a character's background are added. Also all General perks are added.
2. Then we roll Perk Groups from Perk Group Categories. This happens in the order of: Shared, Weapon, Armor, Fighting Styles. A character continues to roll Perk Groups from a category until the maximum allowed perk groups from that category for that character are assigned. Then it moves to the next category. Each subsequently rolled perk group's chance is influenced by previously rolled perk groups during this process. At no point is this process completely random - it is always influenced by weights and multipliers based on background, traits, talents and previously rolled groups.
3. Special perks and perk groups are rolled and a character has a chance to get one or more of these depending on individual criteria defined for each individual special perk group.

### Ease of Use
The user can hover over a perk in a character's perk tree and hold down the Shift button to highlight all other perks belonging to that perk's group. Additionally, in the tooltip of a perk, the perk groups that this perk belongs to are shown at the bottom. These are in the form of nested tooltips and hovering over the perk group's name will open an additional tooltip showing the details of that perk group.

![[assets/images/DynamicPerks-ShowingPerkGroupInTooltip-1.png]]
![[assets/images/DynamicPerks-ShowingPerkGroupInTooltip-2.png]]

### Recruit Tryout
After tryout, a potential recruit's perk groups are shown on the recruitment screen (screenshots at the end of this diary). A user can mouse over each of these perk groups to get a tooltip showing the details of that perk group. Similarly, the entire perk tree of a recruit can also be seen on the recruitment screen and all the perks can be moused over to see their tooltips (screenshots at the end of this diary).

## Perk Group Categories
### Exclusive
Exclusive perk groups represent the history or upbringing of the character and are determined almost exclusively by the character's background. Most backgrounds are guaranteed one particular Exclusive perk group, but some have a chance of a few different ones.

| Icon | Group | Description |
| :--: | :--: | :--: |
| ![[assets/images/perk_groups/rf_knave.png]] | **Knave** | Someone who is accustomed to skullduggery and subterfuge. Throw sand in your opponent's eyes, land cheap shots and engage the enemy with suprise attacks! |
| ![[assets/images/perk_groups/rf_laborer.png]] | **Laborer** |  Any background whose life involved hard labor. Reap the benefits of a body made strong by work. |
| ![[assets/images/perk_groups/rf_militia.png]] | **Militia** | Those who have defended their home from beasts, raiders or otherwise. Utilize strength in numbers to its greatest extent. |
| ![[assets/images/perk_groups/rf_noble.png]] | **Noble** | Men born of blue blood, even if their families don't recognize them as such. Fight with the confidence of a man above others. |
| ![[assets/images/perk_groups/rf_pauper.png]] | **Pauper** | Beggars, Cripples, Refugees and Slaves. Usually worth little on the battlefield, but perhaps the odd pauper has some promising potential. Sometimes men raised from the dirt can stand tall as mountains... |
| ![[assets/images/perk_groups/rf_raider.png]] | **Raider** | Brigands who took what they wanted from those weaker than themselves. Exploit and bully those who fear the menace of a criminal. |
| ![[assets/images/perk_groups/rf_soldier.png]] | **Soldier** | Men trained to fight with a batallion on the battlefield. Steady your allies and take advantage of exhibited patterns in your opponents attacks. |
| ![[assets/images/perk_groups/rf_swordmaster.png]] | **Swordmaster** | Those who've acheieved true mastery with a sword. Rule in combat with unique and deadly ways of fighting with a blade. |
| ![[assets/images/perk_groups/rf_trapper.png]] | **Trapper** | Beastslayers, Fisherman, Manhunters and others with experience in capturing man or beast. Trip up your opponents and utilize nets to their greatest advantage. |
| ![[assets/images/perk_groups/rf_wildling.png]] | **Wildling** | Backgrounds more at home in the wilds than the civilized lands of men. Revitalize yourself with bestial vigor or fight with a feral rage. |

### Shared
Perk groups in the Shared category represent the physical, mental and emotional traits of a brother. They are strongly affected by character traits, talent stars and the character's background. Most backgrounds will roll 2 shared groups.

| Icon | Group | Description |
| :--: | :--: | :--: |
| ![[assets/images/perk_groups/rf_agile.png]] | **Agile** | Fight with mobility and traverse the battlefield with ease. Sprint across the battlefield, become energized after killing an enemy and more effectively strike multiple targets with a single swing. |
| ![[assets/images/perk_groups/rf_fast.png]] | **Fast** | Those who are fleet-of-foot and thought. Quickly swap items in combat, partner up with another brother for unique bonuses and utilize speed to pick your foes apart. |
| ![[assets/images/perk_groups/rf_tactician.png]] | **Tactician** | Those with a unique mind for battlefield tactics. Worth their weight in crowns. Help nearby allies keep their shields up, push through enemy lines or hold fast against enemies that displace you. |
| ![[assets/images/perk_groups/rf_tough.png]] | **Tough** | Sometimes being strong and robust is all you really need. Improve survivability, take advantage after slaying an opponent and take a breath in combat allowing for more actions. |
| ![[assets/images/perk_groups/rf_trained.png]] | **Trained** | Men with training in arms, armor and formation fighting. Manuever on the battlefield, use weapons more effectively and use your opponents impatience against them. |
| ![[assets/images/perk_groups/rf_unstoppable.png]] | **Unstoppable** | Those with a lust for combat unusual amongst the masses. Ignore temporary injuries, build momentum and ride the ebbs and flows of battle. |
| ![[assets/images/perk_groups/rf_vicious.png]] | **Vicious** | Men with a penchant for violence and killing. Target opponent vulnerabilities, fight with confidence and go berserk against your foes. |
| ![[assets/images/perk_groups/rf_vigorous.png]] | **Vigorous** | Your endurance and ability to sustain damage sets you apart. Utilize your body's natural survival instinct, gain bonuses for acting decisively and take more actions when fresh and furious. |

### Weapon
Each Weapon Perk Group has 3 perks: one between tiers 1-3, a mastery at tier 4 and one between tiers 5-7. We wanted these perks to truly feel impactful and feel like you're mastering and unlocking the unique capabilities of your weapon. Weapon perks often synergize with each other, but can also be picked independently depending on your needs. Average characters roll three weapon groups.

| Icon | Group | Description |
| :--: | :--: | :--: |
| ![[assets/images/perks/perk_mastery_axe.png]] | **Axe** | Focuses on enhancing injuries and using the hooked blade of axes to counter opponents. |
| ![[assets/images/perks/perk_mastery_bow.png]] | **Bow** | Allows for sustained fire, harrying shots and displacing enemy troops. |
| ![[assets/images/perks/perk_mastery_cleaver.png]] | **Cleaver** | Capitalize on fatalities, apply bleed and cause injuries. |
| ![[assets/images/perks/perk_mastery_crossbow.png]] | **Crossbows & Firearms** | Utilize precision targeting and slow down your enemies with heavy shots. |
| ![[assets/images/perks/perk_mastery_dagger.png]] | **Dagger** | Take advantage of distracted opponents with quick stabs and negate reach with speed. |
| ![[assets/images/perks/perk_mastery_flail.png]] | **Flail** | Take advantage of the unpredictable nature of your weapon to make repeated strikes against multiple opponenets. |
| ![[assets/images/perks/perk_mastery_hammer.png]] | **Hammer** | Dismantle armor, disrupt opponent effectiveness and knock an opponent back, taking their position. |
| ![[assets/images/perks/perk_mastery_mace.png]] | **Mace** | Disable your opponents, gain advantages on headshots and crush some bones! |
| ![[assets/images/perks/perk_mastery_polearm.png]] | **Polearm** | Distract enemies, support adjacent allies and utilize the length of your weapon to better hit an opponent's head. |
| ![[assets/images/perks/perk_mastery_spear.png]] | **Spear** | Target gaps in armor with multiple attacks and minimal exertion. |
| ![[assets/images/perks/perk_mastery_sword.png]] | **Sword** | Maintain tempo on the battlefield and dance around clumsy opponents. |
| ![[assets/images/perks/perk_mastery_throwing.png]] | **Throwing** | Replenish ammunition from already thrown weapons, utilize uniqueness of different throwing weapons to debuff opponents and become the perfect hybrid fighter. |

### Armor
Vanilla Battle Brothers has an arguable design flaw where there's a wide gap in viable armor pieces in the late game. With one armor perk having a soft weight threshold of 15 and the other incentivizing the highest durability and effectively heaviest armor pieces, there's clear room for a perkset utilizing armors somewhere in the middle. Therefore, alongside a Light Armor and Heavy Armor perk group, we've created a Medium Armor perk group with unique perks to utilize these otherwise undesirable pieces of gear.

| Icon | Group | Description |
| :--: | :--: | :--: |
| ![[assets/images/perk_groups/rf_light_armor.png]] | **Light Armor** | Contains the Relentless, Dodge and Nimble perks. Ignore enemy reach with high Initiative if Nimble. |
| ![[assets/images/perk_groups/rf_medium_armor.png]] | **Medium Armor** | Contains the Skirmisher, Dodge and Poise perks. Skirmisher functions as an amalgamation of Relentless and Brawny, while Poise does the same for Nimble and Battleforged. Ignore enemy reach with High Initiative if Poised. |
| ![[assets/images/perk_groups/rf_heavy_armor.png]] | **Heavy Armor** | Contains the Brawny, Bulwark and Battleforged perks. Bulwark gives heavily armored men with shaky knees the confidence they should have in a suit of heavy plate. Utilize superior protection to ignore enemy reach when Battleforged. |

### Fighting Style
Fighting Styles are perk groups containing perks that complement the way that you fight. Whether with a javelin or bow, arming sword or zweihander, and shielded or unshielded, there are perks for your particular style. The category is divided into four groups: Power, Ranged, Shield and Swift Strikes.

| Icon | Group | Description |
| :--: | :--: | :--: |
| ![[assets/images/perk_groups/rf_power.png]] | **Power** | Favors two-handed weapons and those with long reach. Attack easier after moving with Vigorous Assault or keep enemies at bay with Sweeping Strikes. |
| ![[assets/images/perk_groups/rf_ranged.png]] | **Ranged** | Fight more effectively with Ranged Weapons. Use the Entrenched perk to gain bonuses fighting in the safety of a formation, aim for the weak spots with Bullseye and skewer heads with Nailed It.  |
| ![[assets/images/perk_groups/rf_shield.png]] | **Shield** | Utilize the unique defensive capabilities of shields. Exploit missed enemy attacks, push through hostile lines and cover an ally's escape if they find themselves in a sticky situation.|
| ![[assets/images/perk_groups/rf_swift.png]] | **Swift Strikes** | Take advantage of the swift speed of light weapons. Enable bonuses on successive strikes or utilize a free hand to good effect. |

### Special Perks
<img align="right" src="https://github.com/Battle-Modders/mod-reforged/wiki/assets/images/Perk-Tryout-2.png" alt="A visual of a character's tryout screen showing their perk groups." width="35%"/>
A few design principles embody what we've tried to build with this system: Variety, Depth and Individuality. One final way we've strived for this is with the addition of Special Perks and Perk Groups. These are Perks and Groups that every character has a chance to roll for as long as certain requirements are met and they are not otherwise restricted from gaining access. Some characters may have an improved chance of rolling certain Special Perks and Groups if they have the right talent, Traits or Background. Some noted Special perks include Professional, a tier 1 perk which gifts you the first two weapon perks in a weapon perk group in your perk tree; Fencer, which enables unique capabilities with fencing swords; and Back to Basics, which gives two additional perk points but drops your accessible perk tier down to tier 2.

Currently, there is only one Special perk group, that being Leadership. Those known to be brave or of highborn lineage are most likely to possess this group. The Leadership group is most important for a bannerman, as it allows you to support and rally your troops, command allies to take immediate action and inspire nearby allies to fight more fiercely.

### General Perks
<img align="right" src="https://github.com/Battle-Modders/mod-reforged/wiki/assets/images/Perk-Group-Tooltip.png" alt="A visual of a character's tryout screen showing their perk tree." width="35%"/>
This category contains perks which every character always gets in their perk tree. Currently, this only consists of a single perk group called General which contains a single perk: Bags and Belts. We made the decision that Bags and Belts should be present in every perk tree as it is significant to a wide range of builds. Therefore, every character receives the General perk group and access to the Bags and Belts perk.

### Recover
One final significant perk design change we've made is that every human character now has access to the Recover skill by default. Throughout our long playtest phase of Reforged, we found that Recover had been edged out of favorability due to competition from other perks in Reforged. We thought an interesting solution was to give the Recover skill to every human character, as the skill comes with the built-in cost of having to take a full turn off of combat anyways. This design serves to give every brother a reliable, if slow, way to regain stamina. This change is also significant for the enemy, as in Reforged, we've normalized the base fatigue recovery rate per turn of every human enemy to that of player company characters, being 15. This solves an inherent advantage enemy humans had in vanilla and enables more fatigue counterplay against these foes.

<p align="center">
<img src="https://github.com/Battle-Modders/mod-reforged/wiki/assets/images/Perk-Tryout-1.png" alt="A visual of a perk group's tooltip in the recruitment screen." width="40%"/>
</p>
