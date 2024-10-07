# GameTracker Testing Suite

## Setup

- ensure version number ends with 'x' (enables logging)
- open page
- view local storage `DevTools->Application->Storage->Local storage/file://`

## Suite A

- click on version:
  - [ ] local storage of `LOTR_States` is deleted
  - [ ] local storage of `LOTR_Settings.altSetup` = `false`
  - [ ] local storage of `LOTR_Settings.campaign` = `false`
  - [ ] local storage of `LOTR_Settings.names` = `[]`
  - [ ] local storage of `LOTR_Settings.preferCompendium` = `true`
  - [ ] local storage of `LOTR_Settings.previouslyExtended` = `["New Game", "Options", "About", "Load/Save"]`
- manually delete local storage of `LOTR_Options` if present
- refresh browser:
  - [ ] side tabs **New Game**, **Options**, **About**, **Load/Save** appear, extend and retract.
  - [ ] background pics are displayed.
  - [ ] sequence image is displayed.
  - [ ] version is displayed.
- scroll down:
  - [ ] background pics are loaded and displayed as needed.
- hover over side tabs:
  - [ ] side tabs extend.
  - [ ] tooltips are displayed.
  - end hover:
    - [ ] side tabs retract.
- hover over version:
  - [ ] sequence image is removed.
  - end hover:
    - [ ] displays sequence image.
- **About**:
  - [ ] *About* text is displayed.
  - [ ] *About* text shows proper version in Header, TOC and Version History
  - click on background:
    - [ ] removes *About* text.
- **Options**:
  - [ ] selected - *HTML*, *Show general tooltips*, *Show tooltips on tabs*, *Show End/Start of phases*
  - [ ] not selected - *PDF*, *Alternate Setup*, *Save extended history*.
  - select *PDF*, deselect *Show tooltips on tabs*
  - click on background:
    - [ ] removes **Options**.
  - hover over side tabs:
    - [ ] side tabs extend.
    - [ ] tooltips are not displayed.
- **Load/Save**:
  - [ ] displays **Load/Save**.
  - [ ] save code displayed and selected.
  - copy save code and save as 'Suite A'.

## Suite B

***(requires save code from Suite A)***

- click on **version** to clear local storage of `LOTR_Settings` and `LOTR_States`
- **Options**:
  - select *HTML*, *Show general tooltips*, *Show tooltips on tabs*, *Alternate Setup*, *Show End/Start of phases*
  - deselect *Save extended history*
- **Load/Save**:
  - [ ] closes **Options**
  - copy save code from Suite A into text area
  - click on background:
    - [ ] removes Load/Save.
  - **Options**:
    - [ ] selected - *HTML*, *Show general tooltips*, *Show tooltips on tabs*, *Alternate Setup*, *Show End/Start of phases*
    - [ ] delesected - *PDF*, *Save extended history*
    - select PDF, deselect *Show tootips on tabs*, *Alternate Setup*
- **New Game**:
  - [ ] closes **Options**
  - [ ] asks `Regular or Campaign`
  - hover over `x` (close):
    - [ ] shows tooltip
  - close (`x`):
    - [ ] returns to default page
- **New Game**, `Regular`:
  - [ ] displays options for number of players
  - select `1`, `Done`
    - [ ] displays phase `Setup Phase`
    - [ ] displays step `Shuffle Player Deck` (note singular `Deck`)
- `Help`:
  - [ ] displays Compendium as PDF at `Shuffle Decks`.
  - hover over `Compendium` and `Companion` buttons:
    - [ ] tooltip is displayed.
  - `Companion`:
    - [ ] displays Companion at `Shuffle Decks`.
  - `Alt`+`Compendium`:
    - [ ] opens Compendium PDF in a new tab at `Shuffle Decks`.
  - close tab, `Alt`+`Companion`:
    - [ ] opens Companion in a new tab at `Shuffle Decks`.
  - close tab, close `Help`
- `Help`:
  - [ ] opens Companion.
  - close `Help`
