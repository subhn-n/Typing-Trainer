# Typing Trainer

A local, static typing trainer that runs in the browser with no backend and no external API.

## Features

- random phrase mode
- custom mode by letter
- random French and English words loaded from local JSON files
- infinite custom-mode series
- WPM calculation
- accuracy percentage
- automatic timer on first keystroke
- target WPM selector: 20, 40, 60, 80, 100, or 120 WPM
- subtle pace cursor showing the target typing rhythm
- restart button and `*` keyboard shortcut
- last completed score shown in the header
- responsive interface
- compatible with GitHub Pages

## Custom Mode

1. Choose a letter in `Custom Mode`.
2. Click `Change Letter` to start a series with that letter.
3. Every displayed word contains the selected letter.
4. When a series is copied exactly, a new series is generated automatically.
5. `Next Letter` moves to the next alphabet letter.
6. `Exit Custom Mode` returns to random phrase mode.

The interface shows the current WPM, accuracy, time, progress, selected letter, and last completed score.

## Target WPM

Use `Target WPM` to choose a target speed. The thin gray cursor over the text moves at the pace required to reach that WPM. It starts when typing begins and resets on `Restart`. Press `*` while typing to restart without inserting the character.

## Dictionaries

Generated files:

- `data/french_words.json`
- `data/english_words.json`

Sources used:

| Language | Source | Link | License | Type |
|---|---|---|---|---|
| French | `words/an-array-of-french-words` | https://raw.githubusercontent.com/words/an-array-of-french-words/master/index.json | MIT | JSON |
| English | `words/an-array-of-english-words` | https://raw.githubusercontent.com/words/an-array-of-english-words/master/index.json | MIT | JSON |

The lists were cleaned locally to keep words between 3 and 18 characters.

## Open Locally

Because custom mode loads local JSON files, use a local server from the workspace root:

```bash
python3 -m http.server 8000 -d projects/typing-trainer
```

Then open:

```text
http://localhost:8000
```

Random phrase mode can also work by opening the HTML file directly:

```bash
xdg-open projects/typing-trainer/index.html
```
