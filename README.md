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

V2.0
-General Changes:
	All numbered input fields now select the whole input when clicked.
-Rule Book Changes:
	-Added a new "Exact" search button to look for exact words and sentences within the PDF.
	-Made it possible to select text within the PDF (consequently allowing to copy said selection).
-Main Roller Changes:
	-Added an "Action" input field to the roller. This one represents a given action's number in a chain of multiple actions. The final dice pool is divided by this number, rounded down. If the dice pool would be 0 due to this, the action cannot be performed.
-Added Character Manager:
	-An entire manager for character sheets that includes everything in the Sheet Template from the book, and more.
	-This addition hooks directly into the main roller, including rolls, and even initiative.
	-Added a new Module called "Character" which let's the user have easy access to a chosen character for the sake of playing and rolling using their attributes.
-Implemented Account Sign-in and remote data storage. With an account signed in, all settings and data are now stored in server, rather than just your browser/cookies.

V2.0.1
-Character Managed Changes:
	-Added the ability to share and sync characters with other users by using a code.

V2.1
-General Changes:
	-The Initiative Tracker, Character module, and Character Manager now require being signed in.
-Initiative Tracker Changes:
	-Removed the "Add new actor" button.
	-Added a "Rolls" section, letting the host call for rolls and see their results.
	-Added a roll "History" for the host.
-Character Manager Changes:
	-Characters are now shared by Player ID instead of codes.
	-Users can share up to 3 characters at a time.
	-Hosts can now edit a joiner's character if it's already shared with them.
	-Out-of-clan Disciplines added during character creation now count as clan Disciplines (except for Caitiff).
	-Disciplines can be marked as clan (or out-of-clan) in Free-form edit and XP mode.
-Fixed Celerity Actions not showing on an actor's initiative mod.

V2.2
-Settings Changes:
	-Account options moved into their own "Account…" overlay, with a cleaner Player ID display.
-Character Manager Changes:
	-Merits & Flaws can be picked from the book's list, filling in their cost.
	-Right-clicking a trait, Background, Merit, Flaw, Clan, Nature, Demeanor, or the Health / Blood Pool / Willpower labels opens a menu linking to its page in the Rule Book.
	-Added the Random Character Generator as a new character option (pick a clan or random, a name, and XP to spend).

V2.3
-Character Manager Changes:
	-Replaced the character dropdown with a character browser: character cards with key stats, folders, search and sorting. Synced characters show up there too.
	-Folders sync between devices with your account.
	-Random Character Generator:
		-Its options now use toggles like the Settings menu.
		-Added Merits & Flaws options: max cost and target points for each.
		-Added a "Carried equipment" option: up to 3 weapons (including Feral Claws) and armor, when they fit the character.
	-Feral Claws and other natural weapons attack with Dexterity + Brawl.
	-Hovering a Background, Merit or Flaw shows a short summary (also shown in its right-click menu).
	-Disciplines and Backgrounds can be rolled. The Quick Roller's "Other" tab is now "Virtues", and a new "Other" tab holds Disciplines and Backgrounds.
	-Added a "Defensive Maneuver" button (Block, Dodge, Parry). It and the Soak button now sit under Health.
-Initiative Tracker Changes:
	-Celerity actions cost one blood point each (not limited by Generation), and you can't take more than your blood allows.
	-Right-clicking an actor lets the host call for a roll from them, even when it isn't their turn.
	-The Start round / Next turn / End round button fills the rest of its row.
	-The dice sound plays when someone else's rolled result comes in.

V2.4
-Character Manager Changes:
	-Renamed "Defensive Maneuver" to "Defend". Soak and Defend now share their own row under the damage/heal buttons.
	-Blood Pool (Spend, Feed, Boost) and Willpower (Spend, Regain) buttons use the same even row design.
	-Folders in the character browser are full width on phones.
	-Folder names save with Enter, the ✓ button, or tapping elsewhere (✕ or Esc cancels).
	-Random Character Generator:
		-Added a Class option (Bruiser, Gunner, Mage, Charmer, Controller, Rogue) that steers the character and concept toward a theme.
		-Names now fit the character's nationality and repeat far less.
-Initiative Tracker Changes:
	-Players hear a notification sound when the host calls a roll from them.
	-A player's characters already in the tracker are recognized when they rejoin (any room, any device signed into their account), so they don't need to be re-added.
-Fixed typing in names and other fields on phones getting cut off by background updates.

V2.4.1
-Sync Changes:
	-Syncs only when something really changed, and an edit counts once it's confirmed (Enter, Tab or clicking elsewhere). Changes from other devices are checked every 30 seconds.
-Fixed adding a Discipline or Background sometimes doing nothing when a sync or tracker update arrived while typing its name.
-Fixed dropdowns and expanded sections (like "V20 experience costs") closing or resetting every few seconds while signed in.

V2.5
-Renamed the app to "VTM Player Companion". The subtitle changes between the Roller and Characters views.
-Added a notifications center (bell next to Settings) for things like characters shared with you, access changes and settings changed on another device. Clear them one by one or all at once.
-Settings Changes:
	-The Account overlay lists the characters you're sharing, each with a shortcut to its share menu.
