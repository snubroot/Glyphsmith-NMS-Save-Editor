# Glyphsmith

Glyphsmith is a Windows save editor for No Man's Sky players who want a safer, clearer way to inspect, tune, transfer, and back up their saves.

It is built for real player workflows: inventories, ships, multi-tools, companions, bases, discoveries, rewards, raw JSON, save transfer, backups, and mod management in one desktop editor.

## Download

Use the release zip in this repository:

```text
Glyphsmith-Windows.zip
```

## Install

1. Extract `Glyphsmith-Windows.zip`.
2. Open the extracted `Glyphsmith` folder.
3. Run `Glyphsmith.exe`.

No installer is required.

## Core Features

- Open live `.hg` No Man's Sky saves
- Open readable JSON save exports
- Auto-load the newest discovered local save on startup
- Save live `.hg` files with matching manifest handling
- Save readable JSON copies for inspection or sharing
- Import readable JSON back into the loaded editor session
- Detect external save changes while the game or another tool is active
- Mark edits in memory first so nothing is written until you choose Save
- Keep backup and restore workflows close to the active save

## Save Safety

Glyphsmith is conservative around live save data.

- Live saves and `mf_` manifest files are treated as a pair
- Save transfers treat either a save file or its manifest as an occupied slot
- Live save writes create backup copies before replacement
- Save and manifest replacements use same-folder temp files
- Imported inventories, tech layouts, ships, multi-tools, companions, eggs, and bases are validated before replacement
- Large raw JSON selections are guarded so the editor stays responsive
- External disk changes are detected so stale editor data is not silently saved over newer data

## Save Overview

The General tab gives quick access to high-level save fields.

- Menu save name
- Save summary
- Units
- Nanites
- Quicksilver
- Tainted Metal total
- Total play time
- Current difficulty preset
- Easiest used difficulty preset

## Inventory Editing

Glyphsmith has scoped inventory tabs for the major player storage areas.

- Exosuit general, technology, and cargo
- Freighter general, technology, and cargo
- Storage containers
- Starship general, technology, and cargo
- Exocraft general, technology, and cargo
- Multi-tool installed technology

Inventory editing includes:

- Visual slot grids with item icons
- Slot inspection with item ID, amount, max amount, position, and flags
- Item catalog search by name or ID
- Add product and substance stacks
- Refill existing stacks
- Clear supported item inventories
- Fill inventories with selected item rotations
- Resize inventories
- Unlock slots
- Expand supported inventories to 10x12
- Move stacks by drag and drop
- Duplicate stacks inside the same inventory with Ctrl-drag
- Pin slots so optimizers and auto-stack actions skip them
- Auto-stack matching items into better target inventories
- Optimize duplicate partial stacks without changing item totals
- Sort optimized stacks by material family, rarity, value, or utility
- Export and import inventory files
- Export and import technology layouts for technology inventories

## Inventory Tools

The Inventory Tools tab is for broad inventory operations across target groups.

- Max slots for selected inventory groups
- Max out exosuit technology
- Refill target stacks
- Optimize target stacks
- Apply built-in presets
- Create custom presets
- Import and export presets
- Delete custom presets
- Preview preset purpose, target hint, and item list before applying

Built-in presets include:

- Clear Inventories
- Builders Dream
- Starship AI Valves
- Oxygen + Sodium Survival
- Survival Kit
- Starship Road Kit
- Tech Crafting Kit
- Upgrade Token Vault
- Sentinel Hunter
- Money Printer
- Farm Starter
- Refiner Junk Drawer
- Ocean Kit
- Emergency Explorer

Preset fill modes include:

- Replace inventory
- Fill empty slots only
- Top off existing stacks and add missing items
- Append where possible

Technology inventories are protected from item-preset fills unless the action is a dedicated technology layout action.

## Starships

The Starship tab edits the player's ship collection and selected ship inventory.

- View and switch between owned ships
- Edit current ship selection
- Edit ship name
- Change ship type
- Change class
- Generate or enter a seed
- Edit resource path
- Toggle legacy colors
- Edit damage, shield, hyperdrive, and maneuverability stats
- Preview the selected ship identity while editing
- See key installed technology status
- Max out a ship to S-class stats and rebuilt technology
- Delete ships when the save still has another ship available
- Export ships as `.sh0`
- Import a ship over an existing slot
- Import a ship as a new owned ship
- Export and import starship technology layouts
- Export and import selected ship inventories
- Refill and optimize selected ship item inventories
- Clear, fill with Starship AI Valves, or apply Builders Dream to ship general inventory

