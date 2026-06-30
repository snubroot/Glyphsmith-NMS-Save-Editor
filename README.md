# Glyphsmith

Glyphsmith is a Windows save editor for No Man's Sky players who want a safer, clearer way to inspect and tune their saves.

## Highlights

- Open live `.hg` saves and readable JSON exports
- Edit exosuit, freighter, storage, starship, exocraft, and multi-tool inventories
- Add, refill, clear, sort, resize, and unlock supported item inventories
- Export and import inventories, technology layouts, ships, multi-tools, companions, and eggs
- Copy saves between discovered No Man's Sky account folders
- Preserve save and manifest pairs during save transfer
- Detect external save changes while the game is running
- Browse and edit raw save JSON with a lazy tree and guarded formatting
- Manage portal glyphs, known products, known technology, rewards, discoveries, bases, and companions
- Use curated inventory presets for survival, base construction, farming, exploration, combat, and currency storage
- Preview starships and multi-tools while editing class, seed, stats, and identity fields
- Review backups and compare save changes
- Manage No Man's Sky mods, AMUMSS workspaces, profiles, generated outputs, and rollback-ready installs

## Download

Use the release zip in this folder:

```text
Glyphsmith-Windows.zip
```

## Install

1. Extract `Glyphsmith-Windows.zip`.
2. Open the extracted `Glyphsmith` folder.
3. Run `Glyphsmith.exe`.

No installer is required.

## Save Safety

Glyphsmith keeps save handling conservative:

- Live `.hg` saves are paired with their matching `mf_` manifest files.
- Save transfers treat a save and manifest as one occupied slot.
- Direct save writes create backup copies first.
- Imported files are validated before they replace save data.
- External save changes are detected so the editor does not quietly work on stale data.

## Common Workflows

### Inventory Editing

Use the inventory tabs to add items, refill stacks, apply presets, resize grids, unlock slots, export inventories, and import validated inventory files.

### Save Transfer

Use Save Transfer to copy a save into another discovered No Man's Sky account folder while preserving identity, platform, selected bases, discoveries, ByteBeat data, and settlement data.

### Starships And Multi-Tools

Use the Starships and Multi-Tools tabs to edit names, classes, seeds, stats, installed technology layouts, and import/export files for sharing or reuse.

### Raw JSON

Use Raw JSON for advanced save inspection. Large selections show a summary first, and formatting is explicit so huge saves stay responsive.

### Mod Manager

Use Mod Manager to inspect a No Man's Sky install, organize active and inactive mods, manage AMUMSS workspaces, create selected mod outputs, install them, and roll back the last install.

## Requirements

- Windows 10 or Windows 11
- A No Man's Sky save folder if you want live save discovery