-Character Manager Changes:
	-Added Stored Equipment next to Carried Equipment in Details > Possessions. Drag weapons and armor between them (or use Store / Carry). Stored items aren't usable in play.
	-Reordered the character buttons: Export sits next to Import, then Share; Delete (or Remove) is at the far end.
-Fixed the "Synced" label and the share access dropdown text not being centered.

V2.6
-Added Friends (button next to Notifications): add players by their player ID, accept or decline requests from the notification or the Friends panel, and share sheets straight to a friend. Needs the updated sync server.
-Added Usernames: everyone signed in picks one, and it's the only name other players see (sharing, friends, XP stamps). Your Google name and email stay private. Change it in Settings > Account.
-Character Manager Changes:
	-Experience flags use the Settings-style toggles, on one row when there's room.
	-XP awards show who added them, and who last edited them and when.
	-Backstory and Other Facts have a text editor: bold, italic, underline, strikethrough, headings, lists, quotes and text colours.
	-Other Facts can be shown in up to 3 columns, with optional column breaks.
-Initiative Tracker Changes:
	-Joiners hear the dice sound when a new round starts.
-Fixed the Details tab not showing for characters.
-Fixed Celerity actions planned between rounds changing initiative before the next round starts.
-Fixed Merits and Flaws added in Free-form edit not filling in their cost from the book.

V2.7
-Friends hosting a room now send you a notification with a Join button, and the Friends panel shows a Join room button while they host. No code needed. Needs the updated sync server.
-Notifications play the dice-call sound.
-Added character portraits: add a square image in Free-form edit (with a crop overlay), shown on the Sheet tab, the character bar and the character browser. Portraits sync and share separately from the sheet, so editing a sheet never re-sends the picture. Needs the updated sync server.
-Added the Thin Blood template (5/3/1 Attributes, 11/6/3 Abilities, 3 Virtue dots, no freebie points). Always Caitiff, never takes the Generation or Status Backgrounds, and always has the Fourteenth Generation and Thin Blood Flaws, or the Fifteenth Generation Flaw, picked in Finishing touches or by the Random Character Generator.
-Fourteenth Generation, Fifteenth Generation and Thin Blood Flaws now apply: Spend, Boost and Celerity cost double blood, Fourteenth Generation can't use its last 2 blood for them, and Fifteenth Generation keeps Disciplines at 3 or less.
-Removed the Ghoul and Mortal templates until they're implemented.
-Initiative Tracker Changes:
	-Removed Call Roll: every roll made in a room now goes to the room's roll history. The host's show as the Storyteller, a joiner's as their character in the tracker (the one active in the Characters module if they have several).
	-Joiners can open the roll history and see each outcome; the host also sees each die (hover when there are too many to list).
	-Added Hide Roll (next to the roll buttons while in a room): rolls made with it on stay private. It turns off when you leave the room.
-Character Manager Changes:
	-Added Show Progression (Sheet tab, next to Play and Free-form edit): colours each dot by how it was gained, Base, Freebies or XP.
	-Backgrounds, Merits and Flaws that aren't in the book can have their own hover text, set in their note dialog and kept separate from the note.
	-The XP log can be collapsed, and shows the latest 10 entries with pages for older ones.
	-Added Deterioration (third mode next to Play and Free-form edit): lower a trait after story events, at no cost. It's noted in the XP log, and Show Progression shows how many dots each trait lost.
	-Added Planning (next to Spend XP): plan raises on the sheet in the accent colour without changing anything, then review, reorder and confirm them one dot at a time in XP Plan, with the total XP needed and how much is missing.
	-The sheet always goes back to Play when you leave the Sheet tab, and Free-form edit is never saved or synced.
	-Every section of the Details tab can be collapsed, and so can each Expanded Background; hovering a collapsed one shows the start of its details.
	-Added Derangements to the Details tab: pick one from the book (its text is read from the rulebook, with a page reference) or write your own with its own hover text. Each one collapses, showing a summary on hover.

V2.8
-Added Goon HP to the New Character overlay: the character only has 4 Health Levels (Hurt -1, Wounded -3, Crippled -5, Incapacitated). The Aggravated Penalties setting still applies.
-Fourteenth and Fifteenth Generation blood is no longer locked: past their threshold (the last 2 blood for Fourteenth, the last 4 for Fifteenth, so Fifteenth only has 6 usable) the boxes turn gold with a note on what it can't power, but it can still be spent.
-Fourteenth Generation keeps Disciplines at 4 or less.
-The Random Character Generator no longer equips the weapons it gives; armor still starts equipped.
-Initiative Tracker Changes:
	-Removed the Neither option for Actor Type: leaving both Player and Enemy unticked means no Actor Type.
	-The Actors list is now the Character Browser itself, in the same spot, with Original and Duplicate buttons on each character (Add to encounter when joining a room).
	-Hide Roll is now a thinner eye button.
	-Hovering "X watching" while hosting shows who is watching. Needs the updated sync server.
-Character Manager Changes:
	-The character browser's ⋯ menu can add, change or remove a character's picture.
	-Sections of the Details tab can be moved up and down in edit mode.
	-XP Plan keeps a trait's raises in order: a lower raise can't go below a higher one of the same trait, moving one brings the others along.
	-A portrait can be added in the first step of Guided creation.
	-Each Discipline on the Disciplines tab can be collapsed.
-The Rule Book's search settings use toggle switches like the main settings.
