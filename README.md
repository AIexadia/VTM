V1.0
-First version of the Web App

V1.1
-Added Damage section
-Implemented safety net
-Made all extra modules (Probability, Damage, and future ones), work off of a "Tabs" system.

V1.2
-Changed preset list to be scrollable, default showing 3 items, with the ability to change how many are shown.
-Made it possible to rearrange presets, or have them rearrange themselves based on how most recently used.

V1.2.1
-Added a "Mod" input for Dice Pools that can be toggled on and off.

V1.2.2
-Added modifier input for Difficulty (from -8 to 8, but difficulty clamps between 2 and 10)

V1.3
-Added Settings menu (top right)
	-Added "Rules" Settings Subsection
		-Added M20 Thresholds Toggle, this implements a ruling from WoD Mage The Ascention ruling for difficulties higher than 9.
	-Added "UI Options" Settings Subsection
		-Added "Botch Toggle", hides the botch toggles in the rollers.
		-Added "Instant Results", skips rolling animation.
		-Added "Cookie Refresh", everytime the page is loaded, all stores cookies are refreshed.
	-Added "Appearance" Settings Subsection
		-Added Accent color, and background tint options. Along with a Reset colors button.
	-Added "Danger Zone" Settings Subsection, along with a button to clear all saved data.
	
V1.3.1
-Added Average Damage expected on damage roller

V1.3.2
-Added "Wide Aspect" toggle in the settings menu, under "UI Options".
-Added Single Roll button, to roll a single D10 (and a toggle for it in settings).
-Changed M20 Thresholds to start at a 10 or higher.

V1.4
-Changed all toggles to be the same style (buttons with an icon)
-Added a new setting under "Appearance" called "Toggle Style" which changes all toggle buttons to words rather than symbols.
-Added a "Single Roll" button, which rolls a single D10.
-Added Average Successes Expected for the main roller, and a toggle to hide Averages (both for Main and Damage rollers)
-Changed the M20 Thresholds to have a maximum difficulty of 10 before needing more successes.
-Added the ability for a custom background tint color.
-Adjusted how the page resizes itself to account for Wide Aspect mode.
-Added a toggle to let presets load the Mods that they were saved with.

V1.4.1
-Preset Changes:
	-Changed Presets so they show on 2 separate columns.
	-Saved presets no longer show all their info on the button, only the amount of dice, and the difficulty. The text on presets is now centered.
	-If a preset was saved with MODS, it shows a + or - (depending if the mod in memory is positive or negative).
	-If a preset was saved with Specialty enabled, it shows the dice pool part of the info in Bold.
	-When a preset button is hovered over, it shows the full info saved to the preset.
	-Added the ability to right click a preset, opening a context menu which replaces the previous delete button.
		-Context menu has the option to delete a preset.
		-Presets can now be renamed in the context menu. A new preset being saved with the same name as another will give an error.
	-Shift-Clicking a preset forces a quick roll with MODS enabled on the preset.
	-Removed the drag handle in place of a Drag-n-Hold system to rearrange presets.
	
V1.4.2
-Fixed an error that didn't update AVG damage expected when toggling Specialty or Botch.

V1.5
-Added changelog button.
-Added the ability to shift+click/right-click the "Single Roll" button, and have it add/remove 1 dice to the last roll, which is accounted for in results.
-Added a new Module "Initiative", this functions as an Initiative Tracker.
	-It is possible to "Host" an initiative tracker, so that those that join with the code get to see the tracker as well.
-Added a new subsection to the settings menu called "Modules", which enables and disables modules.
-Added "Main Roller" toggle in the settings menu, under "UI Options". This turns off the main roller, which in turn lets users enable the new "Simple Roller" toggle. It also hides the Probability module, and when both the main roller and simple roller are off, the extra modules treat the "Wide Aspect" toggle as always off.

V1.5.1
-Added README.md file
-Added "Fresh Initiative" toggle to the Initiative Tracker. When enabled, a new D10 roll for initiative is done at the start of each round.
	-Dice rolling SFX plays each time a new round begins when this option is turned on.
-When at least 1 turn has passed on the first round, the "Roll Initiative" button grays out, and pressing it shows a confirm message to reset rounds, should it be pressed again within 4 seconds.
-Changelog now automatically updates from the repo.