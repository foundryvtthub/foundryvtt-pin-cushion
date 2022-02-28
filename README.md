# Pin Cushion

![GitHub issues](https://img.shields.io/github/issues-raw/death-save/pin-cushion?style=for-the-badge) 

![Latest Release Download Count](https://img.shields.io/github/downloads/death-save/pin-cushion/latest/module.zip?color=2b82fc&label=DOWNLOADS&style=for-the-badge) 

[![Forge Installs](https://img.shields.io/badge/dynamic/json?label=Forge%20Installs&query=package.installs&suffix=%25&url=https%3A%2F%2Fforge-vtt.com%2Fapi%2Fbazaar%2Fpackage%2Fpin-cushion&colorB=006400&style=for-the-badge)](https://forge-vtt.com/bazaar#package=pin-cushion) 

![Foundry Core Compatible Version](https://img.shields.io/badge/dynamic/json.svg?url=https%3A%2F%2Fraw.githubusercontent.com%2Fdeath-save%2Fpin-cushion%2Fmaster%2Fmodule.json&label=Foundry%20Version&query=$.compatibleCoreVersion&colorB=orange&style=for-the-badge)

![Latest Version](https://img.shields.io/badge/dynamic/json.svg?url=https%3A%2F%2Fraw.githubusercontent.com%2Fdeath-save%2Fpin-cushion%2Fmaster%2Fmodule.json&label=Latest%20Release&prefix=v&query=$.version&colorB=red&style=for-the-badge)

[![Foundry Hub Endorsements](https://img.shields.io/endpoint?logoColor=white&url=https%3A%2F%2Fwww.foundryvtt-hub.com%2Fwp-json%2Fhubapi%2Fv1%2Fpackage%2Fpin-cushion%2Fshield%2Fendorsements&style=for-the-badge)](https://www.foundryvtt-hub.com/package/pin-cushion/)

![GitHub all releases](https://img.shields.io/github/downloads/death-save/pin-cushion/total?style=for-the-badge)

## Installation

It's always easiest to install modules from the in game add-on browser.

To install this module manually:
1.  Inside the Foundry "Configuration and Setup" screen, click "Add-on Modules"
2.  Click "Install Module"
3.  In the "Manifest URL" field, paste the following url:
`https://raw.githubusercontent.com/death-save/pin-cushion/master/module.json`
4.  Click 'Install' and wait for installation to complete
5.  Don't forget to enable the module in game using the "Manage Module" button

## Installation (developement branch for foundryvtt 9)

It's always easiest to install modules from the in game add-on browser.

To install this module manually:
1.  Inside the Foundry "Configuration and Setup" screen, click "Add-on Modules"
2.  Click "Install Module"
3.  In the "Manifest URL" field, paste the following url:
`https://raw.githubusercontent.com/p4535992/pin-cushion/master/module-dev.json`
4.  Click 'Install' and wait for installation to complete
5.  Don't forget to enable the module in game using the "Manage Module" button

## Settings

- **Show Journal Preview**: Shows a Journal preview when hovering over a map pin

- **Journal Preview Type**: The type of Journal preview to show (HTML or Text snippet)

- **Preview Maximum Length**: **TEXT PREVIEW ONLY** How many characters should the text preview show?

- **Preview Delay**: How long before preview appears (in milliseconds)

- **Default Journal Entry Permission**: The default permission journal entries will be created with

- **Default Journal Entry Folder**: The default folder journal entries will be created in when creating Map Pins with a double-click

- **Enable feature Backgroundless Pins**: Removes the background box from map notes.

- **Show by default the icon image of the journal on the map note.**: If a image is setted on the journal by default is the first image setted from Pin Cushion

- **Enable Player-Only Icons by default**: Newly created notes will have player-only icons enabled automatically.

- **Default Note Icon for Players**: The default icon used for player-only icons

- **Enable Point of Interest Teleporter**: Embedded integration of the seem abbandoned 'Point of Interest Teleporter' module

- **GM Label**: Add the ability for Note tooltips to be configured so that GMs see different text to Players. So secret information can be displayed to GMs whilst players see the 'public' information about the Note.

- **Add an option to have a 'revealed' state on scene Notes.**: When enabled, then the 'revealed' state will be used to determine if the Note is visible to players. (The default Foundry VTT behaviour is for Notes to be visible to players only if the linked document is accessible by the player.)

- **Add an option to have a 'revealed' state on scene Notes.**: is an option to set the tint colour of the Note icon to indicate if the linked document is reachable or not (if the Note has no linked document, then it will always be displayed in the 'unreachable' tint).

- **Note Tint Colour when linked**: For players, the RGB value to be used to tint scene Notes if they have a reachable link (if left blank then the tint, if any, will remain unchanged).  For GMs, this is the initial Icon Tint set during import

- **Note Tint Colour when not linked**: For players, the RGB value to be used to tint scene Notes if they do not have a reachable link (if left blank then the tint, if any, will remain unchanged).  For GMs, this is the initial Icon Tint set during import

- **Select Specific Folder**: Make sense only with the module setting 'Default Journal Entry Folder' set with value 'Specific folder'

## Features

This module add many new settings for many use case on the Note config dialog, here some of the most interesting, but there is more

![create-pin](./img/create_pin.png)
![note-config](./img/note-config.png)
![journal-preview](./img/journal-preview.png)

- Changes the dropdown of map pin icons into a filepicker so users can select any icons they like
- Adds the ability to double-click the canvas while on the Notes Layer and create a map pin (and corresponding Journal Entry)
- Adds a preview of the associated Journal Entry when you hover over a map pin
- Removes the background box from map notes

![img](./img/backgroundless-pins-preview.gif)

- Add the possibility to add a thubnail preview of the journal

![img](./img/journal-thumbnail.png)

- **Add an option to have a 'revealed' state on scene Notes:** When enabled, then the 'revealed' state will be used to determine if the Note is visible to players.
(The default Foundry VTT behaviour is for Notes to be visible to players only if the linked document is accessible by the player.)

- **Add an option to set the tint colour of the Note:** Icon to indicate if the linked document is reachable or not (if the Note has no linked document, then it will always be displayed in the "unreachable" tint).

- **Add an option to hide the label:** When you hover on the note, it useful for avoid the "double" test given from the 'label' and 'title' attributes.

### libWrapper

This module uses the [libWrapper](https://github.com/ruipin/fvtt-lib-wrapper) library for wrapping core methods. It is a hard dependency and it is recommended for the best experience and compatibility with other modules.

# Build

## Install all packages

```bash
npm install
```
## npm build scripts

### build

will build the code and copy all necessary assets into the dist folder and make a symlink to install the result into your foundry data; create a
`foundryconfig.json` file with your Foundry Data path.

```json
{
  "dataPath": "~/.local/share/FoundryVTT/"
}
```

`build` will build and set up a symlink between `dist` and your `dataPath`.

```bash
npm run-script build
```

### NOTE:

You don't need to build the `foundryconfig.json` file you can just copy the content of the `dist` folder on the module folder under `modules` of Foundry

### build:watch

`build:watch` will build and watch for changes, rebuilding automatically.

```bash
npm run-script build:watch
```

### clean

`clean` will remove all contents in the dist folder (but keeps the link from build:install).

```bash
npm run-script clean
```
### lint and lintfix

`lint` launch the eslint process based on the configuration [here](./.eslintrc)

```bash
npm run-script lint
```

`lintfix` launch the eslint process with the fix argument

```bash
npm run-script lintfix
```

### prettier-format

`prettier-format` launch the prettier plugin based on the configuration [here](./.prettierrc)

```bash
npm run-script prettier-format
```

### package

`package` generates a zip file containing the contents of the dist folder generated previously with the `build` command. Useful for those who want to manually load the module or want to create their own release

```bash
npm run-script package
```

## [Changelog](./changelog.md)

## Issues

Any issues, bugs, or feature requests are always welcome to be reported directly to the [Issue Tracker](https://github.com/death-save/pin-cushion/issues ), or using the [Bug Reporter Module](https://foundryvtt.com/packages/bug-reporter/).

## License

- [FVTT-Backgroundless-Pins](https://github.com/schultzcole/FVTT-Backgroundless-Pins) ([GPLv3 License](https://github.com/schultzcole/FVTT-Backgroundless-Pins/blob/master/LICENSE))
- [foundryvtt-journal-thumbnail](https://github.com/J-Guenther/foundryvtt-journal-thumbnail) ([MIT](https://github.com/J-Guenther/foundryvtt-journal-thumbnail/blob/main/LICENSE))
- [Point of Interest Teleporter](https://github.com/zeel01/poi-teleport) ([MIT](https://github.com/zeel01/poi-teleport/blob/master/LICENSE))
- [vtt-gmtext-in-notes](https://github.com/farling42/fvtt-gmtext-in-notes) ([MIT](https://github.com/farling42/fvtt-gmtext-in-notes/blob/master/LICENSE))
- [fvtt-revealed-notes-manager](https://github.com/farling42/fvtt-revealed-notes-manager) ([MIT](https://github.com/farling42/fvtt-gmtext-in-notes/blob/master/LICENSE))
- [journal-sidebar-images](https://github.com/jessev14/journal-sidebar-images) ([MIT](https://github.com/jessev14/journal-sidebar-images/blob/master/LICENSE))

This package is under an [GPLv3 License](LICENSE) and the [Foundry Virtual Tabletop Limited License Agreement for module development](https://foundryvtt.com/article/license/).

## Acknowledgements

- Thank you to [schultzcole](https://github.com/schultzcole) for the module [FVTT-Backgroundless-Pins](https://github.com/schultzcole/FVTT-Backgroundless-Pins) inspiration
- Thank you to [J-Guenther](https://github.com/J-Guenther) for the module [foundryvtt-journal-thumbnail](https://github.com/J-Guenther/foundryvtt-journal-thumbnail) inspiration
- Thank you to [zeel](https://github.com/zeel01) for the module [Point of Interest Teleporter](https://github.com/zeel01/poi-teleport)
- Thank you to [farling42](https://github.com/farling42) and the module [vtt-gmtext-in-notes](https://github.com/farling42/fvtt-gmtext-in-notes)
- Thank you to [farling42](https://github.com/farling42) and the module [fvtt-revealed-notes-manager](https://github.com/farling42/fvtt-revealed-notes-manager)
- Thank you to [jessev14]((https://github.com/jessev14) and the module [journal-sidebar-images](https://github.com/jessev14/journal-sidebar-images)
