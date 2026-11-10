# LevelUpAnnouncer

**By Babuni** · Formerly **BuxbrewDing** · World of Warcraft 1.12

This is my early level-up announcement addon. It contains 60 prewritten roleplay messages, one for each level from 1 to 60, and attempts to announce the appropriate message in guild chat when the character gains a level. Private previews and manual guild announcements are available too.

## Why I made it

A level-up feels like something worth celebrating, especially on a hardcore server where every milestone means the character has survived a little longer. Rather than keeping that moment to myself, I wanted to share it with the guild. The roleplay messages were my way of making that celebration more expressive than a routine level notification.

Variety mattered to me, but the checked-in code has **one fixed message for each level**, not a random selection of alternatives for the same level. From memory, attempts to repair the original addon never left me confident that it worked reliably. That is a personal recollection, not a newly established test result.

At my direction, I renamed the GitHub repository from `BuxbrewDing` to **LevelUpAnnouncer** because the new name explains the function without requiring knowledge of my character. The installed addon still uses `BuxbrewDing.lua`, `BuxbrewDing.toc` and the `/buxbrew` commands.

## Installation and commands

Install the existing addon files under `Interface/AddOns/BuxbrewDing/`. The manifest declares interface **11200** and version **1.0**; current client compatibility has not been independently verified.

| Command | Source-observed behavior |
| --- | --- |
| `/buxbrew 30` | Preview the level 30 line locally |
| `/buxbrew test 30` or `/buxbrew preview 30` | Local preview |
| `/buxbrew announce 30` or `/buxbrew send 30` | Attempt a guild announcement |
| `/buxbrew help` | Show commands |

## What still needs verification

The source uses `string.match`, which needs checking against the intended Lua 5.0 client. The manifest does not declare saved variables, so the level tracker should not be described as persistent. Manual sends have no rate limiter and may name levels other than the character's current level. No fresh game test was performed during this documentation revision.

## History

GitHub records early Lua changes on **August 27, 2025**, including edits to level-specific messages. My original detailed writing and testing process has not been recovered, so I am keeping that part of the history open rather than inventing it. In November 2026 I asked AI to help rename the project in its documentation and tell the story from my perspective. The project name changed on GitHub, but the runtime addon was not renamed.

- **Project** — [Concept](CONCEPT.md), [Changelog](CHANGELOG.md)
- **History** — [Journal](docs/DEVLOG.md), [Collaboration](docs/AI_COLLABORATION.md), [Decisions](docs/DECISIONS.md)
- **Reference** — [Development rules](AGENTS.md)