- **Next**:
  - [ ] side tab **Back** appears, extends, and retracts.
  - [ ] displays step `Shuffle Encounter Deck`.
  - **Back**:
    - [ ] **Back** disappears
    - [ ] displays step `Shuffle Player Deck`.
  - **Next**:
    - [ ] **Back** appears without extending.
    - [ ] displays step `Shuffle Encounter Deck`.
- **Next**, **Next**:
  - [ ] displays step `Set Threat Level` (note singular `Level`).
- **Next**, **Next**:
  - [ ] displays step `Draw Starting Hand` (note singular `Hand`).
- **Next**, **Next**, **Next**:
  - [ ] side tabs **Out of Sequence Enemy**, **Out of Sequence Player Attacks** appear, extend and retract.
  - [ ] displays round as `Round 1`.
  - [ ] displays step as `Start of the Resource Phase`.
  - [ ] phase is not displayed.
  - [ ] `Help` button is not displayed.
  - [ ] outline appears around 1.1.
- **Next**:
  - [ ] displays phase as `Resource Phase`.
  - [ ] outline appears around 1.2.
  - `Help`:
    - [ ] displays Companion at `Resource Phase`.
    - `Compendium`:
      - [ ] displays Compendium as PDF at `Phase 1: Resource`.
    - close `Help`
  - **Options**:
    - select *HTML*, deselect *Show general tooltips*
    - close **Options** (click on background)
  - `Help`:
    - [ ] displays Compendium as HTML at `Phase 1: Resource`.
    - [ ] 1st paragraph is highlighted.
    - hover over `Compendium` and `Companion` buttons:
      - [ ] no tooltips are displayed.
    - close `Help`
- **Load/Save**:
  - copy save code and save as 'Suite B'.

## Suite C

***(requires save code from Suite B)***

- click on **version** to clear local storage of `LOTR_Settings` and `LOTR_States`
- **Options**:
  - select *HTML*, *Show End/Start of phases*. deselect all others
- **Load/Save**:
  - copy save code from Suite B into text area
  - click on background:
    - [ ] removes **Load/Save**.
    - [ ] displays step `Gain Resources`.
- **Next**:
  - [ ] displays step `Draw Card & Action Window` (note singular `Card`).
  - [ ] 'Action Window' is highlighted.
- `Help`:
  - [ ] displays Compendium as HTML at `Phase 1: Resource`.
  - [ ] 2nd and 3rd paragraphs are highlighted.
  - [ ] displays `Action Window` button.
  - `Action Window`:
    - [ ] displays Compendium at `Resource Phase - Action Window`
    - [ ] Action Window text is highlighted.
    - `Alt`+`Action Window`:
      - [ ] displays Compendium in new tab at `Resource Phase - Action Window`
      - [ ] 'Action Window' text is highlighted.
      - close tab
    - close `Help`
- **Next**:
  - [ ] displays step `End of the Resource Phase / Start of the Planning Phase`.
- **Back**,**Options**:
  - deselect *Show End/Start of phases*:
  - close **Options**:
    - [ ] displays round as `Round 1`.
  - **Next**:
    - [ ] displays round as `Round 1 / End of the Resource Phase / Start of the Planning Phase`.
    - [ ] displays phase as `Planning Phase`.
    - [ ] displays step `Special Action Window` in highlighted colour.
    - [ ] outline around 2.1 to 2.3.
- **Next**:
  - [ ] displays round as `Round 1 / End of the Planning Phase / Start of the Quest Phase`.
  - [ ] displays step `Quest Action Window`.
- **Next**, **Next**, **Next**:
  - [ ] displays step `Staging Action Window`.
- **Next**, **Next**:
  - [ ] displays step `Travel Opportunity...`.
- **Next**, **Next**, **Next**:
  - [ ] displays step `Deal Shadow Cards...`.
  - [ ] ***Skip*** tab appears, extends and retracts.
  - [ ] ***Skip*** tab text is `No Combat?`
- **Load/Save**:
  - copy save code and save as 'Suite C'.

## Suite D

***(requires save code from Suite C)***

