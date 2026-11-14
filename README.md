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

V1.5.2
-Initiative Tracker Changes:
	-Added the ability to have the actor whose turn is active, delay their turn by holding click on them and dragging them to the desired position
	-Added an "Undo" button, which can undo almost any action taken in the tracker
	
V1.5.3
-Initiative Tracker Changes:
	-Added Celerity Turns tracking, right clicking an actor let's the user designate them as a "Celerity User", which shows a Celerity field with - and + buttons. These can only be set before the first actor delays, or takes their turn. After which, they become locked until the next round. Once a round would normally end, it wraps back around through all Celerity Users, until they have no celerity turns left. After which, the round ends.
	-Added the "Actor List" and the ability to save actors as presets. The list can be searched, sorted, and updated. Adding any duplicate actors marks them as such between brackets. Saving a preset of an actor already on the list asks the user to confirm, and then replaces the actor preset.
	-Changed a lot of button labels. Mainly, the "Roll Inititative" button now starts the encounter (or ends it), and the "Next Round" button now reads "Start Round" at first. Rounds no longer start automatically, and the start round button must be clicked before locking in data (like celerity uses, and initiative).
	-Added a new Actor toggle for revealing an actor's name. This saves to an actor's preset.
		-Made it so that remote clients can't see an unrevealed actor's name, and instead show as "Enemy [X]", the X being number of enemy.
	-Moved all tag related actor toggles to their own submenu within the context menu.
	-Added an Auto Update option to the tracker, when enabled, it automatically updates presets with changes on the tracker (but not if they're duplicates of actors).

V1.5.4
-Initiative Tracker Changes:
	-Added 2 more Actor Tags.
		-Player: Always revealed, doesn't store nor show the Reveal tag.
		-Enemy: Always hidden, doesn't store the reveal tag, but can be manually revealed mid-encounter.
	-Persistent tag moved out of the submenu, and made back into it's own button on the normal context menu.
	-Hidden Actor Names are numbered in order accounting for revealed actors.
-Fixed some "Hover over" text.

V1.6
-Added "Rule Book" button to the top right of the page. This let's you load the core rule book PDF for VTM v20, and it acts as a PDF Viewer of it, with built-in indexes for ease of search.