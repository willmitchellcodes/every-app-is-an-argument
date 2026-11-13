# Using OSS Fidelity: a 5-minute tutorial

[ossfidelity.com](https://ossfidelity.com) helps you answer the workshop's *ethos*, *logos* and *kairos* questions for an open source project. It reads public data from GitHub and turns it into three grades, each with the reasons behind it.

No account, no cookies, no analytics.

## 1. Check a project

1. Go to **[ossfidelity.com](https://ossfidelity.com)**.
2. In the search box, either
   - **paste a GitHub link**, like `github.com/signalapp/Signal-Android`, or
   - **type what you need**, like `password manager` or `note taking`, and pick a suggestion.
3. Press **Check**.

You can also link straight to a result: `ossfidelity.com/check/?r=github.com/OWNER/REPO`.

## 2. Read the result

You'll see three grades, each a letter plus a number out of 100:

| Grade | Question it answers | Workshop appeal |
|---|---|---|
| **Reliability** | Will it still be here, and still be open? (license, bus factor, age, backing) | Ethos |
| **Maintenance** | Is someone still fixing it? (recent activity, releases, issue follow-through) | Kairos |
| **Visible security** | Which security practices can we see on GitHub? (security policy, dependency updates, code review, signed releases) | Logos |

**Fidelity** is the plain average of the three.

- Open **"Why?"** under any grade to see each signal, its weight, and its source.
- Move the **weight sliders** to see how the grade changes if you care about different things.
- A banner appears when a letter would change under equal weights, or when a project is quiet but "may be finished."
- A project with **no open source license** gets a banner and a capped Reliability grade.
- **AI-assisted commits** are shown for transparency but never scored.

## 3. Know the blind spots

A grade starts the conversation; it isn't a verdict.

- **Stars and downloads are never scored.** Popularity is easy to fake.
- **"Visible security" sees only what's on GitHub.** Signal scores low here because much of its review happens in-house, not in public pull requests.
- **Files are cheap.** Adding a few config files can move a small project's Security grade a lot. Read the "Why?" breakdown, not just the letter.
- **GitHub only, for now.** Projects that moved to Codeberg are detected and linked out.

## 4. Browse, compare, and learn

| Page | What it's for |
|---|---|
| **[Browse](https://ossfidelity.com/browse/)** | Hand-picked open source tools by category (local AI, communication, art & media, notes, office), regraded every Monday |
| **[Open models](https://ossfidelity.com/models/)** | Small open-weight AI models: how open they really are (weights, code, data), whether they fit on a laptop, and a benchmark anyone can rerun |
| **[AI privacy](https://ossfidelity.com/ai-privacy/)** | Seven questions for any AI service (training, processing, retention, human access, connected services, deletion, authorization), answered from each company's own pages with sources |
| **[Method](https://ossfidelity.com/method/)** | Every formula, weight, and reason |

## 5. Rate limits

Projects on Browse load instantly from the weekly scores. A brand-new **live check** makes 15–30 requests to GitHub; without the site's proxy, GitHub allows 60 per hour per network. On shared Wi-Fi, check a couple of projects at a time.

## 6. Run the four questions on the site itself

- **Pathos:** Why do you want a grade? (It's quick and feels objective.)
- **Ethos:** Who built it? One student, with AI help, disclosed on the site.
- **Logos:** What can you check? Every formula and source is public, and the code is open: [willmitchellcodes/ossfidelity](https://github.com/willmitchellcodes/ossfidelity).
- **Kairos:** Is it still true? Look at the "last scored" date on each result.

Found a project that should be on Browse, or a grade that looks wrong? [Open an issue](https://github.com/willmitchellcodes/ossfidelity/issues).
