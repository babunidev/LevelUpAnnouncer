# LevelUpAnnouncer — concept

**By Babuni** · Originally **BuxbrewDing** · World of Warcraft 1.12

## Why it exists

On hardcore servers, reaching another level can feel like a small victory over the odds. Every milestone is worth sharing, and I wanted guildmates to celebrate those moments instead of silently watching the experience bar fill.

LevelUpAnnouncer grew from that idea: make level-ups into little roleplay events. A character's progress should have a voice, with playful announcements that change as the adventure unfolds rather than a generic message repeated at every milestone. Whether or not another addon already offered something similar was never the reason to make this one; the pleasure was in giving the celebration my own roleplay flavor.

## What the original addon contains

The original `BuxbrewDing` source defines 60 prewritten English messages, **one specific message for each level from 1 to 60**. It attempts to announce the corresponding message automatically in guild chat and offers private previews and manual announcements.

The current implementation does **not** randomly choose among several messages for the same level. Randomized alternatives are an idea worth exploring for future development, not an existing feature. Likewise, my recollection is that I tried to fix the addon but never became confident it worked as intended. No successful client test has been recovered or carried out during this documentation review.

## A possible future

Revisiting the addon for newer versions of World of Warcraft interests me, particularly if it can retain its roleplay character and offer more variety. Any port would first need a specific target client, a review of its addon API, and a working, tested baseline. This is an interest in future development, not a completed port or an approved release plan.

The GitHub repository is now **LevelUpAnnouncer**. Installed files, internal identifiers and the `/buxbrew` commands still use the historical **BuxbrewDing** name.