Supported ship type choices include hauler, fighter, Golden Vector, Horizon Vector NX, Utopia Speeder, explorer, Boundary Herald, shuttle, exotic, Starborn Runner, Starborn Phoenix, living ship, The Wraith, solar, interceptor, and corvette.

## Multi-Tools

The Multi-Tool tab edits the player's multi-tool collection and installed technology.

- View and switch between active multi-tools
- Edit active multi-tool selection
- Edit multi-tool name
- Change multi-tool type
- Change class
- Generate or enter a seed
- Edit resource path
- Toggle legacy colors
- Edit damage, mining, and scanner stats
- Preview the selected multi-tool identity while editing
- See key installed technology status
- Repair installed technology layout issues
- Max out a multi-tool to S-class stats and rebuilt technology
- Export multi-tools as `.mt0`
- Import a multi-tool over an existing slot
- Import a multi-tool as a new active multi-tool
- Export and import multi-tool technology layouts
- Export and import installed technology inventory

Supported multi-tool type choices include standard, royal, sentinel, sentinel B, switch, staff, staff NPC, Atlas, and Atlas Scepter.

## Companion Studio

The Animal Companions tab edits companion slots and stored eggs.

- Switch between companions and eggs
- Edit custom companion names
- View matched discovery names when the save contains them
- Edit custom species names
- Edit age, size, trust, hunger, loneliness, and personality values
- Toggle slot unlocked, predator, fur, and egg sequencing flags
- Edit creature ID, creature type, biome, descriptors, and appearance seeds
- Edit primary, secondary, species, genus, color, and bone scale seeds
- Edit accessory preset layers for companions
- Edit egg timing and egg genetics
- Export companions as `.pet`
- Export eggs as `.egg`
- Import companions and eggs from matching files or JSON
- Clear companion or egg slots

## Base Architect

The Base Building tab is a full base inspection and editing workspace.

- List saved bases
- See owned, downloaded, and generated base details
- Filter base parts by name, ID, and category
- Inspect placed part identity, category, flags, and transform data
- Edit base metadata
- Rename bases
- Change base power mode
- Replace selected parts
- Apply material variants
- Edit exact position and orientation vectors
- Nudge parts along X, Y, and Z axes
- Rotate selected parts left or right
- Duplicate selected parts
- Delete selected parts
- Convert selected or filtered parts to another part ID
- Export a complete base as `.glyphbase.json`
- Replace an owned planetary base with an external base while keeping identity, location, and teleport registration
- Assign overseer, scientist, armourer, farmer, or technician workers to a base
- Clear terrain edits linked to a base
- Delete a base with related teleport link and terrain cleanup

Base part categories include anchors, structures, technology, freighter parts, ship parts, wiring, lighting, decorations, and other known build objects.

## Discoveries And Portal Tools

The Discoveries tab focuses on coordinates and travel address editing.

- Load the current player travel address
- Select galaxy
- Edit X, Y, Z, solar system, and planet coordinates
- Paste or click portal glyphs
- Decode portal glyph addresses
- Decode galactic coordinates
- Preview portal code, signal booster code, galactic address, universe address, center distance, and estimated jumps
- Apply a warp target to the save
- Preserve previous universe address data when applying a new address
- Move the player and ship spawn state together for the target system

## Catalog Unlocks

The Catalog tab manages save-known unlock flags.

- Unlock or lock known technology
- Unlock or lock known products
- Unlock or lock portal glyphs
- Filter by name, ID, or category
- Hide damaged items
- Hide Expedition-exclusive items
- Hide alternative building options
- Unlock or lock all visible entries
- Unlock or lock selected entries

## Rewards

The Rewards tab edits account-level reward unlocks when `accountdata.hg` is available.

- Detect account data beside the loaded save
- Choose a different account data file
- View Quicksilver rewards
- View Expedition rewards
- View Twitch rewards
- View platform rewards
- Filter reward tables by name, ID, or category
- Unlock or lock all visible rewards
- Unlock or lock selected rewards
- Save account reward changes
- Compare account unlock state with save-known product and technology state

## Save Transfer