- click on **version** to clear local storage of `LOTR_Settings` and `LOTR_States`
- **Options**:
  - select *HTML*, *Save extended history*, deselect all others
- **Load/Save**:
  - copy save code from Suite C into text area
  - click on background:
    - [ ] removes **Load/Save**.
    - [ ] ***Skip*** tab extends and retracts.
    - [ ] ***Skip*** tab text is `No Combat?`
    - [ ] displays step `Deal Shaow Cards...`.
- **Next**:
  - [ ] ***Skip*** tab extends and retracts.
  - [ ] displays step `Choose Attacking Enemy...`.
  - [ ] ***Skip*** tab text is `The player is not being attacked by an Enemy?`
- **Next**, **Next**, **Next**:
  - [ ] displays step `Determine Combat Damage to Defender`.
- **Next**:
  - [ ] displays step `Choose Attacking Enemy....`.
  - [ ] ***Skip*** tab text is `The player is not being attacked by another Enemy?` (note `another` instead of `an`)
- ***Skip***:
  - [ ] displays step `Choose Enemy to Attack...`.
  - [ ] ***Skip*** tab text is `The player is not attacking an Enemy?`
- **Next**, **Next**:
  - [ ] displays step `Determine Combat Damage to Enemy...`.
- **Next**:
  - [ ] displays step `Choose Enemy to Attack...`.
  - [ ] ***Skip*** tab text is `The player is not attacking another Enemy?` (note `another` instead of `an`)
- ***Skip***:
  - [ ] displays step `Discard All Shadow Cards`.
- **Next**, **Next**, **Next**:
  - [ ] displays step `End of Round Action Window`.
- **Next**:
  - [ ] displays round as `Round 2 / End of the Refresh Phase / Start of the Resource Phase`.
  - [ ] displays step `Gain Resources`.
  - [ ] background images change.
- **Load/Save**:
  - copy save code and save as 'Suite D'.

## Suite E

- click on **version** to clear local storage of `LOTR_Settings` and `LOTR_States`
- refresh browser:
  - [ ] side tabs **New Game**, **Options**, **About**, **Load/Save** appear, extend and retract.
  - [ ] background pics are displayed.
  - [ ] sequence image is displayed.
  - [ ] version is displayed.
- **Options**:
  - select *HTML*, *Alternate Setup*
  - deselect all others
- **New Game**, `Regular`, `3`:
  - [ ] no close button
  - `Player 2`: 'Charlie'
  - `Player 3`: 'Archie'
  - swap `2` & `3`:
    - [ ] player 1 is 'Player 1'
    - [ ] player 2 is 'Archie'
    - [ ] player 3 is 'Charlie'
  - swap `1` & `2`:
    - [ ] player 1 is 'Archie'
    - [ ] player 2 is 'Player 2' (note not '2' not '1')
    - [ ] player 3 is 'Charlie'
  - `Player 2`: 'Betty'
  - `Done`:
    - [ ] displays phase `Setup Phase`
    - [ ] displays step `Place Heroes and Player Decks` (note plural `Decks`)
- **Load/Save**:
  - copy save code and save as 'Suite E'.

## Suite F

***(requires save code from Suite E)***

- click on **version** to clear local storage of `LOTR_Settings` and `LOTR_States`
- **Options**:
  - select *HTML*, *Alternate Setup*
  - deselect all others
- **Load/Save**:
  - copy save code from Suite E into text area
  - click on background:
    - [ ] removes **Load/Save**.
    - [ ] displays step `Place Heroes and Player Decks`.
- **Next**, **Next**, **Next**:
  - [ ] displays step `Set Theat Levels` (note pluralized `Levels`)
- **Next**, **Next**:
  - [ ] displays step `Determine First Player`
  - [ ] buttons displayed for 'Archie', 'Betty', 'Charlie'
  - `Betty`:
    - [ ] displays step `Perform Scenario Setup`
- **Next**, **Next**, **Next**:
  - [ ] displays step `Draw Starting Hands` (note pluralized `Hands`).
