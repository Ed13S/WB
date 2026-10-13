# WB — Systems Engineering & Physics 3&4 Interactive Study Guide

An interactive, single-page revision companion for **VCE Systems Engineering Units 3&4** and **VCE Physics Units 3&4**, built for exam revision against the 2026 study design. The idea: *see the systems, not just the formulae.*

Everything lives in one self-contained file, `index.html`. There is no build step, no dependencies to install and no server required.

## Features

- **Two subjects, one site.** Switch between Systems Engineering and Physics from the top bar; each has its own section menu.
- **Live interactive diagrams.** Animated SVG simulations let you change inputs and watch the result, including formula triangles, voltage dividers, diodes and rectification, transistors, capacitor charge/discharge, gears, simple machines, springs, hydraulics and more.
- **Flashcards.** Flip through formulas and key ideas, with shuffle.
- **Progress tracking and bookmarks.** A contents sidebar shows which sections you have reviewed. Progress, bookmarks and theme are saved in your browser.
- **Site search.** Search across the whole guide from the top bar.
- **Ask AI (optional).** A chat panel that knows which section you are viewing, with *Simpler*, *Deeper* and *Quiz me* shortcuts. It uses your own free [OpenRouter](https://openrouter.ai/keys) API key.
- **Light and dark themes**, plus **print / save as PDF** support.
- **Worked examples, a study priority guide and a glossary** for exam prep.

## Contents

### Systems Engineering

1. The Systems Engineering Process
2. Control, Integration & Feedback
3. Formula Triangles
4. Circuits: Series, Parallel & Voltage Dividers
5. Diodes & Rectification
6. Transistors
7. Capacitors
8. More Electrotechnological Components
9. Motors, Solenoids, Generators & Switching
10. Magnetism
11. Motion & Free Body Diagrams
12. Torque & Moments
13. Vectors
14. Simple Machines
15. Springs
16. Hydraulics & Pneumatics
17. Ethical Design, Systems Production & Risk
18. Clean Energy Technologies
19. New & Emerging Technologies
20. Electrotechnology Symbol Reference

### Physics

- Motion
- Fields
- Electromagnetic Induction
- Waves, Light & Quanta
- Einstein's Special Theory of Relativity
- Physics Formula Sheet

### Shared

- Worked Examples
- Study Priority Guide
- Glossary

## Getting started

**Online:** if GitHub Pages is enabled for this repo, open the published site.

**Locally:** clone the repo and open the file in a browser.

```bash
git clone https://github.com/Ed13S/WB.git
cd WB
open index.html   # macOS; on Windows/Linux just double-click the file
```

The site opens on a lock screen styled as a search box. Enter the access phrase to unlock it; your browser remembers the unlock, and the 🔒 

## Setting up Ask AI

1. Create a free key at [openrouter.ai/keys](https://openrouter.ai/keys).
2. Click the 🤖 button in the top bar, then ⚙️ (settings).
3. Paste your key and pick a model. The default is `openrouter/free`; any free model slug ending in `:free` also works.
4. Open the chat and ask away. The panel shows which section it is "watching" and uses it as context.

Your key is stored only in your browser's `localStorage` and is sent only to OpenRouter. It is never written into the repo. If your chosen model supports image input, the chat can also see the diagram you are looking at; text-only models simply ignore it.

## Project structure

```
WB/
├── index.html   # the whole site: markup, styles and scripts
└── README.md
```

## Tech notes

- Plain HTML, CSS and vanilla JavaScript, with no frameworks or build tooling.
- Diagrams are generated with inline SVG and animated with `requestAnimationFrame`.
- Browser storage is used for the unlock state, theme, progress, bookmarks and the optional AI settings.
- The only network call is the optional Ask AI request to `openrouter.ai`.

## Editing the guide

Each topic is a `<section class="topic">` in `index.html`, with a matching link in the top navigation. To add a topic, copy an existing section, give it a new `id`, and add a link in the relevant submenu (`submenu-systems` or `submenu-physics`).

## Disclaimer

This is an unofficial study aid and is not affiliated with or endorsed by the VCAA. Always check the current official study design and exam specifications. This website was built to 2026 specifications. and therefore is correct as at 2026.
