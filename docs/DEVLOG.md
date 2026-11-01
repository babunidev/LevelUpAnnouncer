# LevelUpAnnouncer — development journal

**By Babuni**

## August 2025 — BuxbrewDing

The original project was called **BuxbrewDing**. Its Lua source contains 60 distinct messages for character level-ups, with guild announcements and preview commands. GitHub records an initial Lua commit on **August 27, 2025** ([31689f3](https://github.com/babunidev/LevelUpAnnouncer/commit/31689f31b797e3355eb28d6c7b84709782a2d85c)). Another commit that day ([e6d6906](https://github.com/babunidev/LevelUpAnnouncer/commit/e6d69061ddf30d153b401237e39fb96d2b8b6bde)) revises some level-specific lines, including mount references.

The original writing and testing conversation is not recovered. My project history should not pretend to know why every line changed.

## October–November 2026 — reviewing the old project

On October 26, I had AI inspect the source and repository history and expand the documentation. That review identified Lua compatibility and persistence questions without running a game test.

During the next project naming pass, I chose **LevelUpAnnouncer** because it describes the function more clearly than the character-specific title. The GitHub repository was renamed accordingly. My AI assistant revised documentation and attribution at my direction; the original Lua, TOC and slash-command identifiers have not been changed. This is a record of documentation work, not verified runtime maintenance.

## November 2026 — remembering the original idea

What drew me to this addon was the joy of announcing a level-up, particularly on hardcore servers where surviving long enough to gain a level feels meaningful. Guild chat seemed like the right place to celebrate, and roleplay messages gave each milestone a bit more personality. Despite attempts to fix it, my recollection is that the addon never really worked reliably.

During this review, AI compared that recollection and my interest in randomized variety with the source: there is one fixed message per level, not a random pool. A future port to newer WoW clients is something I would like to explore, but no implementation or test has begun.
