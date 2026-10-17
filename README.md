# Celeste Classic collection

A small static collection of browser-playable Celeste PICO-8 games and community resources.

## Choose a game

Open [`index.html`](index.html) to choose a game:

- **Celeste Classic** — [`classic/`](classic/), the original game.
- **Celeste Classic 2: Lani's Trek** — [`two/`](two/), the follow-up.

Both game pages include an **All games** link back to the selector, so you can switch if you opened the wrong game. The [`speed/`](speed/) directory contains the community hub, practice mods, and downloads.

## Run locally

Serve the repository root over HTTP (the game builds do not run from `file://` URLs):

```sh
python3 -m http.server 8000
```

Then visit <http://localhost:8000>. The repository is static and does not need a build step.