- **Next**:
  - [ ] side tabs **Elimination**, **Out of Sequence Enemy Attack**, **Out of Sequence Player Attack** appear, extend and retract.
  - [ ] displays round as `1 (Betty is 1st player)...`.
  - [ ] displays phase as `Resource Phase`.
  - [ ] displays step `Gain Resources`.
  - [ ] `Help` button is displayed.
  - [ ] outline appears around 1.2.
- **Next**, **Next**:
  - [ ] display step `Betty: Special Action Window`.
- **Next**:
  - [ ] display step `Charlie: Special Action Window`.
- **Next**:
  - [ ] display step `Archie: Special Action Window`.
- **Next**, **Next**, **Next**:
  - [ ] displays step `Betty: Staging`.
- **Next**, **Next**, **Next**:
  - [ ] displays step `Staging Action Window`.
- **Next**, **Next**:
  - [ ] displays step `Travel Opportunity...`.
- **Next**, **Next**, **Next**:
  - [ ] ***Skip*** tab appears, extends and retracts.
  - [ ] ***Skip*** tab text is `No Combat?`
  - [ ] displays step `Betty: Deal Shadow Cards...`.
- **Load/Save**:
  - copy save code and save as 'Suite F'.

## Suite G

***(requires save code from Suite C)***

- click on **version** to clear local storage of `LOTR_Settings` and `LOTR_States`
- **Options**:
  - select *HTML*, deselect all others
- **Load/Save**:
  - copy save code from Suite C into text area
  - click on background:
    - [ ] ***Skip*** tab appears, extends and retracts.
    - [ ] ***Skip*** tab text is `No Combat?`
    - [ ] displays step `Deal Shadow Cards...`.
- ***Skip***:
  - [ ] displays step `Ready All Cards`.
- **Next**:
  - [ ] displays step `Raise Threat Level` (note singular `Level`)
- **Next**:
  - [ ] displays step `End of Round Action Window`.
- **Next**:
  - [ ] displays round as `Round 2`.
  - [ ] display step `Gain Resources`.

## Suite H

***(requires save code from Suite F)***

- click on **version** to clear local storage of `LOTR_Settings` and `LOTR_States`
- **Options**:
  - select *HTML*, *Alternate Setup*
  - deselect all others
- **Load/Save**:
  - copy save code from Suite F into text area
  - click on background:
    - [ ] ***Skip*** tab appears, extends and retracts.
    - [ ] ***Skip*** tab text is `No Combat?`
    - [ ] displays step `Betty Deal Shadow Cards...`.
- **Next**:
  - [ ] ***Skip*** tab disappears.
  - [ ] displays step `Charlie Deal Shadow Cards...`.
- **Next**:
  - [ ] displays step `Archie Deal Shadow Cards...`.
- **Next**:
  - [ ] ***Skip*** tab appears, extends and retracts.
  - [ ] ***Skip*** tab text is `Betty is not being attacked by an Enemy`.
  - [ ] displays step `Betty Choose Attacking Enemy...`.
- **Next**, **Next**:
  - [ ] displays step `Betty Reveal and Resolve...`
- **Next**, **Next**:
  - [ ] ***Skip*** tab appears, extends and retracts.
  - [ ] ***Skip*** tab text is `Betty is not being attacked by another Enemy` (note `another`).
  - [ ] displays step `Betty Choose Attacking Enemy...`.
- ***Skip***:
  - [ ] displays step `Charlie Choose Attacking Enemy...`.
- ***Skip***, ***Skip***:
  - [ ] ***Skip*** tab appears, extends and retracts.
  - [ ] ***Skip*** tab text is `Betty is not attacking an Enemy`.
  - [ ] displays step `Betty Choose Enemy to Attack...`.
- ***Skip***, ***Skip**, ***Skip***:
  - [ ] displays step `Discard All Shadow Cards`.
- **Next**, **Next**:
  - [ ] displays step `Raise Threat Levels` (note pluralized `Levels`).
- **Next**:
  - [ ] displays step `Pass First Player Token to Charlie...`.
- **Next**:
  - [ ] displays round as `Round 2 (Charlie is 1st player)`.
  - [ ] displays step `Gain Resources`.
