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

V3.0
-Added Goon HP to the New Character overlay: the character only has 4 Health Levels (Hurt -1, Wounded -3, Crippled -5, Incapacitated). The Aggravated Penalties setting still applies.
-Added a Dossier tab to characters (between Story Progression and Tracker), where you can create a Note Board: a corkboard of pinned notes you can drag around, tie together with red string, give shapes and colours, and collapse to their title.
	-Containers hold other notes, and collapsing one hides everything inside it.
	-Strings come in several colours (new strings take the last colour used). They run over the notes they cross, and fade over whatever you hover.
	-Text can be written straight on the board, then moved, resized and turned, in the titles or details font.
	-Right-click the board (or press and hold) to add things, and right-click anything on it for its shape, colour, font, strings and so on; double-click anything to edit its text.
	-The board syncs on its own, apart from the rest of the character, with room for a couple of thousand notes.
	-Strings can carry a label (double-click a string, or right-click it).
	-Notes can be stamped Final Death, Torpor, Missing, Diablerized, Blood Bound, Ally, Enemy or Suspect.
	-Search the board: everything else dims, and Enter zooms to what's found (Ctrl+F).
	-Select several things with Shift-click, Shift-drag a box or Ctrl+A, then move, recolour, reshape, stamp, collapse or delete them together.
	-Undo and redo (Ctrl+Z / Ctrl+Y, or the arrows by the zoom).
-Added Privacy to shared characters: once a character is shared with a Viewer, everything on it is private to view-only people until you choose what they see. People who can edit always see everything.
	-The Privacy button (next to Sharing) has presets: Name only, Identity, At the table, Character sheet and Everything.
	-Or pick on the sheet itself: tabs, sections, subsections, single fields and board notes can each be made visible or private; making something private takes back what was picked inside it.
	-View-only people get the sheet with the private parts taken out, and they stay off the character's card too (clan, generation, blood, willpower, humanity, XP...).
	-A room's host still sees the whole sheet of a character added to the encounter.
	-Needs the updated sync server.
-Added account tiers: Guest, Player and Storyteller, shown as a badge next to usernames.
	-New accounts start as Guests: they get the Roller and Rule Book (saved on their device) and can request access, with an optional note, from Characters or Initiative. Accounts made before this are Players.
	-Storytellers can share up to 50 characters; Players can share 10.
	-Rooms need an account with access, and the host sees each watcher's tier.
	-A banned account only shows that it's banned (and why) until it signs out.
	-Needs the updated sync server and its database update.
-Settings > Account has Sign out everywhere, which signs the account out on every device and closes its open shared sheets and rooms.
-Rooms are now by invitation, with no codes to type: hosting opens a Room window to invite friends, and Invite friends adds more later.
	-Invited friends get a notification with Join, and can join from the Friends menu for as long as the room is open (after losing the connection too). Nobody else can join.
	-Friends no longer get a notification whenever someone they know hosts a room.
	-An account can be in one room at a time: joining from another device takes it out of the room on the first one.
	-Everyone in a room can see who's in it.
-Players can use one of their characters' pictures as their profile picture (Settings > Account). It shows next to their name for friends and other players.
-Added the Skirmish Map to the Initiative Tracker: a live, rough picture of where everyone stands in the encounter, shared with the whole room. Open it with the Skirmish Map button next to Actors list; it takes the Actors list's spot.
	-Each character is a token about 1 yard/metre across, showing their portrait or initials. Enemies that haven't been revealed show as E1, E2 and so on. Hover a token for its name and details.
	-Drag a token to move it; everyone sees it move, and who's moving it. Watchers can move their own characters, and the host can move anything (or let watchers move any token).
	-While you drag, rings show your running speed and half of it (to move and still attack).
	-Moves leave a faint line for the round; hover one to see it and its distance. Small corrections (within 1 yard/metre) redo the last move instead of adding one, and clicking a line lets you undo that move and any after it.
	-Tokens close enough to touch within 1 yard/metre are linked as engaged in melee, and dragging shows when you'd be engaging or leaving melee.
	-Tokens that have lost half or more of their health show claw marks and blood.
	-Click a token, then a spot or another token, to measure the distance for everyone.
	-Hover a token for its health (and blood and willpower for the host). Watchers see speeds for player characters, and only a rough wound state for others.
	-Speeds on the hover card follow wounds: Wounded can only walk, Mauled can hobble 3, Crippled can crawl 1, and Incapacitated is Downed.
	-The cog has the map's settings: the host picks Metric or Imperial for the room (1 yard = 1 metre = 3 feet), and everyone can turn the grid off or change how strong it is.
	-Everyone can also pick their own background: Grimy tabletop, Aged parchment, Night street or Elysium marble, or let it match light/dark mode.
	-Right-click a token (or press and hold it) to give it an Area of Effect (watchers can only use their own characters, unless the host lets them move any token): a radius from the token's edge, a description, a colour, and whether everyone sees it or only you and the host. It moves with the token, stays faint until you hover it (then shows its description), and areas can overlap.
	-Needs the updated sync server for watchers to see portraits.
