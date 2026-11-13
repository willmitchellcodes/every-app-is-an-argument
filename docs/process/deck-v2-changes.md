# How the deck changed before the talk

The deck was reviewed against its outline, the research, and the time budget on Oct 23, 2026, then rebuilt as v2 (the version presented and published here). This is the change log from that pass. Slide numbers are v2's.

## Theme: "marked-up argument" (Oct 23)

The deck looks like an argument being marked up: you're teaching people to edit an app's case the way a critic marks up an essay.

- **Colors:**
  - Lavender paper `#F5F2FC`, a long-standing queer color.
  - Aubergine ink `#211833`.
  - Violet print `#5B36C9`.
  - Chartreuse highlighter `#D6F25B`. Lavender and chartreuse are also the genderqueer flag's pair.
  - Hot pink `#C2245E` for notable data and annotations.
- **The four appeals** each have a sticker color, used the same way everywhere: Pathos pink, Ethos lavender, Logos chartreuse, Kairos aqua.
- **Type:** Recursive, one family for headlines (casual axis), body text (linear) and URLs (mono). It's bundled in `public/fonts/` (SIL Open Font License), so it works on offline Wi-Fi. You no longer need Inter or JetBrains Mono installed.
- **Charts:** all 44 were recolored from the SVG sources into `public/graphics-lav/`. The new pair (violet vs. pink) passes colorblind-separation checks. The old green vs. orange pair didn't under protanopia.
- **Motion:** one moment per slide.
  - The highlighter swipes in under the emphasized word.
  - Stickers pop on, and framework cards deal in.
  - Big numbers stamp in.
  - Section slides slide up.
  - The cover star turns slowly.

  All of it turns off when the computer asks for reduced motion, and in PDF export.

## What changed from v1

Slide numbers below are v2's.

**Structure**
- Three parts, matching the roadmap (slide 16): four questions; use them on AI and your apps; use them on open source and on the site.
- The queer "why" now comes before the method: techno-queer (9), documented risks (10), the Grindr ruling (11–12), "more options, less control" (13), then the thesis (14).
- Part 1 ends with a worked example: the TV, four ways (28). It shows the pattern the audience uses next. The order is I do (TV), we do (Granite, 49), you do (audit 41–45, predict-the-grade 63).
- New slide: "Why do we care about open source?" (27). It makes the small argument about who software is built for (ads and data retention vs. a commons you can leave), with the tradeoffs in the notes.
- 75 → 70 main slides; two of them are demo fallbacks you skip if the demos work. Nine dense graphics moved to backup.

**Framework**
- Kairos is now "Why now? Is it still true?" The framework slide credits "three appeals from Aristotle, plus kairos from the sophists."
- One click on the framework slide (18) reveals how each appeal gets exploited: wants get engineered, trust gets faked, evidence gets gamed, the ask is timed and facts expire.
- Every slide that uses an appeal carries a small tag in its top-right corner.
- New Ethos slide on lateral reading (22).
- Logos now uses the Grindr consent ruling (23).
- Kairos opens with "When did your TV ask?" (24).
- The audit grid is rebuilt in HTML with its axes named Ethos and Kairos (42). The seven install checks are sorted under the four questions (58). The three site grades show their appeal, and the slide says pathos is never scored (62).
- New closer before the recap: "Now check my site" (66), the four questions applied to OSS Fidelity.

**Content swaps**
- The NVDA slide is replaced by the presenter's own build-and-check story (39).
- The benefit stat is now Cui et al.'s +26% completed pull requests, so both numbers on that slide are about code (37).
- The local-model demo is Granite 4.2, with a four-question walkthrough first (49–50).
- The swap tables became one readable "Start here" slide (46) and a "Free isn't open source" statement (47). The full tables are in backup.
- Code hosts are three cards, with the Codeberg vote folded in (60).
- Research and open source logos are merged onto one slide; the fun fact is a click on the "Hi" slide; the browser question is now in the notes for slide 19.
- Recap comes before the write-down; the $750 slide follows.

**Fact fixes**
- RFC 1 is "the first ARPANET Request for Comments."
- LG's settlement is quoted from the Texas AG's release; "no money" is dropped.
- METR is described in the past tense.
- Techno-queer uses the presenter's working definition (Oct 23) and credits Edmond Y. Chang (2012).
- Bandura is cited as "especially influential."
- The Signal fallback card now says "cached grades."
- Sources were added to every slide with a number that lacked one.

