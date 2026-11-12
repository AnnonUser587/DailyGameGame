# 🎲 DailyGameGame

All your daily games in one place. Tap a game to play it in a new tab, or hit **Random** to get one you haven't played yet today.

Made for iPhone first, and it works on desktop too.

## Features

- **One-tap play.** Every game opens in a new tab and gets checked off for today.
- **Random mode.** It only picks games you haven't played today, so you never get the same one twice in a day. You can reroll, skip one for the day, or roll from favorites only.
- **Resets at midnight** (your local time), with a countdown.
- **Progress ring and 🔥 streak** for days you played at least one game.
- **Add your own games.** Tap **+**, paste a link, and the name fills in by itself. You can pick an icon and category, edit or delete them, and hide built-in games you don't play.
- **Favorites, search, and filters** (Unplayed / Played / category).
- **Share your games** as a link. Anyone who opens it can add them in one tap.
- **Backup / restore** to a JSON file.
- **Installable app (PWA).** Add it to your home screen and it opens full-screen like a real app, even offline.
- Light/dark mode, plus keyboard shortcuts on desktop (`r` = random, `/` = search).

All data is stored on your device (localStorage). No accounts, no server.

## Put it on GitHub Pages (free)

1. Create a new repository on GitHub (for example `dailygamegame`).
2. Upload **all** these files, keeping the `icons` folder:
   ```
   index.html
   manifest.webmanifest
   sw.js
   icons/
   README.md
   ```
3. In the repo go to **Settings → Pages**. Under *Source* pick **Deploy from a branch**, then branch **main** and folder **/ (root)**, then **Save**.
4. After about a minute your site is live at `https://YOUR-USERNAME.github.io/dailygamegame/`.

## Install on iPhone

Open the link in **Safari**, tap **Share** (the square with an arrow), then **Add to Home Screen**.

## Add more built-in games

Edit the `BUILTIN` list near the top of the `<script>` in `index.html`:

```js
{id:"mygame", name:"My Game", url:"https://mygame.com/", emoji:"🎯", tag:"Puzzle"},
```

`tag` can be: Words, Puzzle, Numbers, Geography, Guessing, Skill, Trivia, Other.

After changing files, bump `VERSION` in `sw.js` (e.g. `dailygamegame-v5`) so installed phones pick up the update.

## Handy links

- `…/dailygamegame/?random` opens straight into a random roll (good for a home-screen shortcut)
- `…/dailygamegame/?add=https://somegame.com&name=Some%20Game` opens the add form pre-filled
