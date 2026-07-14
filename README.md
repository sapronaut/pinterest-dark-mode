# Pinterest Dark Mode (Chrome Extension)

## Install (unpacked, for personal use)

1. Unzip this folder somewhere permanent (don't delete it after installing — Chrome loads it from disk).
2. Open Chrome and go to `chrome://extensions`.
3. Turn on **Developer mode** (top-right toggle).
4. Click **Load unpacked** and select the `pinterest-dark-mode` folder.
5. Visit pinterest.com — it should load in dark mode automatically.

## How it works

It uses a CSS `filter: invert(1) hue-rotate(180deg)` trick on the whole page, then
inverts images/videos back so photos still look correct while the white UI
chrome becomes dark. No JavaScript, no data collection, no permissions beyond
running on pinterest.com.

## Notes

- If some element looks off (odd colors on a specific badge/icon), it's usually
  because Pinterest is using a background-image or SVG that needs to be added
  to the re-invert list in `dark.css`. Right-click it → Inspect → note the
  selector → add it to the `img, video, ...` rule.
- To disable, just toggle it off in `chrome://extensions`.
