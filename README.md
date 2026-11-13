# Every App Is an Argument

**A practical framework for judging software, open source, and AI, built for queer people and anyone else who'd like more control over their tech.**

> 🎤 **Presented Saturday, October 24, 2026** at the **oSTEM 2026 Annual Conference** in Albuquerque, New Mexico.
> A 60-minute interactive workshop by **Will Mitchell** (he/they), chapter president of oSTEM at Montana State University.

| | |
|---|---|
| 📑 **Slides (PDF)** | [`slides/every-app-is-an-argument.pdf`](slides/every-app-is-an-argument.pdf): every slide with all clicks revealed |
| 🛠️ **Slides (source)** | [`slides/`](slides/): the Slidev deck as presented, with speaker notes ([how to run it](slides/README.md)) |
| 🧭 **Run of show** | [`docs/run-of-show.md`](docs/run-of-show.md): minute-by-minute plan with slide numbers |
| 🔎 **Companion site** | [ossfidelity.com](https://ossfidelity.com) · [how to use it](docs/using-ossfidelity.md) · [source](https://github.com/willmitchellcodes/ossfidelity) |
| 📚 **Sources** | [`SOURCES.md`](SOURCES.md): by slide, plus the full 258-item bibliography |
| 🔬 **Research** | [`docs/research-brief.md`](docs/research-brief.md): the verified research report behind every claim |

## The idea

Every app makes a case for why you should use it: it's free, your friends are on it, it came preinstalled, it says it respects your privacy. This workshop teaches four questions for checking that case, borrowed from classical rhetoric.

| Appeal | Question | How it gets exploited |
|---|---|---|
| **Pathos** | Why do I want it? | Wants get engineered: defaults, "free," everyone's already on it |
| **Ethos** | Who's behind it, and who else vouches for it? | Trust gets faked: fake GitHub stars, a trusted contributor who planted a backdoor (xz-utils) |
| **Logos** | What can I check? | Evidence gets gamed: a checked box isn't proof of consent |
| **Kairos** | Why now? Is it still true? | The ask is timed and facts expire: setup screens, relicensing, changed terms |

Three appeals come from Aristotle; *kairos* comes from the sophists. Pointing them at software builds on Bogost's procedural rhetoric and on lateral reading (Wineburg & McGrew).

## How the session went

| Time | Part | Slides |
|---|---|---|
| 0:00–9:30 | **Opening.** Smart TVs that watch what you watch; software keeps public records; who I am; the techno-queer stakes (Grindr, location data, AI that misreads queer people); the thesis | 1–16 |
| 9:30–17:15 | **Part 1: the framework.** One story per appeal, why open source matters, then the TV examined four ways | 17–28 |
| 17:15–40:45 | **Part 2: AI and your apps.** What the AI productivity data actually says, *activity: audit your apps*, open source swaps, a live local-model demo (IBM Granite 4.2 with Wi-Fi off) | 29–53 |
| 40:45–60:00 | **Part 3: open source projects and OSS Fidelity.** *Activity: which would you install?*, seven checks before installing, where code is hosted, *activity: predict the grade*, auditing the auditor, one change to make | 54–70 |

Slides 71–95 are backup.

## Try it yourself

1. **Audit your apps.** List five apps you use every day. For each one, ask *who controls this data?* (ethos) and *could I leave if it changes?* (kairos). Star the one you'd most like to leave.
2. **Pick a swap.** Find an open source alternative for your starred app. Slide 46, or section 9.6 of the [research brief](docs/research-brief.md#96-start-here-summary), has one "start here" pick per category.
3. **Predict the grade.** Choose an open source tool, guess its grade from A to F, then check it on [ossfidelity.com](https://ossfidelity.com). The [tutorial](docs/using-ossfidelity.md) walks through it.
4. **Write it down.** One app to switch, one question to ask, one setting to change.

## What's in this repository

```
README.md               ← you are here
SOURCES.md              every citation: by slide, additions, full bibliography
slides/                 Slidev source as presented (slides.md, style.css, public/)
  every-app-is-an-argument.pdf
docs/
  using-ossfidelity.md  tutorial for the companion site
  run-of-show.md        timing plan, slide by slide
  research-brief.md     the research report (evidence cutoff Oct 21, 2026)
  graphics.md           alt text and source for each of the 44 charts
  process/              how the deck and site were planned and revised
data/                   CSV data behind every chart
```

## Accuracy and care

- Every number in the deck was checked against a primary source before the talk. Claims that couldn't be verified are labeled as such in the research brief.
- Company policies, court cases and software licenses change. Treat everything here as **true as of late October 2026**, and re-check anything you rely on. This is not legal advice.
- **Content note:** the talk and research discuss surveillance, outing risk, arrests, and mental-health statistics.
- The presenter built OSS Fidelity with AI assistance and disclosed it in the talk (slides 8 and 39).

## Thanks

To oSTEM for hosting, to Queer in AI for its research and its grad-application aid program, and to everyone who came to the session.
