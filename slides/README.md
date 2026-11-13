# Slides

The [Slidev](https://sli.dev) source for *Every App Is an Argument*, exactly as presented on Saturday, October 24, 2026 (deck v2).

**Just want to look?** Open [`every-app-is-an-argument.pdf`](every-app-is-an-argument.pdf). It shows every slide with all clicks revealed.

## Run it

Needs Node.js 18 or newer.

```bash
cd slides
npm install
npm run dev      # opens the deck at http://localhost:3030
                 # press P (or open /presenter/) for presenter view with speaker notes
npm run export   # writes a PDF (first run: npx playwright install chromium)
```

## What's here

| Path | Contents |
|---|---|
| `slides.md` | All 95 slides (70 main, 25 backup) with full speaker notes and timings |
| `style.css` | The "marked-up argument" theme |
| `public/graphics-lav/` | The 44 charts and diagrams. Alt text and sources: [`../docs/graphics.md`](../docs/graphics.md); data: [`../data/`](../data/) |
| `public/personal/` | Images for the "about me" slide |
| `public/fonts/` | Recursive, bundled so the deck works offline (SIL Open Font License, see `Recursive-OFL.txt`) |
| `public/qr-*.png` | QR codes for ossfidelity.com and its github.io fallback |

## Design

The deck looks like an argument being marked up, the way a critic marks up an essay:

- **Colors:** lavender paper, aubergine ink, violet print, a chartreuse highlighter, and hot pink for notable data. Lavender and chartreuse are also the genderqueer flag's pair.
- **The four appeals** each get a sticker color, used the same way everywhere: Pathos pink, Ethos lavender, Logos chartreuse, Kairos aqua.
- **Chart colors** (violet vs. pink) were picked to stay distinguishable for colorblind viewers.
- **Motion** turns off when the computer asks for reduced motion, and in PDF export.

## Speaker notes

The notes are left in, since they explain the reasoning behind each slide. Some are pre-talk reminders for the presenter.
