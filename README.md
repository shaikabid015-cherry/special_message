# Lucky_Asking – A Personal Interactive Message Website

**Live URL:** [---not deployed yet---]  
**GitHub:** [github.com/shaikabid015-cherry/special-message]

## Overview
A single‑page HTML/CSS/JS website designed to deliver a heartfelt, interactive message to a special person. It combines nostalgic typewriter animation, custom modals, persistent exit‑intent reminders, and a back‑button override to ensure the message is seen.

## Features
- **Typewriter effect** – Paragraph 1 types itself letter by letter.
- **Animated clickable link** – Pulsing + wiggling “please remember our chat” button.
- **Modal popup (paragraph 3)** – Scrollable, fully customisable bold/highlight message.
- **Exit‑intercept logic** – Custom popup on every back‑button press, plus browser “beforeunload” warning.
- **Floating reminder** – Stays visible until the link is clicked.
- **Fully responsive** – Works on mobile and desktop.
- **Zero backend** – Static files, deploy anywhere (Vercel, Netlify, GitHub Pages).

## Tech Stack
- HTML5
- CSS3 (flexbox, keyframe animations, custom scrollbar)
- Vanilla JavaScript (no frameworks)

## How to Run Locally
1. Download or clone the repository.
2. Place your own `background.jpg` and `study.jpg` in the same folder as `index.html`.
3. Open `index.html` in any modern browser.

## Customisation Points
- **Paragraph 1 text** → Edit the `textBeforeLink` variable inside the `<script>` tag.
- **Paragraph 2** → Edit the `<div class="para2">` content.
- **Paragraph 3 (modal)** → Edit the `<div id="specialModal">` content (supports HTML).
- **Background & study images** → Replace the filenames in `<style>` and `<img>`.
- **Modal scrollability** → The `.modal-content` CSS includes `max-height: 80vh` and `overflow-y: auto`.

## Deployment on Vercel
1. Push the folder (containing `index.html` + images) to a GitHub repository.
2. Import the repository into Vercel.
3. Vercel automatically detects static files – no configuration needed.
4. You get a live URL instantly.

## Known Behaviour
- The back‑button override uses `history.pushState` and `popstate` – it will show the custom popup **every time** the back button is pressed.
- The `beforeunload` event triggers on tab/close, asking the user to stay.
- After clicking the special link, the floating reminder disappears.

## License
Free to use and adapt for personal, non‑commercial purposes.