-Fourteenth and Fifteenth Generation blood is no longer locked: past their threshold (the last 2 blood for Fourteenth, the last 4 for Fifteenth, so Fifteenth only has 6 usable) the boxes turn gold with a note on what it can't power, but it can still be spent.
-Fourteenth Generation keeps Disciplines at 4 or less.
-The Random Character Generator no longer equips the weapons it gives; armor still starts equipped.
-Initiative Tracker Changes:
	-Removed the Neither option for Actor Type: leaving both Player and Enemy unticked means no Actor Type.
	-The Actors list is now the Character Browser itself, in the same spot, with Original and Duplicate buttons on each character (Add to encounter when joining a room).
	-Hide Roll is now a thinner eye button.
	-Hovering "X watching" while hosting shows who is watching. Needs the updated sync server.
	-Starting or ending an encounter clears the roll history for everyone in the room.
-Character Manager Changes:
	-The character browser's ⋯ menu can add, change or remove a character's picture.
	-Sections of the Details tab can be moved up and down in edit mode.
	-XP Plan keeps a trait's raises in order: a lower raise can't go below a higher one of the same trait, moving one brings the others along.
	-A portrait can be added in the first step of Guided creation.
	-Each Discipline on the Disciplines tab can be collapsed.
	-The Quick Reference shows movement per turn (walking, jogging and running in metres/yards, with Celerity), slowed by wounds.
	-Export can save several characters at once (tick the ones you want), and Import shows what's in the file first: untick any to skip, and for one you already have, choose to overwrite it or add it as a new [Copy].
-The Rule Book's search settings use toggle switches like the main settings.
-Each version in the Changelog can be folded open and closed; only the newest starts open.