The Save Transfer tab copies saves between discovered No Man's Sky account folders.

- Discover local account folders
- Choose source and destination accounts
- Browse to an account folder manually
- Choose source and destination save slots
- Detect occupied destination slots from save files and manifest files
- Copy live save data with the matching manifest
- Preserve destination identity fields where needed
- Transfer selected base ownership data
- Transfer ByteBeat data
- Transfer discoveries
- Transfer settlement data
- Review selectable bases before transfer
- Warn before replacing occupied save slots

## Backups

The Backups tab keeps recovery actions close to the active save.

- List backups beside the current save
- Create a backup on demand
- Restore a selected backup
- Open a backup read-only
- Compare a backup with the current save
- Save notes for backups
- Handle matching manifest backups when present

## Raw JSON

The Raw JSON tab is for advanced inspection and careful manual edits.

- Lazy tree navigation for large saves
- JSON pointer path display
- Child table editing for selected objects and arrays
- Add fields
- Add array items
- Duplicate selected JSON data
- Delete selected JSON data
- Copy JSON pointer paths
- Format selected JSON explicitly
- Show summaries for huge or root selections before formatting
- Validate edited JSON
- Apply edited JSON back to the loaded save
- Revert editor changes
- Copy and paste JSON
- Find within selected JSON text
- Add, rename, delete, and jump to bookmarks

## AI Copilot

The AI Copilot tab is an optional guided assistant for the loaded save.

- Use local Ollama
- Use Claude with an API key or `ANTHROPIC_API_KEY`
- Refresh available local models
- Test the selected provider
- Ask grounded questions about the loaded save
- Get save overview summaries
- List inventories
- Inspect a named inventory
- Find held items
- Search the bundled item catalog
- Look up item IDs, families, categories, stack behavior, and icons
- Queue confirmed editor actions through Glyphsmith's normal save flow

Supported confirmed actions include clearing item inventories, refilling stacks, applying safe item fills, applying Builders Dream or Starship AI Valves, unlocking and expanding inventories, unlocking all portal glyphs, converting all ships to a selected type, and maxing out named ships.

The player still chooses Save before anything is written to disk.

## Mod Manager

The Mod Manager tab manages No Man's Sky mod folders, profiles, AMUMSS workspaces, generated outputs, and rollback-ready installs.

- Detect common No Man's Sky install locations
- Choose an install folder manually
- Verify install readiness
- Create expected mod folders
- Remove `DISABLEMODS.TXT`
- Open active and inactive mod folders
- Move selected active mods to inactive storage
- Move selected inactive mods back to active mods
- Refresh active and inactive mod lists
- Save active mods as a named profile
- Preview and apply profiles
- Delete profiles
- Install selected generated outputs as active or inactive mods
- Sync all generated outputs to active mods
- Check selected output conflicts
- Check generated output conflicts
- Back up replaced mod targets before install
- Roll back the last install
- Reject linked output entries during install instead of following them

AMUMSS workspace support includes:

- Detect or choose an AMUMSS folder
- List scripts from `ModScript`
- Save, reload, duplicate, rename, delete, validate, build, and open selected scripts
- Run selected scripts without building every script in the folder
- Cancel a running build
- Capture build logs
- Browse generated outputs
- Open output folders and build logs
- View build history
- Load or open history logs
- Copy short error snippets
- Generate starter AMUMSS scripts
- Search item references from Glyphsmith's bundled catalog
- Insert or copy item IDs for mod work

Starter generator flows include:

- Empty AMUMSS mod
- Product or recipe tweak
- Inventory stack tweak
- Reward or table edit
- Simple value replacement

## Supported Import And Export Files

- `.hg` live save files
- `.json` readable save exports
- `.gsi0` inventory exports
- `.gspreset` inventory presets
- `.stl0` starship technology layouts
- `.gtl0` general technology layouts
- `.sh0` starship exports
- `.mt0` multi-tool exports
- `.pet` companion exports
- `.egg` egg exports
- `.glyphbase.json` base exports

## Requirements

- Windows 10 or Windows 11
- A local No Man's Sky save folder for live save discovery
- Optional: AMUMSS for mod build workflows
- Optional: Ollama or an Anthropic API key for AI Copilot provider features

## Notes

No Man's Sky is developed by Hello Games. Glyphsmith is an independent editor for personal save management.