- **Load/Save**:
  - copy save code and save as 'Suite H'.

## Suite I

***(requires save code from Suite F)***

- click on **version** to clear local storage of `LOTR_Settings` and `LOTR_States`
- **Options**:
  - select *HTML*, *Alternate Setup*
  - deselect all others
- **Load/Save**:
  - copy save code from Suite F into text area
  - click on background:
    - [ ] ***Skip*** tab appears, extends and retracts.
    - [ ] ***Skip*** tab text is `No Combat?`.
    - [ ] displays step `Betty Deal Shadow Cards...`.
- **Out of Sequence Enemy Attack**:
  - [ ] displays phase as `Special Phase Out of Sequence Combat Stage`.
  - [ ] displays step `Deal Shadow Card`.
  - [ ] tabs **Out of Sequence Enemy Attack**, **Out of Sequence Player Attack** disappear.
- **Next**, **Next**:
  - [ ] displays step `Reveal and Resolve Shadow Effects...`
- **Next**, **Next**:
  - [ ] returns to step `Betty Deal Shadow Cards...`.
- **Out of Sequence Player Attack**:
  - [ ] displays phase as `Special Phase Out of Sequence Combat Stage`.
  - [ ] displays step `Declare Attacked Enemy and Attackers...`.
  - [ ] tabs **Out of Sequence Enemy Attack**, **Out of Sequence Player Attack** disappear.
- **Next**, **Next**, **Next**:
  - [ ] returns to step `Betty Deal Shadow Cards...`.

## Suite J

***(requires save code from Suite F)***

- click on **version** to clear local storage of `LOTR_Settings` and `LOTR_States`
- **Options**:
  - select *HTML*, *Alternate Setup*
  - deselect all others
- **Load/Save**:
  - copy save code from Suite F into text area
  - click on background:
    - [ ] ***Skip*** tab appears, extends and retracts.
    - [ ] ***Skip*** tab text is `No Combat?`.
    - [ ] displays round as `Round 1 (Betty is 1st player)`
    - [ ] displays step `Betty Deal Shadow Cards...`.
- **Elimination**:
  - [ ] shows option for each player ('Archie', 'Betty', 'Charlie'), plus `Cancel`.
  - **Cancel**:
    - [ ] displays step `Betty Deal Shadow Cards...`.
  - **Next**:
    - [ ] displays step `Charlie Deal Shadow Cards...`.
  - **Next**:
    - [ ] displays step `Archie Deal Shadow Cards...`.
  - **Next**:
    - [ ] displays round as `Round 1 (Betty is 1st player)`
    - [ ] displays step `Betty Choose Attacking Enemy...`.
- **Elimination**:
  - [ ] shows option for each player ('Archie', 'Betty', 'Charlie'), plus `Cancel`
  - select `Betty`:
    - [ ] displays round as `Round 1 (Charlie is 1st player)`
    - [ ] displays step `Charlie Choose Attacking Enemy...`.
  - ***Skip***:
    - [ ] displays step `Archie Choose Attacking Enemy...`.
  - ***Skip***:
    - [ ] displays step `Charlie Choose Enemy...`.
- **Elimination**:
  - [ ] shows option for remaining players ('Charlie', 'Archie'), plus `Cancel`.
  - select `Archie`:
    - [ ] displays step `Charlie Choose Enemy...`.
    - [ ] displays round as `Round 1` (note no display of 1st player).
    - [ ] **Elimination** tab disappears
- ***Skip***, **Next**, **Next**:
  - [ ] displays step `Raise Threat Level` (note singular `Level`).
- **New Game**, `Regular`, `4`:
  - [ ] displays player names `Archie`, `Betty`, `Charlie`, `Player 4`

## Suite K

***(requires save code from Suite D)***

- click on **version** to clear local storage of `LOTR_Settings` and `LOTR_States`
- **Options**:
  - select *HTML*, deselect all others
- **Load/Save**:
  - copy save code from Suite D into text area
  - click on background:
    - [ ] displays round as `Round 2`.
    - [ ] displays step `Gain Resources`.
