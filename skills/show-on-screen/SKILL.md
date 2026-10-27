---
name: show-on-screen
description: Show content on a Screenbird screen or sub-screen, now or until a set time, and switch it back afterwards. Use when the user wants something shown on one of their screens.
---

# Show content on a screen

1. Call `list_screens`, with `query` when the user names a screen. Note the screen id, any sub-screens, what it shows now, and the account's time zone and local time.
2. Call `search_content` with part of the content's name. Content can be a file, a design, an app, a split screen or a playlist.
3. If more than one screen or item matches, show the candidates and let the user choose. Changing a screen changes what people see there, so confirm first unless the request is explicit.
4. Call `push_content` with `screen_id` and `content_id`, plus `subscreen_id` for a sub-screen. For something temporary, set `until` to the account's local time without an offset, for example `2026-11-02T14:00`. Leave `until` out to keep the content on the screen until you switch it back.
5. Tell the user what the screen shows now and until when. If the result reports that the screen is offline or has no player paired, explain that the content appears as soon as the screen is online.

To switch a screen back to its own content, call `release_screen` with the `screen_id`, plus the `subscreen_id` for a sub-screen.
