---
name: make-a-design
description: Create a full-screen Screenbird design, such as a menu, an announcement or an event poster, from the user's description, and optionally show it on a screen. Use when the user wants a new menu, announcement or poster for their screens.
---

# Make a design

1. Collect everything that must be on the design: the title and every line of text, with prices, dates, times and names exactly as the user gives them. Ask for anything that is missing instead of making it up.
2. Ask whether the screen is landscape or portrait if that is not clear.
3. Call `create_design` once, with a `brief` that holds all texts in the user's words, the `orientation`, the `language` of the texts and a short `name`.
4. Tell the user the design was created and what it is called. Each design uses the account's AI budget, with at most 20 designs per hour, so only create a new one when the user asks for changes.
5. If the user wants it on a screen, use the show-on-screen skill to put the new design on that screen.
