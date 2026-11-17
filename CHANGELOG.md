# Changelog

## v1.0.0

### Data safety
- Question-level data (topic, topic definition, mistake reason, personal note, review status) is now stored per question and survives reloads.
- Automatic safety snapshot before migration, restore, deleting an exam, or resetting.
- Restoring a JSON backup now merges by default and never overwrites without confirmation.
- Safe migration of data saved by earlier versions (nothing is removed; unknown fields are kept).
- Autosaved draft for an unfinished exam, plus a visible save status.

### New
- Per-question details dialog (topic with suggestions, definition, reason, note, flag, reviewed).
- Rebuilt mistake notebook: filters, search, grouping by exam / subject / topic / reason, pagination.
- Independent analytical report per exam with a study plan; PDF and Markdown export.
- Custom mistake-reason categories.
- Offline answer-sheet scanner (120 questions, 4 options) that fills an exam automatically.
- Version shown in Settings and written into exported backups.

### Performance
- Removed an infinite CSS animation and a blurred sticky header that forced constant repaints.
- Chart.js and fonts load without blocking first paint.
- Cached exam calculations; debounced saving while typing.

### Release
- Service-worker cache bumped to `karnameh-pro-v1.0.0` so installed apps update.
