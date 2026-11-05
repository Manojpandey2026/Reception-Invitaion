# Lalit & Deepa — Wedding Reception Invitation

A single-page, mobile-friendly digital invitation for the wedding reception of **Lalit & Deepa**, to be held on **Thursday, 19 November 2026, from 7:00 P.M. onwards** at **The Rosario – A Luxury Banquet**, Mahavir Enclave, New Delhi.

Built with plain HTML, CSS and JavaScript. There is no framework and no build step.

## Features

- "Tap to begin" welcome screen that starts the background music
- Music play/pause button (top right)
- Animated hero section with a couple caricature, floating gold particles and rotating rings
- Invitation section with a Ganesh shloka, blessings, and family details
- Date and time section with a twinkling-stars background
- Venue section with an embedded Google Map and a **Get Directions** button
- Live countdown to the reception (days, hours, minutes, seconds, in IST)
- RSVP section with tap-to-call phone links
- Scroll-reveal animations and a responsive layout for phones and desktops

## Project structure

```
.
├── index.html          # The whole invitation (HTML + CSS + JS)
├── caricature_3.png    # Hero image of the couple
├── music.mp3           # Background music
└── README.md
```

> `caricature_3.png` and `music.mp3` must be in the same folder as `index.html`, with exactly these names, or the image and music will not load.

## Run locally

Open `index.html` in any browser. Music starts after the first tap, because browsers block autoplay.

To serve it locally instead:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy for free with GitHub Pages

1. Open the repository **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Choose the `main` branch and the `/ (root)` folder, then click **Save**.
4. After a minute or two, the site is live at `https://<your-username>.github.io/<repo-name>/`.

Share that link with guests on WhatsApp or by message.

## Customize

All content is in `index.html`. Search for these items:

| What to change | Where to look |
| --- | --- |
| Names | `<title>`, `hero-names`, `p-name` |
| Parents / family lines | `inv-host`, `inv-blessing`, `p-lineage` |
| Date and time text | `hero-sub`, `date-main`, `date-time` |
| Countdown target | `new Date('2026-11-19T19:00:00+05:30')` in the script |
| Venue name and address | `venue-name`, `venue-sub`, `venue-addr` |
| Map pin and directions | `<iframe src=...>` and the `dir-btn` link |
| RSVP names and numbers | the `rsvp-card` block (`tel:` links) |
| Colors | CSS variables in `:root` (`--gold`, `--ivory`, `--bg`, ...) |
| Hero image | replace `caricature_3.png` |
| Music | replace `music.mp3` |

## Credits

Fonts from [Google Fonts](https://fonts.google.com/): Cormorant Garamond, Playfair Display, Cinzel and Montserrat. Map by Google Maps.

With best compliments — all relatives & friends.
