# Contributing Translations — pvp-corev3

Thank you for helping translate the pvp-corev3 MDT / CAD system!
All translations are managed through **Weblate** — a free, browser-based translation platform.

---

## Quick start

1. Create a free account at **https://hosted.weblate.org**
2. Open the project: **https://hosted.weblate.org/projects/pvp-corev3/mdt-nui/**
3. Select your language → start translating
4. Your changes are automatically committed to this repository

No Git knowledge required.

---

## Adding a brand-new language

If your language does not exist yet, open a GitHub issue titled **"New language: \<name\>"** and mention the ISO 639-1 code (e.g. `fr` for French, `es` for Spanish).  
A maintainer will add the empty file and enable it on Weblate.

---

## File format

Translations live in `translations/locale/<code>.json`.  
The **source** (reference) file is `en.json`.

- Every key in `en.json` must exist in your translation file.
- Values may contain HTML-like color codes from FiveM (e.g. `~r~`, `~y~`) — keep them unchanged.
- Values may contain `{placeholder}` variables (e.g. `{id}`, `{unit}`) — keep them unchanged, only translate the surrounding text.

**Example:**
```json
"ban_permanent": "You are permanently banned. (ID: {id})"
```
→ German:
```json
"ban_permanent": "Du bist dauerhaft gebannt. (ID: {id})"
```

---

## Style guidelines

| Language | Formality       | Notes                                      |
|----------|-----------------|--------------------------------------------|
| English  | Neutral / brief | Source — do not change without maintainer  |
| German   | Informal (du)   | Police jargon welcome                      |
| Russian  | Neutral         | Use Cyrillic only, no transliteration      |
| *other*  | Neutral         | Match the tone of the English source       |

- Keep translations **short** — many strings appear in compact UI buttons.
- Uppercase words (e.g. `UNIT STATUS`) should stay uppercase in translations where it looks natural.

---

## How translations reach the game

A maintainer periodically runs `scripts/update-locale.ps1` in the private main repository,
which copies the JSON files from this community repo into the actual resource.
This is a manual step to ensure quality control before each release.

---

## Questions?

Open a GitHub issue or ask in the community Discord.
