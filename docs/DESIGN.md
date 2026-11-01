# LevelUpAnnouncer — experience design

**By:** Babuni

Level progression becomes a small public roleplay moment: early adventure grows into exaggerated heroic confidence at level 60. The idea came from wanting to share the excitement of every level-up with the guild, especially on hardcore servers where reaching the next level feels hard-earned. Playful roleplay announcements give that shared moment a little character. The player can inspect each line privately before deliberately sending it.

The source currently assigns one fixed line to each level. It does not implement random alternatives at the same level, although a richer pool of messages is a possible future design direction. The original addon is not confirmed to work reliably in-game.

Automatic output is event-driven with an increasing-level guard. No options panel, enable switch, localization system or pacing control is implemented. Manual preview and announcement are separate, but the misleading success message for unguilded sends should be tested and addressed in a separately authorized code change.

## Verification priorities

- Verify or fix `string.match` availability on the intended Lua 5.0/1.12 client in a separate code change.
- Verify callback event/argument conventions and PLAYER_LEVEL_UP timing against the actual client.
- Do not promise persistence: TOC omits SavedVariables and entering-world resets the tracker.
- Check local preview, integer versus fractional inputs, unguilded sends and misleading manual confirmation.
- Check duplicate events, reload/zone transitions, level 60 boundary and guild channel restrictions; manual sends are unthrottled.
