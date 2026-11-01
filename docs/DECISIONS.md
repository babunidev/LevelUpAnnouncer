# LevelUpAnnouncer — decisions and evidence

**By:** Babuni

| Implemented choice | Evidence | Interpretation boundary |
| --- | --- | --- |
| Fixed level-specific text | `LevelMessages[1..60]` | No generated text or model integration |
| Private preview, separate send | `PreviewLevel`, `AnnounceLevelToGuild` | Manual send can claim any in-range level |
| Increasing-level guard | event handler global | Not persistent; TOC has no SavedVariables |
| Defensive string functions | trim and parser | `string.match` remains a Lua 5.0 risk |
| Preserve historical alias strings | source banner/comment | Current documentation credits Babuni |

## Open verification

- Verify or fix `string.match` availability on the intended Lua 5.0/1.12 client in a separate code change.
- Verify callback event/argument conventions and PLAYER_LEVEL_UP timing against the actual client.
- Do not promise persistence: TOC omits SavedVariables and entering-world resets the tracker.
- Check local preview, integer versus fractional inputs, unguilded sends and misleading manual confirmation.
- Check duplicate events, reload/zone transitions, level 60 boundary and guild channel restrictions; manual sends are unthrottled.

These are source-observed choices and proposed checks, not invented historical approvals or an approved feature backlog.

## 2026-11-01 — creative purpose and possible next direction

The original creative goal was to turn level-ups into shared, roleplay-flavored guild celebrations, especially meaningful during hardcore play. That intention comes from my present recollection of why I made the addon, not from a recovered historical design transcript.

The source's 60 different messages vary **between levels**; they are not randomly selected **within a level**. My interest in random alternatives is a possible future refinement, not a feature already present or a committed implementation decision.

From memory, earlier repair attempts did not yield a reliably working addon. A newer-client port remains of interest, but neither a target client nor a development schedule has been selected. Source compatibility and actual in-game behavior remain unverified.

## Preserved earlier documentation

The following earlier record is retained verbatim. Statements about unavailable history or pending verification describe that earlier snapshot; the dated evidence above supplements it.

# BuxbrewDing — decisions and evidence

**Author:** Babuni

## Current implementation choices (not confirmed historical approvals)

The level itself shapes each prewritten message; guild announcements and local previews have separate paths.

## Unresolved

Confirm guild-message behavior and compatibility with Vanilla Lua; the source comment still contains an earlier author alias.

## 2026-11-01 — repository naming

The GitHub repository has been renamed **LevelUpAnnouncer** at my direction. The old **BuxbrewDing** names remain accurate references to the installed addon, source files and commands. At my direction, AI updated documentation only; this decision does not establish a tested runtime migration.
