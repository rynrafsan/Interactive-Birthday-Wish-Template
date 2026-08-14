# 💌 Birthday Surprise — Interactive Website Template

A single-file, zero-build-tools "birthday surprise" web experience: a personalized login gate, a private passcode quiz, an Instagram-Stories-style recap, an animated relationship map, scratch-to-reveal coupons, a museum-style photo gallery with a full-screen story viewer, a complete light/dark theme toggle, and a countdown-gated letter reveal with a reply-by-email box.

Originally built as a real birthday gift for my girlfriend — this is the open, personal-info-free template version so anyone can fork it and build their own.

**🔗 Live demo:** *add your GitHub Pages link here*
**🧪 Try it:** the login and passcode screens show their own demo hints, so you can click straight through.

## Features

- 🔐 Custom login screen (your own username/password)
- ❓ A 4-question passcode gate — one exact match, one multi-answer nickname check, two normalized string matches
- 📊 A tap-to-advance "wrapped" recap with animated rolling counters
- 🗺️ An animated SVG map connecting the places that matter to the two of you
- 🎟️ Scratch-off coupon cards with a real canvas-based scratch effect
- 🖼️ Two "story" buttons plus a full masonry photo gallery, both opening a swipeable, auto-advancing full-screen viewer (Instagram/Snapchat-style)
- 🎨 A genuine theme system — a single toggle swaps every color, gradient, and confetti particle across every screen between a rose/pink palette and a dark "baddie" palette
- ⏳ A live, ticking countdown timer
- 💌 A confetti-triggered letter reveal, plus a reply box that opens straight into the visitor's email app (with a copy-to-clipboard fallback)

## Tech stack

React 18 + Tailwind CSS, both loaded via CDN, with JSX transpiled in-browser by Babel Standalone. No `npm install`, no bundler, no build step. Open `index.html` directly in a browser, or host it anywhere that serves static files (GitHub Pages, Netlify, Vercel, S3, etc.).

## Customize it

Everything you'd want to personalize lives in one `CONFIG` block near the top of the `<script>` tag:

| Constant | What it controls |
|---|---|
| `PARTNER_NAME` | The name shown throughout the site |
| `LOGIN_CREDENTIALS` | Username/password for the login screen |
| `PASSCODE_ANSWERS` / `ACCEPTED_NICKNAMES` | Answers for the 4-question passcode gate |
| `REUNION_TARGET` | The countdown target date |
| `REPLY_EMAIL` | Where the reply box sends its message |
| `GITHUB_URL` | The "view the code" link on the last screen |

The questions, map pins, scratch coupons, and letter text are just below the `CONFIG` block in their respective components — search for the component name (`PasscodeGateway`, `ConnectionMap`, `ScratchCoupons`, `ReunionVault`) to find them.

**On photos:** nothing personal ships in this repo. Every "photo" you see is generated on the fly (an SVG gradient + emoji, via the `svgPhoto()` helper) so the template is safe to publish as-is. Swap in your own images by replacing the `photos`/`src` values with your own URLs — a public image host, your own GitHub repo, or a Google Drive file shared as "anyone with the link" and referenced via `https://drive.google.com/thumbnail?id=FILE_ID&sz=w1000` all work well.

## Why this exists

I built the original for my girlfriend's birthday as a fully interactive, personalized experience rather than a normal gift. It turned out to be a fun front-end problem — state machines for the gated flow, a canvas scratch-card effect, a theming system driven entirely by CSS custom properties, a reusable story-viewer component — so I cleaned it up into something anyone can fork.

## License

MIT — fork it, remix it, surprise someone. ⭐ a star is appreciated if you use it!
