# Celeste Classic collection

A small static collection of browser-playable Celeste PICO-8 games and community resources.

## Choose a game

Open [`index.html`](index.html) to choose a game:

- **Celeste Classic** — [`inbuilt/classic/`](inbuilt/classic/), the original game.
- **Celeste Classic 2: Lani's Trek** — [`inbuilt/two/`](inbuilt/two/), the follow-up.

Both game pages include an **All games** link back to the selector, so you can switch if you opened the wrong game. The [`inbuilt/speed/`](inbuilt/speed/) directory contains the community hub, practice mods, and downloads.

## Layout

The repository root holds only the game selector page. Every app lives under [`inbuilt/`](inbuilt/):

```
index.html          game selector
inbuilt/
  classic/          Celeste Classic (celeste.js, celeste.p8.png)
  two/              Celeste Classic 2: Lani's Trek (index.html, index.js)
  speed/            community hub, practice mods, downloads, fonts
classic/index.html  redirect stub -> inbuilt/classic/
two/index.html      redirect stub -> inbuilt/two/
speed/index.html    redirect stub -> inbuilt/speed/
```

The three stubs at the old paths exist only so links shared before the move still resolve; they forward to the matching app under `inbuilt/`. Each app is self-contained inside its own directory, so all of its assets and scripts stay relative to it.

## Run locally

Serve the repository root over HTTP (the game builds do not run from `file://` URLs):

```sh
python3 -m http.server 8000
```

Then visit <http://localhost:8000>. The repository is static and does not need a build step.
