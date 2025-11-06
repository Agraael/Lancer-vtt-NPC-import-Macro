# Lancer NPC Importer for Foundry VTT

A Foundry VTT macro that allows you to import NPCs into the Lancer system from two sources:
- **JSON files** exported from Comp/Con
- **Comp/Con cloud** account (direct sync)

## Features

- **Dual Import Methods**
  - Import from local JSON files (always creates new NPCs)
  - Import directly from your Comp/Con cloud account (can update existing NPCs)

- **Smart NPC Management**
  - Update existing NPCs while preserving token images and settings
  - Batch import multiple NPCs at once
  - Search and filter NPCs by name, class, tier, or tag
  - Select/deselect all functionality

- **Comprehensive Warnings**
  - Alerts for missing NPC classes in compendiums
  - Alerts for missing NPC templates
  - Summary of missing features with counts
  - Warning for custom tier NPCs (not yet supported)

- **User-Friendly Interface**
  - Live selection counter
  - Search functionality with real-time filtering
  - Clean, intuitive dialogs

## Installation

1. Copy the contents of [`macro.js`](./macro.js) into a new macro in Foundry VTT
2. Set the macro type to "Script"
3. Save and run the macro

## Usage

### Import from JSON Files

1. Run the macro
2. Click "Import from JSON File(s)"
3. Select one or multiple `.json` files exported from Comp/Con
4. NPCs will be imported as new actors

### Import from Comp/Con Cloud

1. Make sure you're logged into Comp/Con in Foundry VTT:
   - Go to **Settings → System Settings → COMP/CON Login**
   - Enter your Comp/Con credentials

2. Run the macro
3. Click "Import from Comp/Con"
4. The macro will fetch your active NPCs from Comp/Con
5. Use the search box to filter NPCs if needed
6. Select the NPCs you want to import
7. Choose whether to update existing NPCs (recommended to keep token settings)
8. Click "Import Selected"

## Requirements

- **Foundry VTT** v10 or higher
- **Lancer System** (official Lancer game system for Foundry VTT)
- **Comp/Con Account** (for cloud import feature)

## Known Limitations

- Custom tier NPCs are not supported and will default to Tier 1
- NPCs must exist in your system's compendiums to be imported correctly
- Missing NPC classes, templates, or features will generate warnings

## Warnings and Notifications

The macro provides detailed feedback during import:

- **Custom Tier Warning**: NPCs with custom tiers will be imported as Tier 1
- **Missing Items**: Alerts when NPC classes or templates are not found in compendiums
- **Missing Features**: Summary count of features not found, with details in console
- **Import Summary**: Success and error counts after batch import

## Troubleshooting

**"Not logged into Comp/Con" error**
- Go to Settings → System Settings → COMP/CON Login and enter your credentials

**Missing classes or features**
- Make sure you have the official Lancer compendiums enabled
- Check that your compendium packs are up to date

**NPCs not updating**
- Ensure "Update existing NPCs" is checked
- Verify that the NPC has a matching Lancer ID (lid) in your world

## Credits

Created for the Lancer community on Foundry VTT.

## License

This macro is provided as-is for use with Foundry VTT and the Lancer system.
