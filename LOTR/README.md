# GameTracker
This website is an SPA intended to provide a non-commercial aid while playing the [Lord of the Rings LCG](https://www.fantasyflightgames.com/en/products/the-lord-of-the-rings-the-card-game/) from [Final Flight Game](https://www.fantasyflightgames.com/en/index/).

## Version History
#### v1.8.3
Added out-of-sequence attack steps.
Altered positioning of tooltips.
Corrected version number.
Fixed display of step name in help dialogue.
Fixed tooltip for opening help in another tab.
#### v1.8.2
Added tooltips for Nav bars.
Sequence steps include tooltips for special action Nav bars.
#### v1.8.1
Added alternate setup sequence.
shortened tooltip fade time to 3 sec.
support more variation of step name depending on number of players.
### v1.8.0
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
#### v1.7.2
Corrected display of tooltips.
Removed display of "TrackerDisplay" as tooltip.
#### v1.7.1
Changed About text.
Shortened URLs of background images.
HTML conversion in progress:
  - pgs 1-120: complete
### v1.7.0
Added Campaign mode.
Skip campaign-only steps in regular mode.
 - i11: Fixed bug that lost states when using 'back'.
Fixed bug that prevented display of round and points.
Changed display of final step for single-player.
Reformatted document.
### v1.6.0
Added support for tooltips.
Tooltip for help buttons.
Tooltip for close button for new game.
Fixed sizing of frame used to display help.
Help display scales to fit containing frame.
#### v1.5.1
Additional conversion changes to the HTML Compendium.
### v1.5.0
Compendium and Companion can be opened in new tabs.
#### v1.4.1
i3: Compendium PDF does not display in Chrome on certain devices
 - Switched from object to iframe for display area.
### v1.4.0
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
#### v1.3.1
Fixed Help close button not working.
### v1.3.0
Added ability to support option flags. 
Record Compendium vs Companion in option flags. 
Changed stylings and formatting of About display.
Internal changes to code styling (use of CAPS for constants, CamelCase for globals).
#### v1.2.5
Added copyrights and attributions. Added About button. Standardized SideNav naming conventions. Removed unneeded stylings and classes.
#### v1.2.4
Cleanup of data organization and comments. Removed obsolete CCS elements. Images change based on day rather than day of the month.
#### v1.2.3
Background images change daily.
#### v1.2.2
i6: Corrected sizing of the background images.
#### v1.2.1
i4: Corrected confusing colouring of "Action Window" text.
### v1.2.0
Use new encoding values.
Changes to display of sequence image.
Support new levels of looping and skips,
### v1.1.0 
Added scrollable background.
### v1.0.0
Added player elimination.
Help button to display online Companion links.
