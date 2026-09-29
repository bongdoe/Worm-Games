# WORM: standalone edition

A modern 3D take on the classic Nokia-era Snake game, packed into **one HTML file**.

`worm.html` has everything built in: the game, the Three.js 3D engine, styles and fonts. It needs no install, no server, and no internet connection.

## Play

1. Download `worm.html`.
2. Double-click it (or drag it into a browser window).
3. Press **Start**.

That's it. You can copy the file to a USB stick, email it, or keep it on your phone.

## Controls

| Action            | Keyboard                         | Touch                          |
| ----------------- | -------------------------------- | ------------------------------ |
| Steer             | Arrow keys or WASD               | Swipe on the arena, or use the D-pad |
| Start             | Space, Enter, or any arrow key   | Start button, or any D-pad arrow |
| Pause / resume    | Space, P, or Esc                 | Pause button (top right)       |
| Restart           | Space or Enter on Game Over      | Restart button                 |
| Mute / unmute     | M                                | Speaker button (top right)     |

## How to play

- The worm starts 5 segments long and keeps moving forward.
- Eat the **orange gem** to grow by one segment and score **10 points**.
- After every 5th gem, a **gold bonus gem** appears for a short time. It's worth 20–60 points: the faster you reach it, the more you get. It blinks just before it disappears.
- The longer the worm gets, the faster it moves.
- Hitting a wall or your own body ends the game.
- You can't turn straight back on yourself, just like the original.

Your best score is saved in the browser. Clearing browser data resets it.

## Requirements

Any up-to-date browser with WebGL: Chrome, Edge, Firefox or Safari on desktop, Android or iOS.

If your system is set to reduce motion, the game turns off camera shake, bobbing and most particles automatically.

## Put it online

The file works as a web page as-is. To host it on **GitHub Pages**:

1. Rename `worm.html` to `index.html` and commit it to your repository (either the root or a `docs/` folder).
2. Go to **Settings → Pages** and set the source to that branch and folder.
3. After a minute, the game is live at `https://<your-username>.github.io/<repository>/`.

Any other static host (Netlify, Vercel, itch.io as an HTML game, your own server) works the same way.

## Troubleshooting

- **Black screen or "WebGL is not available":** turn on hardware acceleration in your browser settings, or try another browser.
- **No sound:** browsers only allow audio after you interact with the page, so press a key or tap first. Also check that the speaker button isn't muted.
- **Page scrolls or zooms on mobile:** open the file directly in the browser app rather than in a file-manager preview.

## Building it yourself

This file is generated from the full source project (Three.js + Vite). With Node.js installed, run this in the project folder:

```bash
npm install
npm run build:standalone
```

That writes a fresh `worm.html`. See the main `README.md` for the project structure and how to tweak speed, grid size, scoring and colors in `src/config.js`.
