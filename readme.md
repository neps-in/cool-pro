# Neps.in — Cool Hacks

A collection of small, browser-based tools built for web developers. No installs, no sign-ups — just open and use.

**Live:** [neps.in/hacks](https://neps.in/hacks)  
**GitHub:** [github.com/neps-in/cool-pro](https://github.com/neps-in/cool-hacks)

---

## Tools

### CSS Color Finder

**Path:** `/css-color-finder/`  
**Status:** Active

Paste any CSS snippet and instantly visualize every color value it contains. Colors are grouped by selector, inline property, or bare value — each shown as a labelled swatch card.

**Supported input formats:**

| Format                               | Example                                             |
| ------------------------------------ | --------------------------------------------------- |
| CSS selector block                   | `.btn { background-color: #2196f3; color: white; }` |
| Inline CSS variables / properties    | `--primary: #ff0000;`                               |
| Plain color values (comma-separated) | `#FF5733, #33FF57, #3357FF`                         |
| Mixed — any combination of the above | ✓                                                   |

**Supported color formats:** `#hex`, `rgb()`, `rgba()`, `hsl()`, `hsla()`, named colors (`red`, `blue`, `transparent`, etc.)

**How it works:**

1. The CSS text is parsed line by line using a custom `parseCssTextToColorMap()` function.
2. Colors found inside selector blocks are grouped under their selector name.
3. Properties outside selectors (CSS variables, standalone declarations) are grouped as `[inline properties]`.
4. Bare color values (hex strings, comma-separated lists) are grouped as `[inline colors]`.
5. Each color is rendered as a card with a visual swatch, property name, and value.

---

## Project Structure

```
/hacks
├── index.html              # Landing page — card grid of all tools
└── css-color-finder/
    ├── index.html          # CSS Color Finder (main tool)
    └── *.html              # Prototypes and earlier iterations
```

---

## Planned Tools

- **Log Parser & Visualiser** — paste server logs, filter/group/visualize errors, endpoints, and response times
- **JSON Formatter & Diff** — prettify, compare, and validate JSON payloads for APIs and webhooks

---

## Tech Stack

Pure HTML, CSS, and vanilla JavaScript. No frameworks, no build step, no dependencies.
