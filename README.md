# Board Game Rules

Community-maintained game guides for the Board Game Helper Android app.

## Adding a game

1. Add a directory under `games/` containing `rules.md` and a landscape `header.png`.
2. Add the game to `catalog.json` with a unique stable ID, display text, default timer length, paths, and theme colours.
3. Keep images original or appropriately licensed. Do not copy official rulebook text or box artwork.

The app reads the catalog from the repository's `main` branch. Existing IDs and paths should remain stable so cached app content continues to work.

## Rules Markdown

Rule files support paragraphs, level-one and level-two headings, bullet lists, numbered steps, callouts beginning with `>`, and images.

Use standard Markdown image syntax. Image paths are resolved relative to the `rules.md` file:

```markdown
## Board setup

![Example board setup](images/board-setup.png)
```

For that example, store the image at `games/your-game/images/board-setup.png`. Absolute HTTPS image URLs are also supported. Write meaningful image descriptions because the app uses them for accessibility and displays them as captions.

## Catalog fields

- `defaultTimerSeconds` must be between 1 and 600.
- Colours use `#RRGGBB` or `#AARRGGBB` notation.
- `rules` and `image` may be repository-relative paths or absolute HTTPS URLs.

The included guides are concise references. The rulebook supplied with a game remains authoritative.
