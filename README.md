# Baize Solitaire

Klondike patience for iPhone. It runs with no network connection once it has been added to the home screen.

## What's in the folder

- `index.html` – the whole game (no external fonts, scripts or images)
- `sw.js` – stores the game on the phone so it opens offline
- `manifest.webmanifest`, `icon-180.png`, `icon-512.png` – home-screen name and icon

## Getting it onto your iPhone

iOS only keeps a web app for offline use if Safari has loaded it once from an `https://` address. So the folder needs hosting somewhere, once. GitHub Pages is free:

1. Create a new public repository on GitHub, for example `baize-solitaire`.
2. Upload the five files above to the root of the repository.
3. In the repository, go to Settings → Pages, choose "Deploy from a branch", pick `main` and `/ (root)`, then save.
4. After a minute the site is live at `https://<your-username>.github.io/baize-solitaire/`.
5. On the iPhone, open that address in Safari, tap Share, then "Add to Home Screen".
6. Open it once from the home-screen icon while still online. From then on it works in flight mode.

Your game in progress, draw setting and win count are saved on the phone.

## Playing

- Tap a card to send it to the best legal place (foundation first, then a tableau column).
- Or drag a card, or a run of face-up cards, to where you want it.
- Tap the stock to draw. When it's empty, tap the ↻ space to turn the waste back over.
- Draw 1 or Draw 3 is set at the top. A change made mid-game applies from the next deal.
- Undo goes back one move at a time. Finish appears once every card is face up and plays the rest out.
- New deal asks for a second tap if you're part-way through a game.

## Updating

If you change `index.html`, also change `baize-v1` in `sw.js` to `baize-v2` (and so on), or phones will keep the old copy.
