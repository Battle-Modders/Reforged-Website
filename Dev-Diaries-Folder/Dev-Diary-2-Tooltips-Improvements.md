**Dev Diary #2 - 06-Sep-2024**\
_LordMidas_

* [Tactical Tooltip](#tactical-tooltip)
* [Nested Tooltips](#nested-tooltips)

# Tactical Tooltip
In Reforged we have significantly improved the tooltip that you get when hovering over an entity during a battle. These improvements include:
- Listing all the Status Effects, Perks, Actives and Items of the entity.
    - All of these are nested tooltips so the user can hover over them to see their individual tooltips.
- Listing the attributes of the entity along with the current modifiers.
- Replacing the Morale bar with Action Points bar.
- Showing actual numerical values for Hitpoints, Armor, Fatigue etc.
- Making it clear that an entity has already used Wait.

This information can be selectively enabled/disabled and customized using options provided in the Reforged Mod Options.

## Screenshots
### Vanilla Comparison
The following two screenshots show a comparison of the tooltip of an Ancient Legionary in vanilla vs a tooltip of the same entity in Reforged. The green and red numbers next to attributes show the total bonus/malus to the attribute the entity currently has due to various reasons such as equipment, effects etc.
<img align="center" src="https://github.com/Battle-Modders/mod-reforged/wiki/assets/images/TacticalTooltip-Vanilla.png" alt="" width="35%"/>

<img align="center" src="https://github.com/Battle-Modders/mod-reforged/wiki/assets/images/TacticalTooltip-1.png" alt="" width="35%"/>

# Nested Tooltips
Nested Tooltips is a system that is present in many modern-day games but was missing from Battle Brothers. We have brought this feature to Battle Brothers via the Nested Tooltips Framework (more on that in a later dev diary) and have made extensive use of it in Reforged to streamline and improve user experience especially when learning about new concepts and the relationship between various items, skills and concepts. Nested Tooltips exist both as text links (in these screenshots you can see them as underlined text) and as images. You can hover over the text or images to open their respective tooltips.

We will be showcasing the use of this feature in various dev diaries but here we show how this helps us make the most of the new and improved Tactical Tooltip.

The tactical tooltip display can be customized using Mod Options to specify a threshold above which the effects/perks etc. are collapsed into a list of icons instead of being listed individually as icon + text. However, in both cases, they are nested tooltips and can be hovered over to see the tooltip of the respective skill or item.

<img align="center" src="https://github.com/Battle-Modders/mod-reforged/wiki/assets/images/TacticalTooltip-2.png" alt="" width="35%"/>
<img align="center" src="https://github.com/Battle-Modders/mod-reforged/wiki/assets/images/TacticalTooltip-3.png" alt="" width="35%"/>
<img align="center" src="https://github.com/Battle-Modders/mod-reforged/wiki/assets/images/TacticalTooltip-4.png" alt="" width="35%"/>