V3.1
-Skirmish Map Changes:
	-Tokens are engaged in melee when their edges are within 1 yard/metre of touching.
	-Tokens can't overlap: at most their edges touch.
	-Measuring from a token starts at its centre and ends at the other token's nearest edge (or the spot picked), and snaps to the token under the pointer.
	-During an encounter, moves count against a token's speed for the round. The rings show what's left (running speed, and half of it), dragging stops at the limit, a token with nothing left can't move, and "Over Half" shows once it passes half its running speed.
	-A token's first move of a round that's shorter than 1 yard/metre (and doesn't engage anyone) is undone instead of counting.
	-Before an encounter starts, moving tokens leaves no path and has no speed limit.
	-Hurt tokens only show blood along their bottom edge (no more tint or claw marks), so the portrait stays clear.
	-Labels no longer cover each other or the token being moved; the distance being moved gets out of the way.
	-Dragging a token past the edge of the map moves the view along with it.
	-Added a Full screen button.
	-The mouse wheel zooms the map.
	-Escape while dragging a token puts it back.
-Initiative Tracker Changes:
	-Each actor's wound state (Unhurt, Hurt, Injured and so on) shows next to their name for everyone in the room; the host also sees their health levels left.
-Character Manager Changes:
	-Dossier: the note being edited shows above everything else on the board.
	-Dossier: new notes use the shape and colour you last picked for a note (remembered on each device).
	-Dossier: a note's title is optional; a note without one shows just its details.
	-Dossier: a collapsed note leaves room for its stamp.
	-Dossier: containers are picked up by their title; dragging anywhere else inside one moves the board.
	-Dossier: when a selection is dragged and the note you're holding lands in a container, everything selected goes into it.
	-Dossier: searching marks the matching words inside the notes.
	-Dossier: containers size themselves to fit what's in them, growing and shrinking as notes go in, come out or change size (an empty container keeps its size and can still be resized by hand).
	-Dossier: a note stays in its container until its middle is dragged out twice the note's width away from it; closer than that, the container stretches to follow it. Dropped into a different container, it goes straight in. While dragging, the container it would go into glows and the one it would leave fades.
	-Dossier: notes and containers no longer stack: dropping one on another pushes the one underneath out of the way, a container that grows pushes its neighbours, and a new note finds a free spot.
	-Dossier: Ctrl+click (Cmd+click on a Mac) a note or container to fit it on screen (zooming in up to 125%); Ctrl+click an empty spot to fit the whole board.
	-Dossier: string labels run along their string, on its upper side (the right side for upright strings), and never upside down.
	-Dossier: text can be resized by dragging its corner down as well as sideways.
	-Dossier: diamond and hexagon notes only react to the pointer inside their shape, so you can grab what's behind their corners.
	-Dossier: the right-click menu has a Size row with − and + buttons (the menu stays open while you click them): notes and containers go from 50% to 200%, text changes letter size. Works on several selected things at once.
-Fixed duplicates in the Initiative tracker losing their sheets, and health changes not sticking, when the page was closed (or a phone switched away) right after a change. A duplicate whose sheet is missing is now made again from its original.

V3.1.1
-Skirmish Map Changes:
	-Bashing damage no longer sets a character's wound state on the map: speed limits and the wound marks only count lethal and aggravated damage (bashing counts once it spills over into lethal on a full health track).
	-Map settings have a Background marks switch and a Marks opacity slider, to fade or hide the stains and marks on the background without changing its colour (your own view only).
-Initiative Tracker Changes:
	-The wound word, and the health left shown to the host, only count lethal and aggravated damage.

V3.1.2
-Character Manager Changes:
	-New Rage button under the Blood Pool on Active Play: spend 1 blood (2 for thin blood, still 1 towards the turn's limit) to ignore wound penalties, both dice and movement speed, for the rest of that round. It only works during an encounter in the Initiative tracker, once per round.
	-Quick rolls of a Virtue, Willpower or Humanity/Path no longer take wound penalties (soak never did).
-Skirmish Map Changes:
	-A raging character moves at full speed this round, for everyone in the room; the hover card says so.

V3.1.3
-Fixed Thaumaturgy and Necromancy paths (the primary path's name and secondary paths) being wiped on shared sheets, and on the host's copy of a joiner's sheet in a room.

V3.1.4
-Character Manager Changes:
	-Dossier: text can be attached to a note or container (right-click the text, Attach to…, then click the note or container). There's no string: the text keeps its place next to it, moving with it and hiding when it's inside a collapsed container. Detach it from the same menu; deleting the note leaves the text loose. A selected text shows what it's attached to with a dashed outline.
	-Dossier: a container's title and details are never covered. Notes and containers inside it move down below them, including when the details get longer, and the container sizes itself around them.
	-Dossier: containers no longer have a size limit; they grow as far as what's inside them needs.
	-Dossier: dragging a text's corner now resizes its text box (width and height) without changing the letter size; letter size is set with the Size row in its right-click menu.
	
V3.1.5
-Character Manager Changes:
	-New CQM button on Active Play, left of Soak and Defend: Close Combat Maneuvers (Bite, Claw, Clinch, Disarm, Hold, Kick, Strike, Sweep, Tackle). Each shows its traits, difficulty and damage; picking one rolls the attack in the main roller and readies its damage in the Damage module.
	-Low Generations raise the trait maximum past 5, while a character is being made too: 7th Generation up to 6, 6th up to 7, 5th up to 8, 4th up to 9, and 3rd (now selectable) up to 10.

V3.1.6
-Character Manager Changes:
	-Randomly generated fighters (Bruiser, Gunner) always have at least 2 dots in the skill for what they fight with: Brawl for claws or fists, Melee for blades and clubs, Firearms for guns.
	-Randomly generated characters start with a full blood pool and full Willpower.
	-The Soak window has a "Wear armor for this soak" box: untick it to leave your armor out of that one roll (it's ticked again next time).
	-Dossier: Shift-dragging a box adds what it catches to the selection; if everything it caught was already selected, it deselects them instead. Shift-click still adds or removes one at a time.
-Initiative Tracker Changes:
	-Incapacitated characters don't roll initiative and are skipped by Next turn; they're listed at the bottom and roll again at the start of the next round once they're back up.
	-New "Show on map" in each actor's right-click menu: opens the Skirmish Map centred on that actor.
-Skirmish Map Changes:
	-Fit leaves out Incapacitated tokens (unless everyone's down).
-Fixed tier badges being squished or cut off next to long names in Friends and the Share window.

V3.1.7
-Character Manager Changes:
	-The Soak window's "Wear armor for this soak" option is now a switch, like the ones in Settings.
-Fixed syncs interrupting you: changes arriving from another device, a shared sheet or a room now wait while you're typing, pressing or dragging, or have a menu open, and show up as soon as you're done. This covers the Dossier (dragging the board or notes, editing, menus), character sheets, the Initiative tracker's rows and menus, Friends, and Settings > Account.

V3.1.8
-Character Manager Changes:
	-New Temp Mod button on Active Play (far right, level with CQM, Soak and Defend): give a character temporary bonuses or penalties to any Attribute, with an optional short note. They count right away in every roll, soak, damage, movement and initiative that uses the Attribute, show on the button (with how many are in effect) and next to the Attribute on the sheet, and stay until you remove them with the X in the list.
	-CQM, Soak and Defend now fit on one line.
-Initiative Tracker Changes:
	-A blood boost or Temp Mod to Dexterity or Wits during a round applies to everything at once, but only moves the character in the initiative order when the next round starts.
	-Boosted dots above your Generation's limit (6 for 8th Generation and above, up to 10 for 4th and lower) last 3 rounds from the round they're bought, each purchase on its own clock; dots up to the limit last the whole encounter.

V3.1.9
-Skirmish Map Changes:
	-Right-clicking a token (or pressing and holding it) now opens a token menu instead of going straight to areas of effect; pick "Areas of effect…" there. More options will join it.
	-Everyone can see a character's equipped weapons and worn armor when hovering over its token.
	-New "Pop out" button (not on phones): the map becomes a floating window you can drag by its title bar anywhere in the browser and resize from its corner; "Dock" puts it back. Its spot and size are remembered on each device.
	-New "Detach" button (Supported browsers on a computer): the map moves into its own window that stays on top of everything, even other apps, and can go anywhere, another screen included. "Reattach" (or closing that window) puts it back; its size is remembered.
	-A popped-out map stays on screen while you switch to Damage, Probability or the Characters view; before, it hid until you came back to the tracker.
	-Pop out, Dock, Detach and Reattach are now icon buttons like the settings gear (hover one for its name). A popped-out or detached map leaves out the Full screen button and the instructions under the map.

V3.1.10
-Skirmish Map Changes:
	-Fixed the detached map's buttons only reacting along their bottom edge in Opera.
	-Opening the Actors list no longer closes the map. A docked map steps aside while the list is open and comes back, as you left it, when the list closes (or press Skirmish Map); a popped-out or detached map stays put.

V3.2
-Character Manager Changes:
	-Dossier: new Edit switch at the top of the board. A new board starts with it on; whenever you leave the Dossier (another tab, another character or the Roller) it goes back to off. With Edit off nothing on the board can be added, moved, resized, changed or deleted, and right-clicking does nothing, so it's safe to browse; dragging the board, zooming, search, collapsing and expanding containers and Ctrl+click to fit still work.
	-Dossier: when something is dropped on a group of things sitting close together, the group moves out of the way together, keeping its layout, instead of being scattered (unless that would mean a much longer move).
	-Dossier: string labels no longer cover each other; one that would slides along its own string until it's clear.
	-Dossier: strings bend around notes, containers and other strings in their way when a modest curve does it.

V3.2.1
-Character Manager Changes:
	-Dossier: strings can now weave between notes and containers in their way, leaving a note from whichever side suits and snaking around what's in the way. A gentle bend is still used whenever that's enough; the weaving path is only for when it isn't.
	-Dossier: something dropped between other things now gets room of its own: each thing it lands on makes way on its own side, and whatever sits close to that thing moves with it, keeping its place, while everything else stays put. Before, everything nearby moved off together as one block.
	-Fixed a Dossier element taken out of the selection with Shift-click staying highlighted until something else was Shift-clicked.

V3.3
-Skirmish Map Changes:
	-New "Hide" in a token's menu (right-click it, or press and hold). The host can hide any token; someone who joined can hide their own. A hidden token, along with its moves, measurements to and from it, and the areas of effect following it, is only shown to the host and the token's owner. "Unhide" shows it to everyone again.
	-"Visible to…" (under Hide) picks who else in the room can see a hidden token; nobody else by default.
	-Those who can see a hidden token see it faded, with a dashed ring and a small crossed-out eye; its hover card says who can see it.
	-New "Add hidden" switch in the host's Actors list: actors added while it's on (from the list, the tracker's Add button or a preset) start hidden on the Skirmish Map, so they can join an encounter already under way without anyone else seeing them.
	-A dragged token passes over hidden tokens (which still stop it at visible ones); dropped on a hidden token, it's nudged to the nearest free spot, but never further than the movement it has left.
-Character Manager Changes:
	-Dossier: with Edit off, the board can be dragged from anywhere, notes, containers and strings included (a click without dragging still selects what's under it).
	-Fixed Dossier strings sometimes hooking or looping back as they reached a note: they now come straight in to the nearest point of its edge, and can slip through narrower gaps between notes instead of going the long way around.
-Initiative Tracker Changes:
	-People who joined only see player characters until an encounter starts; everyone else (in the tracker and on the Skirmish Map) appears once it does.
	-Actors hidden on the Skirmish Map also stay out of the tracker for those who can't see them, until someone who joined has seen them; from then on they stay in the tracker, even if hidden again.
	-"Enemy [n]" numbers are handed out in the order enemies are first seen by those who joined, so a hidden enemy leaves no gap in the numbering.

V3.4
-Chronicles (Storytellers and Admins):
	-New "Chronicles" tab, next to Roller and Characters: your chronicles as cards (title and description). Make new ones; rename them; deleting one asks twice.
	-Players: invite friends to a chronicle. They get a notification and accept or decline it; once in, they put their own characters in from the sheet. Each player shows with their characters; you can remove a player, or take a character out.
	-Characters in a chronicle are shared with its Storyteller automatically, as an editor. Automatic shares don't count towards the player's sharing limit.
	-Right-click a character there (or use ⋯) to mark it Missing, Unavailable or Final Death, or clear the mark.
	-"Your characters here": add your own characters (or ones shared with you) to a chronicle's Players tab.
	-Notable NPCs: sections you make, rename, reorder and delete, each holding your own characters (or ones shared with you), with the same marks.
	-Grand Dossier: a Dossier board for the whole chronicle, holding about 2.5 times as much, with character cards (portrait and name) that open the sheet (right-click the board, Add a character…).
-Character Manager Changes:
	-The sheet's Chronicle field: in a chronicle you've joined, "Assign…" puts the character in it. While it's in one the field shows the chronicle's title, locked (it follows renames); in several it shows "N Chronicles", listing them on hover. Taking it out unlocks the field, keeping the last title, and ends the automatic share.

V3.4.1
-Chronicles Changes:
	-A character is either in the Players tab or a Notable NPC, not both: each list's "Add a character" leaves out the other's.
	-"Add a character" in the Players tab and Notable NPC sections opens the character browser, with an Add button on each card; characters already in the chronicle say so instead.
	-The Grand Dossier's "Add a character…" lists only the chronicle's own characters (players' characters, yours in it, and the Notable NPCs, by section), with a search.
	-Fixed the Grand Dossier: turning Edit on or off could leave the board unresponsive (no dragging, the browser's own right-click menu, a switch that wouldn't turn off), and Edit could turn itself off after a while.

V3.5
-Skirmish Map Changes:
	-New "Draw" button (a pencil) in the map's header, with a drawing toolbar: free-hand, line (Shift: steps of 45°), rectangle (Shift: square), circle (Shift: perfect circle), path (click each point; double-click or Enter finishes) and erase (click a shape, or drag over several). Six colours and three thicknesses. The hand tool goes back to moving the map and tokens.
	-The toolbar is one row: the tools, then the pen button (colour, thickness, and the "Sizes" switch, which shows lengths and sizes while drawing and resizing) and ⋯ (Copy, Paste, Delete, Presets… and Maps…).
	-Select tool: click a shape (Shift-click for more, or drag a box); drag to move, the corner handle to resize. Copy, Paste and Delete (also Ctrl+C, Ctrl+V, Delete; Ctrl+A selects everything). Picking a colour or thickness changes the selected shapes.
	-Presets…: save selected shapes to use again, and place them in the middle of the view. Maps… (host): save the whole drawing, and load it back (it replaces what's drawn, after a second click). Presets and maps are saved to your account.
	-Only the host draws, unless they turn on "Watchers can draw" in the map's settings. Everyone in the room sees the drawing, including people who join later.

V3.5.1
-Skirmish Map Changes:
	-Undo and Redo (buttons, or Ctrl+Z and Ctrl+Y): your own drawing changes, including placed presets and loaded maps.
	-Select tool: right-click for Copy, Paste, Delete and Presets….
	-Placing a preset: it follows the pointer and is only put down where you click (Escape or a right-click cancels).
	-The middle mouse button always drags the map, whatever tool is on. The pointer shows the tool in use.
	-The browser's own handling of presses on the map (selecting text, dragging the picture, middle-button scrolling) is off.
	-Imperial units: Feet and Yards switches (side by side, under it). With both on, sizes show as before (feet, with yards beside them); with one, only that unit.
	-Fixed Delete not removing selected shapes until you'd right-clicked the map first.

V3.6
-Skirmish Map Changes:
	-Shift-click keeps a preset on the pointer after putting it down, so you can place several; letting go of Shift stops.
	-Paste now works like a preset: the copy follows the pointer until you click to put it down (Shift-click for several).
	-Path tool: Shift keeps each new segment to steps of 45°, like the Line tool.
	-Ctrl snaps lines, rectangles, circles and path points to other shapes near the pointer: ends of lines and paths and the corners of rectangles first, then anywhere along a shape. It works for a shape's starting point and while you draw it; a small ring shows where it will snap.
	-Select tool: the right-click menu has colour and thickness choices for the selected shapes (it stays open, so you can change both; the pen keeps its own).
	-Alt snaps to the grid: line, rectangle, circle, path and text points land on the nearest grid corner, and moving shapes or placing a preset puts their corner on one.
	-Fills: rectangles, circles and closed paths can be filled with a see-through version of their colour (the Fill switch in the pen, or for selected shapes in the right-click menu).
	-Line styles: solid, dashed or dotted, in the pen and in the right-click menu.
	-Hidden shapes: the host can hide shapes from players (the Hidden switch in the right-click menu), or turn on "Draw hidden" in the pen for new ones. Hidden shapes show faded for the host, and players never get them until they're shown.
	-Text tool: click to write a label on the map (Enter keeps it, Escape cancels); the thickness picks its size. Click a text with the Text tool, double-click it with Select, or use "Change text…" to change it.
	-Select tool: the right-click menu can rotate the selection a quarter turn either way, or flip it left to right or top to bottom.
	-Ctrl+D duplicates the selection (the same as Copy then Paste); also in the right-click menu and More.
	-Path tool: clicking the first point again closes the path into a shape (the point turns green when you're on it).
	-Fixed Escape in the right-click menu clearing the selection instead of closing the menu.
	-Walls: any shape but a text can be a wall (the Wall choice in the pen, or for selected shapes in the right-click menu): Solid, Half, Window or Door, each with its own look.
		-Solid walls block sight and movement. Doors do too, until opened. Windows block movement but not sight, until broken. Half walls block neither, but a measurement across one turns orange past it and says "cover"; across a wall that blocks sight it turns red and says "no line of sight".
		-Anyone can right-click a door to open or close it, or a window to break or mend it.
		-A wall drawn on top of part of another takes over just that part: a door drawn over a stretch of a solid wall makes only that stretch a door.
		-Tokens can't be dragged through walls that block movement; they slide along them instead.
		-Players only see the tokens their own tokens can see, with a fog over the rest of the map. The host sees everything.
		-Hidden walls only count for the host, so a hidden door drawn over a wall stays a plain wall for players until it's shown.

V3.6.1
-Skirmish Map Changes:
	-A move's line follows the way the token actually went, pulled tight around walls that block movement: it bends at the corner nearest to where it has to (a token's width clear of it), and its length is the distance moved (and what counts against the token's speed).
	-Fixed a token being dragged when the window lost focus (the Windows key, Alt+Tab) or the mouse button was let go outside it: the move wasn't kept, and the token's new spot became where its movement started from. The drag now ends there as a normal drop.

V3.6.2
-Skirmish Map Changes:
	-Fixed a move's bends making it impossible to go back: dragging the token back near the last bend now takes that bend away.
	-The speed rings while dragging follow a move's bends: they're centred on the last bend, smaller by the distance it took to get there, so they show how far the token can really still go.

V3.6.3
-Skirmish Map Changes:
	-A move's bends now go away as soon as they're no longer needed (when the way straight past a bend crosses no wall), not only when the token is dragged back near them.

V3.6.4
-Skirmish Map Changes:
	-Fixed a move's line cutting through a corner where two walls meet (dropping a bend it still needed, like one through a broken window): a bend now only goes when every wall at the corners either side of it still lies inside the line's turn.

V3.6.5
-Skirmish Map Changes:
	-Fixed a move's bends not going away at some corners (like after going round a building's corner and back): a move's line is now pulled tight like a string around the walls, a token's width clear of them, so it's the shortest way that still goes round each wall on the side the token did. Rounding a corner shows as a few short bends hugging it.

V3.7
-Skirmish Map Changes:
	-Pings: press Tab with the pointer over the map to ping that spot. Everyone sees a pulse with your name and hears the notification sound, a little faster (even with the app's sounds off; muting the browser tab silences it). Tab works as usual anywhere else, or while typing.
	-Fog of war: players now see nothing of the map their tokens can't see (shapes, walls, areas, measurements, everything), not just the tokens. What they've seen before stays, dimmed (also after a reload).
	-Last known position: when a token goes out of a player's sight, or is hidden in front of them, a faint marker stays where they last saw it. It goes when they see the token again, when they look at that spot again after looking away, when the encounter ends, or when they right-click it and choose Forget.
	-Settings (host): "Players forget the map" clears what every player (and every token) remembers seeing, and their last known positions.
	-Token view (host): the eye button, or Space with the pointer over the map, shows the map as one token sees it: the last token you picked up, or a player's token someone else just moved (named in the map's corner). It has the same fog, remembered parts and last known positions a player gets. Every token keeps its own memory all along, so turning Token view off (to see everything) and back on finds it as it was.
-Friends Changes:
	-The friends list is split into Online and Offline (online friends get a green dot). A friend counts as online while they have the app open.

V3.7.1
-Skirmish Map Changes:
	-What a token learns while it's dragged (parts of the map seen, last known positions made or cleared) only counts once the move is dropped. Cancelling the drag, or undoing the move later, forgets it (and brings back any marker it cleared).
	-Token view: clicking tokens to measure doesn't change whose eyes you're using; only moving one does.

V3.7.2
-Skirmish Map Changes:
	-A move only teaches a token what it sees where it's dropped: whatever it glimpsed on the way (parts of the map, tokens) is forgotten, so dragging out and back reveals nothing.
	-Last known positions about a token being moved wait for its drop too, and undoing a move takes back what it changed for everyone watching it.
	-Fixed last known positions staying after a move was undone.
	-Token view (host): every token stays visible, but those the chosen token can't see are dimmed. Clicking a token sees through it (except the click that finishes a measurement).
	-Tokens can't be engaged through a solid wall, an intact window or a closed door.

V3.7.3
-Room Changes:
	-Fixed rooms closing when the host reloaded the page: the page tried to take its room back before the account had signed in, so it was refused and gave the room up.
	-The room now waits two minutes for a host who lost the connection or reloaded (watchers are told the host is away, instead of being dropped), and the host's page keeps trying to reconnect.
	-Watchers who lose the connection rejoin by themselves, and a reload takes them back into the room.
	-A heartbeat notices a connection that quietly stopped working, and reconnects right away instead of waiting for the browser to notice.
	-Rejoin room: when the connection to a room is lost for good, a Rejoin button (for the host, if the room is still open; for a watcher, if it still exists) takes them back in.

V3.7.4a
-Skirmish Map Changes:
	-Once a move is dropped, the token learns from its whole path (the move's line, bends and all), not only where it ended: what's seen from along it is remembered, and tokens it saw on the way get a last known position if they're out of sight from where it stopped. Undoing the move takes it all back.
	-Fixed a player keeping a new last known position for a token whose move was undone: if a token behind a wall moved into sight and the move was undone, the player kept a marker where it had briefly been, instead of the one behind the wall they knew of before.
	-Fixed undone moves not taking back what they revealed (remembered map, last known positions) after the page had been reloaded: everything a token knows, and which move taught it, is now kept past a reload.
	-Token view (host): the token you were seeing through is kept past a reload.
	-Fixed a player's token keeping what it saw during a move the host made for it (remembered map, last known positions) after the host undid that move: a move the host (or anyone else) makes with a player's token is now taken back like the player's own, it learns from the path it was moved along, and a move the host picks up and cancels teaches nothing.
	-Fixed undone moves sometimes keeping what they revealed (remembered map, last known positions), seemingly at random: a token moved while another had just been nudged (or put back) could have its discoveries counted toward the wrong move and kept for good; an undo made right after a player dropped their token was missed while their page still showed it where they dropped it; and a second move made quickly after the first could go unrecorded.
	-What changes about a token that just moved (it comes into sight, or its last known position is cleared) now always belongs to that token's move, so undoing that move takes it back, whoever is watching.
	-Smaller initials on tokens (and on last known positions), so they fit inside the token; three-letter ones are smaller still.
-General Changes:
	-Fixed friends not changing between Online and Offline: closing the app now shows you offline to friends right away (instead of minutes later), coming back to the tab shows you online again, and the Friends list looks again every 15 seconds while it's open.
-Chronicles Changes:
	-Fixed a player who accepted a chronicle invitation still showing as "invited, hasn't answered yet", and their characters not showing in it, until the page was reloaded: an open chronicle now picks up answers and characters put in (or taken out) within seconds.

V3.7.5
-Skirmish Map Changes:
	-Fixed the Skirmish Map going dark and showing nothing in Firefox once walls that block sight were placed: the fog now only covers what's in view, instead of a huge area Firefox couldn't draw.

V3.8
-Dossier Changes (Character Dossiers and the Chronicles' Grand Dossier):
	-Images: notes can now hold an image. Right-click the board and choose Add image…, paste an image onto the board, or drop an image file on it; right-click a note to add, change or remove its image.
	-Images are shrunk before uploading (at most 1600 px; a photo's location data is dropped) and kept on the server, so they don't make the Dossier bigger. Once seen, they're kept on the device and show without a connection.
	-Who sees them: on a Character Dossier, whoever can see that character (its owner and the people it's shared with); on a Grand Dossier, its Storyteller.
	-Each account has room for 50 MB of images (Storytellers: 250 MB). An image no Dossier uses any more is deleted a week later, so undoing its removal still brings it back.
	-Duplicating a character keeps its Dossier's images; deleting a character or a chronicle lets go of them.
	-Images need you to be signed in. Rulebook pages don't belong here: images are synced.
	-Fixed undo and redo on a Grand Dossier not being saved to the chronicle.
