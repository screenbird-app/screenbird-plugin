---
name: check-screens
description: Show which of the user's Screenbird screens are offline and what each one is showing, and help set up a new screen. Use for questions like "which screens are offline?" or "how do I add a screen?".
---

# Check screens

For an overview, call `list_screens`. When the result has a `next_cursor`, pass it as `cursor` to get the next page, until there are no more pages. Report:

- screens that are offline or have no player paired;
- what each screen shows now: its own content, pushed content or screen mirroring, with the end time if there is one.

Keep the answer short and name the screens that need attention first.

For a new screen or device:

- `check_device` tells whether a device, for example "Samsung TV" or "Fire TV Stick", works with Screenbird.
- `get_install_steps` gives the installation steps for a device type, ending with the pairing code the user enters in the Screenbird dashboard.
- `search_help` searches the Screenbird help center for anything else. Answer from the articles it returns.
