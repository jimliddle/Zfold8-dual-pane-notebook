# FoldFolio

FoldFolio is a single file notebook web app built for foldable phones such as the Samsung Galaxy Z Fold 8. It turns the unfolded inner screen into a two page paper notebook with a 3D cover, page turning animations, pen support, and local storage.

Everything runs from a single `index.html` file with no build step, backend, or account required.

## What It Does

- **3D Cover & Elastic Strap:** Opens onto a closed hardcover book. Pull the elastic strap left or right (or swipe the cover) to snap it open. You can also jot quick notes or tasks straight from the closed cover.
- **Full Screen Dual-Page Spread:** Opens into a clean, two page spread with a center spine shadow and stacked paper edges. Both the top menu tabs and the bottom pen bar stay hidden by default so the screen looks like plain paper. Pull the top red ribbon or bottom pen tab to show the controls when you need them.
- **PageTurn Physics & Sound:** Drag or tap the bottom page corners to curl pages back and forth across the crease, complete with synthesized paper and strap sounds.
- **TapAnywhere Writing & Pen Drawing:** Tap any line on the page to start typing right on that row, or switch to the Pen, Highlighter, and Rubber (eraser) tools to draw directly on the page. Includes multi step undo (`Ctrl+Z` or the Undo button).
- **Notes & Checklists:** The left page is for freeform notes. The right page can switch between companion notes and an action checklist.
- **Web & PDF Clippings:** Tape live, resizable mini webpages (`+Web`) or multi-page PDF files (`+PDF`) directly onto either page and drag them around your notes.
- **Custom Paper, Covers & Fonts:** Pick from 5 cover colors, 4 paper stocks (white, cream, kraft, blueprint), 4 page layouts (lined, dotted, grid, blank), and 10 handwriting or book fonts.
- **Local IndexedDB Storage:** All pages, drawings, clippings, tasks, and preferences are saved locally in your browser's IndexedDB (`FoldFolioVault_v3`). You can wipe the database clean at any time from the Vault menu.
- **Optional Gemini AI:** Add your own Gemini API key in the Vault menu to summarize your open spread, chat with your notes, or pull tasks out of your handwriting into the checklist.
- **Export & Share:** Jump between saved spreads from the Index menu, start new note sections, or export your current spread or full notebook to `.md` (Markdown) or `.txt`.

## How to Use It

### 1. Run Locally or Host Anywhere
Because the entire app is inside `index.html`, you can:
- Open `index.html` directly in your browser.
- Host it on GitHub Pages, Netlify, Vercel, or any static file server.
- Access it directly at: https://jimliddle.github.io/Zfold8-dual-pane-notebook/

### 2. Install as an App (PWA) on Galaxy Z Fold 8
FoldFolio includes an embedded web manifest and icon so you can install it to your home screen:
1. Open the hosted `index.html` page in Chrome or Samsung Internet on your phone.
2. Tap the browser menu and select **Add to Home screen** / **Install app**.
3. Launch it from your home screen for a full screen, edge-to-edge layout without browser bars.

## Controls Quick Guide

- **Open the Book:** Drag or tap the elastic band on the front cover.
- **Show Top Menu:** Tap or pull down the red ribbon at the top center crease.
- **Show Pen & Rubber Bar:** Tap or pull up the `Pen Bar` handle at the bottom center crease.
- **Turn Pages:** Drag or tap the bottom left or bottom right page corners, or use the `<` and `>` arrows in the bottom bar.
- **Add Gemini Key / Clear Data:** Pull down the top ribbon and tap the green database icon on the far right.

## Tech Stack

- Single file HTML5, CSS, and vanilla JavaScript
- [Tailwind CSS](https://tailwindcss.com/) (CDN)
- [Lucide Icons](https://lucide.dev/)
- [Tone.js](https://tonejs.github.io/) & Web Audio API for paper and strap acoustics
- [PDF.js](https://mozilla.github.io/pdf.js/) for rendering PDF clippings on the page
- Browser `IndexedDB` for offline local storage

## License

MIT
