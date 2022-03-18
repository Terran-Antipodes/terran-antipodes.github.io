# GameTracker

This website is an SPA intended to provide a non-commercial aid while playing the [Lord of the Rings LCG](https://www.fantasyflightgames.com/en/products/the-lord-of-the-rings-the-card-game/) from [Final Flight Games](https://www.fantasyflightgames.com/en/index/).

- [GameTracker](#gametracker)
  - [Rights and Permissions](#rights-and-permissions)
  - [Using the GameTracker](#using-the-gametracker)
    - [Purpose](#purpose)
    - [Screen Elements](#screen-elements)
    - [Getting Started: New Game tab](#getting-started-new-game-tab)
    - [Help](#help)
    - [Side Tabs](#side-tabs)
      - [Options tab](#options-tab)
      - [About tab](#about-tab)
      - [Back tab](#back-tab)
      - [Load/Save](#loadsave)
      - [Skip tab](#skip-tab)
      - [Elimination](#elimination)
      - [Out Of Sequence Enemy Attack](#out-of-sequence-enemy-attack)
      - [Out Of Sequence Player Attack](#out-of-sequence-player-attack)
    - [Options](#options)
        - [Display the Compendium Rules as](#display-the-compendium-rules-as)
        - [Show Tooltips](#show-tooltips)
        - [Sequence Options](#sequence-options)
    - [Version](#version)
  - [Version History](#version-history)
      - [v2.0.1](#v201)
    - [v2.0.0 Feature Complete Release](#v200-feature-complete-release)
    - [Earlier versions](#earlier-versions)

## Rights and Permissions
This GameTracker webpage is the property of Clive Pottinger. Email any comments or concerns to terran.antipodes@gmail.com.
All displayed images, arts, fonts and The Lord of The Rings: The Card Game are copyrighted at © Fantasy Flight Games.  
The copyrightable portions of The Lord of the Rings: The Card Game and its expansions are © 2011 - 2020 Fantasy Flight Publishing, Inc.  
The Lord of the Rings, and the characters, items, events and places therein are trademarks or registered trademarks of The Saul Zaentz Company / Middle-earth Enterprises and are used, under license, by Fantasy light Games. Living Card Game, LCG, LCG logo and Fantasy Flight Supply are trademarks and/or registered trademarks of Fantasy Flight Publishing, Inc.  
All Rights Reserved to their respective owners.<br /> 
The Rules Compendium and Rules Companion are the intellectual property of, and used by the permission of, Mathieu Martin. 

## Using the GameTracker

### Purpose
I created the GameTracker when my wife and I started playing Lord Of The Rings LCG. There was a lot to learn and every time we had to clarify a rule we ended up reading cards, thumbing through rule books, and scouring the web. We often forgot where we were in the game and what to do next. So, I created the first GameTracker to help us remember.

Over time the GameTracker evolved, and new features were added (and some removed). But I have tried to keep the purpose the same: to guide players through the sequence of steps in the game. The tracker does not help with how to use cards, how to interpret rules, or even what the players' threat levels are. It's only purpose is to let players know what is the next step in the game. 

### Screen Elements

When the GameTracker is opened, the following elements should be visible:
  - Background images: a set of pictures from the LOTR LCG site that scroll with the page
  - The Sequence image: shows all phases and steps of regular game-play starting with the "I. Resource Phase" and ending with "7.5 Refresh phase ends".
  - Side tabs: coloured rectangles that expand when hovered over to allow various actions.
    - Initially, the visible side tabs should include:
      - [*New Game*](#getting-started-new-game-tab) (green)
      - [*Options*](#options-tab) (teal)
      - [*About*](#about-tab) (yellow)
      - [*Load/Save*](#loadsave-tab) (fuscia - at the bottom of the screen)
    - If you have already started a game, then other side tabs may also be visible.
  - Main Dialogue: this won't be visible unless you have started a game.
  - Pop ups: these will appear when certain side tabs are clicked on ([*Options*](#options-tab), [*About*](#about-tab), [*Load/Save*](#loadsave-tab)).
  - Version number: appears in the bottom left corner.

### Getting Started: New Game tab

Simply move to the [*New Game*](#getting-started-new-game-tab) side tab and click on it. The Main Dialogue will appear and guide you through setting up a game.

The player's progress throughout the game is recorded in the browser's internal storage. So if the players leave this site and return, it should resume exactly where the players left off.

Note that starting a new game will overwrite any stored information about the previously active game.

Tips:
  - Treat the automatic **Do not rely only on the browser to hold the record the game's progress**. Browser information can easily be cleared as a result of several factors unrelated to the use of the GameTracker. For that reason, the GameTracker includes a [*Load/Save*](#loadsave-tab) capability (outlined below) that should be used to ensure that a game's progress is not lost.

### Help 

Detailed information on playing the game has been compiled, by Mathiew Martin, in two excellent source: **The Rule Compendium** and **The Companion** website.

Where possible, the GameTracker provides context sensitive links to these source. Most steps will display a Help button which allows the players to view either source's notes about that particular step.

Tips:
  - Clicking on the green *Compendium* and *Companion* buttons will switch which source is used to show the help. This selection will be remembered the next time the Help button is used.
  - The *Compendium* can be viewed in either PDF form or HTML. The HTML view will highlight the pertinent text in the display (see [*Options*](#options)).
  - Click Alt + either button will open the source in a seperate browser tab.
  - I **highly** recommend spending some some browsing through these sources. They contain a wealth of information about playing the game.

### Side Tabs
Tips:
  - Some side tabs will appear as needed as the players advance through the game sequence, and disappear when appropriate.
  - A side tab will automatically extend to show its text the first time appears while playing a game. After a few seconds, it will automatically retract.
  - Some side tabs (particularly the [*Skip* tab](#skip-tab)) will extend each time it changes, just remind the players that it is there.

#### Options tab

The Options pop up allows some customization of how the GameTracker appears and operates. The various options and their effects are covered in the [Options](#options) section below.

#### About tab

Well, if you are reading this, then you already know what that side tab is for.

#### Back tab

The *Back* side tab allows the players to go back to previous steps. Technically, using this tab is a LOTR "no-no" - but... everyone makes mistakes (especially when first learning to play).

Tips:
  - The GameTracker, by default, remembers all the steps executed in the current game (right back to the initial setup), which players were active and which were eliminated, and who was the First Player.
  - Though the players can go backwards through the game, there is no mechanism for going forward again. Once the *Back* side tab is used, any subsequent changes to the game (active/eliminated players, out-of-sequenct attacks, etc) are forgotten.

#### Load/Save

This side tab appears at the bottom of the screen. It can be used to obtain a block of text that has all the information about the current game in an encoded format. By copying this text block and saving it to disk, the players can be sure that they will not lose their game information if, for whatever reason, the browser's internal storage is cleared.

At any time, the players can paste a copy of a previously stored coded block of text, and the GameTracker will instantly display the game at the point where the code was generated.

Tips:
  - The *Load/Save* pop up will automatically display the save code for the current game and will automatically select the entire block for copying (or deleting).
  - When maunually selecting a block of text code to copy, take care to note that the entire block has been selected. Some methods of selecting blocks of text (e.g. double-clicking on the text) will, sometimes, not select the entire block. This will be the case if the block ends in one or more equals signs (=, ==). 

#### Skip tab

At various points during the progression of the game, the red *Skip* tab will appear on the left side of the screen. The wording on the tab is dependent on the situation and player, but it always has the same purpose: to allow the players to jump past a set of steps. For instance, when the players reach the start of the Combat Phase, the *Skip* tab appears and reads "No Combat?". If the conditions of the game mean that no enemies will engage the players and the players will not be attacking, then the players may click on the *Skip* tab and jump directly to the Refresh Phase.

#### Elimination

During multi-player games, the GameTracker tracks which of the players is the round's First Player. It also cycles through the players during any set of steps that are to executed by each player in sequence (e.g. the Special Action Window, Combat).

If a player is eliminated from the game (the player's heroes die, or the treat level rises to 50), the *Elimination* tab should be clicked to mark that player as no longer active. The GameTracker can then skip that player when determining the next player to perform a set of steps, and when the First Player token is to be passed.

#### Out Of Sequence Enemy Attack

If any card or card effects would cause an enemy to attack a player before, or after, the normal "Resolve Enemy Attacks" portion of the Combat Phase, then the players can click on the *Out Of Sequence Enemy Attack* tab to progress through the combat steps.

Once the combat is resolved, the GameTracker returns to the step that was interrupeted by the attack.

Tips:
  - The GameTracker does not support the interruption of one Out Of Sequence attack by another. Should such a situation arise, the players will have to handle the interrupting interruption on their own (sorry).

#### Out Of Sequence Player Attack

If any card or card effects would allow a player to attack an enemy before, or after, the normal "Player Attacks" portion of the Combat Phase, then the players can click on the *Out Of Sequence Player Attack* tab to progress through the combat steps.

Once the combat is resolved, the GameTracker returns to the step that was interrupeted by the attack.

Tips:
  - The GameTracker does not support the interruption of one Out Of Sequence attack by another. Should such a situation arise, the players will have to handle the interrupting interruption on their own (sorry).

### Options

##### Display the Compendium Rules as

This allows the players to choose whether the Help button will display the *Compendium* information as either a PDF or as HTML. The choice is completely up to the players as the information displayed is the same in either format.

Tips:
  - When HTML is chosen, the display will highlight the particular text on the page that is relevant to the step chosen.

##### Show Tooltips

Tooltips appear as white text on a black background when the mouse hovers over certain screen elements. They can be useful when first using the GameTracker, and can be turned off here when no longer needed.

##### Sequence Options

The *Alternate Setup* option changes the sequence of steps in the intial Setup Phase of a new game. The regular setup sequence tends to require many reshufflings of the players' decks as well as the encounter decks. The alternate sequence was designed to minimimize that annoyance.

The *Show End/Start of phases as steps* option will cause the a step to displayed whenever one phase is ending and a new one is starting. THis does not affect the game play in any way.

Tips:
  - Changing the option *Alternate Setup* option has no effect once a game has started. It is only applied when the New Game side tab is used.
  - Using the *Show End/Start of phases as steps* option to show the changes in phases can be handy reminder to activate/deactive abilities, remove cards that only apply to the current phase, or to perform other tasks as various scenarios require.


### Version

The GameTracker's current version number is displayed in a small grey box in the bottom left of the screen. 

Tips:
  - Please include the version number in any questions or bug reports you may send.
  - Hovering over the version number will cause the Sequence image, the Main Dialogue, and the Side tabs to disappear, allowing a clear view of the wonderful artwork that various artists have created for LOTR LCG and that I have included as backround images. 

## Version History

#### v2.0.1

- Internal:
  Bug Fix: function logleave() did not return values in the live environment.
  Removed test files from main branch.
  
### v2.0.0 Feature Complete Release

Players in multiplayer games can be named.
Tracks and displays the 1st player.
Players can be eliminated from the game.
Removed Victory Points.
Added Out Of Sequence Player Attacks.
Added Load/Save.
Eliminated need for "Combat Check" step.
Removed format updating.
- Internal:
  Improved use of {} for alternate wordings.
  Removed use of [] for alternate state text.
  Reorganized and renamed code functions.
  Isolated auto-skip of stages to new function.
  Standardized naming of sliding buttons as side tabs.
  Added support for side tabs at bottom of screen.
  Auto-advance in Options and Load/Save.
  Added suite of tests.
  Removed unneeded styling of active anchor tag.
  Initial state now includes active player info.
  Standardized variable naming for step vs stepNum.
  Auto-advance if Show Start/End phase option is deselected while on a Start/End phase step.
  Standardized tooltip text separator as tilde.
  Options are now applied to the current state's display when Options is closed.
  Minor text revisions.
  Standardized naming of elements formerly identified as GAME_HELP to HELP_AREA.
  Avoid flashing of dialogues on startup by moving the hiding of elements to earlier in the code execution.
  Eliminated unneeded postPhaseChange step type.
  Display 1st player name with round information.
  Introduced Settings to hold game specific parameters that are not part of the StateHistory.
  Extracted game specific items from Options and placed in new Settings structure.
  Automatic activation/suppression of trace messages.
  Added Settings to browser local storage.
  Options are not cleared by clicking on version.
  Compendium/Companion preference now set in methods rather than button.
  Added fast fades.
  Corrected several issues with active players by adding new, always active player 0.

### Earlier versions

-- **v1.8.4 Image Processing**

JIT Image loading
StateHistory: changed from retreival of local storage string to global array.
Change images each round.
Fixed appearance of Back button at step 0.
Delay the retraction of extended Skip nav buttons.

-- **v1.8.3**

Added out-of-sequence attack steps.
Altered positioning of tooltips.
Corrected version number.
Fixed display of step name in help dialogue.
Fixed tooltip for opening help in another tab.

-- **v1.8.2**

Added tooltips for Nav bars.
Sequence steps include tooltips for special action Nav bars.

-- **v1.8.1**

Added alternate setup sequence.
shortened tooltip fade time to 3 sec.
support more variation of step name depending on number of players.

-- **v1.8.0**

Overhaul
Features:
  - End and Start of Phases can now be optionally shown as steps.
  - Each Nav bar will appear extended the first time it is displayed in a game.
  - Added tooltip which shows cards can be played when step being displayed includes an Action Window.
  - Removed display of 'First Player:' for single-player games.
Bug Fix:
  - i13: Action Windows were not indicated during the Combat sequence.
  - i14: Combat sequence was only presented once for each player.
  - Victory Points were not displayed.
  - While altering Victory Points, the new value was not clearly shown.
  - Option for displaying tooltips was not being correctly parsed.
  - Option for compendium/companion preferrence was not being correctly parsed.
  - Option for compendium foramt was not being parsed.
Internal:
  - Added code to automatically upgrade data storage formats.
  - Added new format: options are stored separately from the state history,
                      new storage location for state history.
  - Generation and processing of Options and About Nav Bars is now consistent with other Nav bars.
  - Replaced references to "phases" element of Sequence object with new "phase" element text in Sequence.steps.
  - Removed "phases" element of Sequence object.
  - Instituted "playerloop" to allow for mulitple attacks on/by each player.
  - Implemented new "Change" phase type in Sequence.steps.
  - Implemented new "postPhaseChange" as a new "type" in Sequence.steps to complement "Change".
  - Changed Options from an integer of flags to an object.
  - New function decodeStateHash() ensures consistent creation of state objects.
  - Sequence.steps now supports different name for single-player and multi-player games.
  - Removed old comments containing trace code.
  - GetStandardBanners() now accepts a current state object and previous state name, rather than hash values.
  - Changed Option for compendium format from boolean to string.

-- **v1.7.2**

Corrected display of tooltips.
Removed display of "TrackerDisplay" as tooltip.

-- **v1.7.1**

Changed About text.
Shortened URLs of background images.
HTML conversion in progress:
  - pgs 1-120: complete

-- **v1.7.0**

Added Campaign mode.
Skip campaign-only steps in regular mode.
 - i11: Fixed bug that lost states when using 'back'.
Fixed bug that prevented display of round and points.
Changed display of final step for single-player.
Reformatted document.

-- **v1.6.0**

Added support for tooltips.
Tooltip for help buttons.
Tooltip for close button for new game.
Fixed sizing of frame used to display help.
Help display scales to fit containing frame.

-- **v1.5.1**

Additional conversion changes to the HTML Compendium.

-- **v1.5.0**

Compendium and Companion can be opened in new tabs.
-- **v1.4.1**
  
i3: Compendium PDF does not display in Chrome on certain devices
 - Switched from object to iframe for display area.
  
-- **v1.4.0**

Revised help system
 - i3: Added HTML display of the Rules Compendium.
Nav Bars
 - Tweaks to nav-bar font sizing and colours.
 - Added Options.
 - Fixed fade-in and fade-out of About.
 - Added auto-display of 'skip' nav bars.
 - i9: Fixed Back causing error in Setup Phase.
 - i10:Back functions right back to first step in Setup Phase.
Options
 - Compendium preferred over Companion.
 - Compendium as HTML or PDF.
Appearance
 - Adjust images on resize.
 - Adjust outline box on resize.
Internal
- Removed ununsed Round.png image.
- Changed references to Rules to Help for clarity.
- Standardized coding standard on CAPS for constants, CamelCase for globals.
- Change declaration of constants and globals.

-- **v1.3.1**

Fixed Help close button not working.

-- **v1.3.0**

Added ability to support option flags. 
Record Compendium vs Companion in option flags. 
Changed stylings and formatting of About display.
Internal changes to code styling (use of CAPS for constants, CamelCase for globals).

-- **v1.2.5**

Added copyrights and attributions. Added About button. Standardized SideNav naming conventions. Removed unneeded stylings and classes.

-- **v1.2.4**

Cleanup of data organization and comments. Removed obsolete CCS elements. Images change based on day rather than day of the month.

-- **v1.2.3**

Background images change daily.

-- **v1.2.2**

i6: Corrected sizing of the background images.

-- **v1.2.1**

i4: Corrected confusing colouring of "Action Window" text.

-- **v1.2.0**

Use new encoding values.
Changes to display of sequence image.
Support new levels of looping and skips,

-- **v1.1.0 **

Added scrollable background.

-- **v1.0.0**

Added player elimination.
Help button to display online Companion links.
