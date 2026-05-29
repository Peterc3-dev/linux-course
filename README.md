# Linux Course

An interactive, single-page web course that teaches Linux fundamentals to people
coming from Windows. Framed as "unlearning" Windows habits rather than starting
from scratch.

## What it is

A single self-contained `index.html` file (HTML + CSS + vanilla JavaScript, no
build step, no dependencies beyond two Google Fonts loaded over the network).
It covers 8 sections:

1. The filesystem is not a drive
2. Paths: forward slashes & roots
3. Everything is a file
4. Permissions & ownership
5. The terminal is not CMD
6. Cloning: what it actually does
7. Building from source
8. Package managers vs installers

Each section pairs a Windows assumption with the Linux reality, plus code
examples and analogies. There are inline multiple-choice quizzes that give
correct/wrong feedback on click, a simulated terminal-input check, "mark section
complete" toggles, and a scroll-position progress bar.

## Status

Working, but a small static prototype — it's one HTML file, not a course
platform. Content is concept-oriented (read + answer quizzes); it does not run a
real shell or sandbox. Quiz answers and section-complete state are not persisted
(no localStorage), so progress resets on reload.

## Run it

No build or server required. Either:

- Open `index.html` directly in a browser, or
- Serve the folder, e.g. `python3 -m http.server` then visit
  `http://localhost:8000`.

An internet connection is used only to load the JetBrains Mono / Syne web fonts;
everything else works offline.

## Limitations

- Content scope is the 8 sections above — introductory, not comprehensive.
- The "terminal" is a styled input with an answer check, not a real emulator.
- No progress persistence across page reloads.
