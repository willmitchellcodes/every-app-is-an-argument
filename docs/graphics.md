# Workshop graphics

> In this repository the deck's lavender versions are in [`../slides/public/graphics-lav/`](../slides/public/graphics-lav/) (same base names, no `-dark`/`-light` suffix), and the chart data is in [`../data/`](../data/). The original green dark/light PNG and SVG sets described below aren't included.

Graphics for "Digital Autonomy, Open Source, and AI" (oSTEM 2026), grouped by talk segment.

Each graphic has four files: `-dark.png` / `-dark.svg` use the slide palette (#0F1A14 background, Inter) at 16:9; `-light.png` / `-light.svg` are for print and the report. PNGs are 3200 × 1800. SVGs have text converted to outlines, so they render the same everywhere (drop them in Slidev's `/public`). Source data for each chart is in `../data/` as CSV.

Every graphic states its source on the image. Alt text below is ready to paste into Slidev (`![alt text](/file.png)`).

## Hook and AI context
Folder: `01-hook-ai-context/`

### ChatGPT use among U.S. adults, 2023–2026
`ai-01-chatgpt-adoption` · Report Figure 17 · Data: `../data/ai-01-chatgpt-adoption.csv`

**Alt text:** Line chart. Share of U.S. adults who say they have used ChatGPT: 18% in 2023, 23% in 2024, 34% in 2025 and 44% in 2026. The final segment is dashed because the 2026 question wording changed.

**Source:** Pew Research Center (2026)

### Chatbot use versus optimism about AI
`ai-05-use-vs-outlook` · Report Figure 18 · Data: `../data/ai-05-use-vs-outlook.csv`

**Alt text:** Left: 49% of U.S. adults have ever used an AI chatbot. Right: a 100% bar of the expected effect of AI on society over 20 years: 16% positive, 31% equally positive and negative, 40% negative, remainder not sure.

**Source:** Pew Research Center (2026)

### AI use and pessimism by age
`ai-09-use-and-pessimism-by-age` · Report Figure 19 · Data: `../data/ai-09-use-and-pessimism-by-age.csv`

**Alt text:** Dot plot by age group. Ever use AI chatbots / expect a negative impact on society: ages 18–29, 66% / 48%; 30–49, 61% / 39%; 50–64, 42% / 38%; 65 and older, 23% / 35%.

**Source:** Pew Research Center (2026)

### UK undergraduate AI use, 2024–2026
`ai-08-student-ai-use` · Report Figure 22 · Data: `../data/ai-08-student-ai-use.csv`

**Alt text:** Column chart of the share of full-time UK undergraduates using AI tools: 66% in 2024, 92% in 2025, 95% in 2026.

**Source:** HEPI / Kortext (2024–2026)

### Public concerns about AI
`ai-04-public-concerns` · Report Figure 20 · Data: `../data/ai-04-public-concerns.csv`

**Alt text:** Horizontal bar chart of U.S. adults: 71% say AI will make personal information less secure; 67% have little or no confidence the government will regulate AI well; 63% say AI is advancing too quickly; 59% have little or no confidence companies will develop AI responsibly.

**Source:** Pew Research Center (2026)

### Why some U.S. adults don't use AI chatbots
`ai-03-why-people-abstain` · Report Figure 21 · Data: `../data/ai-03-why-people-abstain.csv`

**Alt text:** Stacked bar chart among U.S. adults who don't use AI chatbots. Not interested: 60% major reason, 83% major or minor. Concerned about personal information: 54% major, 79% total. Don't trust the accuracy: 45% major, 76% total. Don't know how to use them: 29% major, 55% total. Worried what others would think: 3% major, 14% total.

**Source:** Pew Research Center (2026)

## Why digital autonomy matters
Folder: `02-why-autonomy-matters/`

### Grindr data case timeline
`risk-02-grindr-data-timeline` · Report Figure 1 · Data: `../data/risk-02-grindr-data-timeline.csv`

**Alt text:** Vertical timeline: 2018, researchers find HIV status shared with two app vendors; Jan 2020, Norwegian Consumer Council complains about Grindr and five ad-tech firms; Dec 2021, Norway fines Grindr NOK 65 million; 2023–2025, appeals board, district court and Court of Appeal uphold the fine; Sep 2026, UK group claim settled for £26 million with no admission of liability; Oct 2026, Norway fines Xandr NOK 92 million over the same data flows.

**Source:** Datatilsynet; Forbrukerrådet; Grindr 8-K

### FTC location-data orders and LGBTQ+ places
`risk-03-ftc-location-orders` · Report Figure 2 · Data: `../data/risk-03-ftc-location-orders.csv`

**Alt text:** Table of FTC location-data broker orders: X-Mode/Outlogic (final Apr 2024) names LGBTQ+-serving places; InMarket (May 2024) does not but bans selling any precise location data; Gravy Analytics/Venntel (Jan 2025) yes, in a separate section; Mobilewalla (Jan 2025) yes; Kochava (Jun 2026) no, narrower sensitive-location list.

**Source:** FTC (2024–2026)

### Human Rights Watch digital targeting cases
`risk-04-hrw-digital-targeting` · Report Figure 3 · Data: `../data/risk-04-hrw-digital-targeting.csv`

**Alt text:** Four stat tiles of documented cases in five MENA countries: 20 online entrapment cases; 45 arbitrary arrests involving 40 people; 17 extortion cases; 26 harassment cases including doxxing and outing.

**Source:** Human Rights Watch (2023)

### GLAAD Social Media Safety Index 2025–2026
`risk-01-glaad-safety-scores` · Report Figure 4 · Data: `../data/risk-01-glaad-safety-scores.csv`

**Alt text:** Dot plot of GLAAD policy scores out of 100, 2025 to 2026: TikTok 56 to 56; Instagram 45 to 41; Facebook 45 to 40; Threads 40 to 39; YouTube 41 to 30; X 30 to 29.

**Source:** GLAAD SMSI 2025, 2026

### Re-identification from three facts
`qa-09-three-facts-identify-you` · Report Figure 5 · Data: `../data/qa-09-three-facts-identify-you.csv`

**Alt text:** ZIP code plus gender plus date of birth: 87% of the U.S. population likely unique using 1990 Census data (Sweeney 2000); 63% in a re-check using 2000 Census data (Golle 2006).

**Source:** Sweeney (2000); Golle (2006)

### Six forces behind software popularity
`dg-04-why-popular-isnt-best-fit` · Report Figure 7

**Alt text:** Six cards with audience questions: Defaults (was it preinstalled or picked for you?), Network effects (is it only useful because friends use it?), Switching costs (can you export your data?), Bundling (did it come with school, work or your device?), Friction (is accepting easier than refusing?), Compatibility (will collaborators open your files?).

**Source:** Workshop framework

### Defaults are paid for
`rh-01-defaults-are-paid-for` · Report Figure 8 · Data: `../data/rh-01-defaults-are-paid-for.csv`

**Alt text:** Three stat tiles: Google paid $26.3 billion in 2021 to be the default search engine; $20 billion went to Apple in 2022; the court found users rarely switch defaults and many don't know a default exists.

**Source:** U.S. v. Google (D.D.C.)

## Queer AI ethics
Folder: `03-queer-ai-ethics/`

### How gender-recognition research modeled gender
`qa-06-misgendering-machines` · Report Figure 9 · Data: `../data/qa-06-misgendering-machines.csv`

**Alt text:** Three stat cards from a review of 58 automatic gender recognition papers: 94.8% treated gender as binary, 72.4% as immutable, 60.3% as physiological.

**Source:** Keyes (2018), CSCW

### Gender Shades error rates
`qa-08-gender-shades` · Report Figure 10 · Data: `../data/qa-08-gender-shades.csv`

**Alt text:** Two bars: maximum error rate 34.7% for darker-skinned women versus 0.8% for lighter-skinned men across three commercial gender classifiers tested in 2017.

**Source:** Buolamwini & Gebru (2018)

### Moderation AI and drag queens' tweets
`qa-07-moderation-drag-queens` · Report Figure 12 · Data: `../data/qa-07-moderation-drag-queens.csv`

**Alt text:** Range chart of average toxicity scores per Twitter account from Google's Perspective API in 2019: 80 drag queens ranged from 16.68% to 37.81%; four white nationalist figures from 21.30% to 28.87%; Donald Trump 21.84%.

**Source:** InternetLab (2019); Dias Oliva et al. (2021)

### Pronoun mentions in English Wikipedia
`qa-05-wikipedia-pronouns` · Report Figure 11 · Data: `../data/qa-05-wikipedia-pronouns.csv`

**Alt text:** Log-scale bar chart of pronoun mentions in English Wikipedia (March 2021): he over 15 million, they 4.9 million (mostly plural), she 4.8 million, ze 7,400, xe 4,500, ey 2,900.

**Source:** Dev et al. (2021), EMNLP

### Queer in AI 2021 community survey
`qa-01-queer-in-ai-survey` · Report Figure 16 · Data: `../data/qa-01-queer-in-ai-survey.csv`

**Alt text:** Left: 85% of respondents report a lack of role models and 80% a lack of community. Right: bar chart of discrimination or harassment experiences: targeted by innuendo or jokes 29%, deliberately ignored or excluded 27%, singled out as the resident authority 27%, target of derogatory comments 25%, felt intimidated or bullied 20%, feared for physical safety 16%, received unsolicited physical contact 15%. n = 142.

**Source:** Queer in AI (2021 survey, reported in Rebuilding Trust)

### Scoping review funnel: chatbots for LGBTQ+ people
`qa-02-queer-chatbot-evidence-funnel` · Report Figure 13 · Data: `../data/qa-02-queer-chatbot-evidence-funnel.csv`

**Alt text:** Funnel on a log scale: 1,390 records found, 1,181 screened, 21 read in full, 9 studies included, covering 7 distinct apps. Side panel: the apps addressed HIV prevention and PrEP navigation, HIV status disclosure, support for rural LGBTQ+ youth, crisis-counselor training, and a community art project; mostly small samples and short trials.

**Source:** Bragazzi et al. (2023), JMIR

### LGBTQ+ youth outlook on generative AI
`qa-03-lgbtq-youth-ai-outlook` · Report Figure 14 · Data: `../data/qa-03-lgbtq-youth-ai-outlook.csv`

**Alt text:** Paired bars, LGBTQ+ vs cisgender and straight 14–22-year-olds: expect a mostly negative impact 28% vs 17%; expect a mostly positive impact 9% vs 18%; among never-users, avoid it over inaccuracy and bias 34% vs 14%.

**Source:** Hopelab / Common Sense Media / Center for Digital Thriving (2024)

### LGBTQ+ adults' concerns about AI
`qa-04-lgbtq-adults-ai-concerns` · Report Figure 15 · Data: `../data/qa-04-lgbtq-adults-ai-concerns.csv`

**Alt text:** Horizontal bars, LGBTQ+ U.S. adults somewhat or very concerned: spreading misinformation 73%, replacing human oversight in safety systems 73%, privacy risks that could expose LGBTQ+ identities 72%, bias in content moderation 71%, bias in algorithms 68%.

**Source:** LGBT Tech / Data for Progress (2025)

## Software audit
Folder: `04-software-audit/`

### Software audit matrix
`dg-01-audit-matrix` · Report Figure 6

**Alt text:** Two-by-two grid. Horizontal axis: could I leave? (easily to hard). Vertical axis: who controls this data? (me to a company). Top-left 'Rented': a company holds it but you could export and leave. Top-right 'Locked in' (highlighted): a company holds it and leaving is hard; start swaps here. Bottom-left 'Yours': on your device in open formats. Bottom-right 'Stuck format': on your device but only one app can read it.

**Source:** Workshop framework (interpretation)

### Seven privacy questions for AI services
`dg-03-seven-privacy-questions` · Report Figure 33

**Alt text:** Seven cards: 1 Training (are my chats used to improve models?, highlighted), 2 Processing (where does the model run?), 3 Retention (what is kept and for how long?), 4 Human access (can reviewers or staff read it?), 5 Connected services (what do search, plugins and sync send out?), 6 Deletion (what does delete really remove?), 7 Authorization (who else can retrieve my files?).

**Source:** Workshop framework

## Alternatives and local AI
Folder: `05-alternatives-and-local-ai/`

### Start-here everyday open source swaps
`sw-01-start-here-everyday` · Report Figure 36 · Data: `../data/sw-01-start-here-everyday.csv`

**Alt text:** Table: ChatGPT app to Jan (Apache-2.0); ChatGPT on phone to PocketPal AI (MIT); WhatsApp or iMessage to Signal (AGPL-3.0, needs phone number); without a phone number, SimpleX Chat (AGPL-3.0); Chrome to Firefox (MPL-2.0, telemetry on by default); LastPass to Bitwarden (GPL-3.0 apps); Microsoft Office to LibreOffice (MPL-2.0); Notion or OneNote to Joplin (AGPL-3.0).

**Source:** Project sites (Oct 2026)

### Start-here creative open source swaps
`sw-02-start-here-creative` · Report Figure 37 · Data: `../data/sw-02-start-here-creative.csv`

**Alt text:** Table: Procreate to Krita (GPL-3.0, no iPad); Photoshop photo editing to GIMP 3.2 (GPL-3.0+); Illustrator to Inkscape; Premiere or CapCut to Kdenlive (GPL-3.0); Maya to Blender (Apple Silicon Macs only); Figma to Penpot (MPL-2.0, browser); Audition to Audacity 4 (GPL-3.0); GitHub for open projects to Codeberg.

**Source:** Project sites (Oct 2026)

### Free isn't open source
`sw-03-free-isnt-open-source` · Report Figure 38 · Data: `../data/sw-03-free-isnt-open-source.csv`

**Alt text:** Table of tools that look open but aren't: LM Studio (proprietary), Msty (proprietary, non-commercial free tier), Obsidian (closed source, free), Anytype (source-available), Open WebUI v0.6.6+ (custom license with branding clause), Llama and Muse Spark Open (custom model licenses).

**Source:** Project license pages (Oct 2026)

### Three layers of an AI app
`dg-02-ai-three-layers` · Report Figure 29

**Alt text:** Three stacked cards. 1: the app you click (interface and runtime): is its code open source, does it send telemetry? 2: the model (weights): what does the weight license allow, is training-data information published? 3: connected services (cloud models, web search, plugins, sync): what leaves your device and under whose privacy policy?

**Source:** Workshop framework; OSI OSAID 1.0

### Where your prompt goes: cloud vs local AI
`dg-05-local-vs-cloud` · Report Figure 35

**Alt text:** Two flows. Cloud chatbot: your device, then the internet (encrypted in transit), then the provider's servers where the model runs, subject to retention, human review, training and legal requests under the provider's policy. Local AI app: the model runs on your device, but chat history, logs, backups and sync, and plugins or web search can still store or send data.

**Source:** Workshop framework

### Four levels of openness in AI models
`om-03-how-open-is-open` · Report Figure 28

**Alt text:** Four columns. Closed (use only through the company's app or API; e.g. ChatGPT, Gemini, Claude): none of weights, open license, training code or data information. Open weights with custom license (e.g. Llama 4, Gemma 3, Muse Spark Open): weights only. Open weights with standard license (Apache-2.0 or MIT; e.g. Gemma 4, Qwen3, Mistral Small 4, DeepSeek, gpt-oss): weights and open license. Open source AI per OSI (e.g. OLMo, Pythia): weights, open license, training code and training-data information.

**Source:** OSI OSAID 1.0; model cards

### Open-weight model license register
`om-05-model-license-register` · Report Figure 30 · Data: `../data/om-05-model-license-register.csv`

**Alt text:** Table of open-weight model families: Llama 4 (Llama 4 Community License; 700M-user cap, attribution, EU limit on multimodal; no ../data/code); Muse Spark Open (Muse Model License; deal for >$20M-revenue API resellers); Gemma 4 (Apache-2.0); Qwen3/Qwen3.8 (Apache-2.0, largest 3.8 models custom); Mistral Small 4 and Large 3 (Apache-2.0; Medium 3.5 Modified MIT with revenue cap); DeepSeek V4/R1 (MIT); gpt-oss (Apache-2.0 plus usage policy); Olmo 3/3.1 (Apache-2.0, releases data, code and checkpoints).

**Source:** Model cards (Oct 2026)

### Local model sizes vs laptop memory
`om-04-what-fits-on-a-laptop` · Report Figure 32 · Data: `../data/om-04-what-fits-on-a-laptop.csv`

**Alt text:** Horizontal bars of 4-bit model download sizes with reference lines at 8 GB and 16 GB of RAM: Llama 3.2 3B 2.0 GB; Qwen3 4B 2.5 GB; Phi-4-mini 2.5 GB; Gemma 3 4B 3.4 GB; Llama 3.1 8B 4.9 GB; Qwen3 8B 5.2 GB; Qwen3 14B 9.3 GB; gpt-oss 20B 14 GB; Gemma 3 27B 17 GB; Qwen3 30B MoE 19 GB.

**Source:** Ollama library (2026)

### Open vs closed model performance gap
`om-01-open-vs-closed-gap` · Report Figure 31 · Data: `../data/om-01-open-vs-closed-gap.csv`

**Alt text:** Dot chart of the gap between the top closed and top open model on Chatbot Arena: 8.0% in Jan 2024, 0.5% in Aug 2024, 1.7% in Feb 2025, 3.3% in Mar 2026.

**Source:** Stanford AI Index 2025, 2026

### Consumer AI chatbot privacy matrix
`pv-01-chatbot-privacy-matrix` · Report Figure 34 · Data: `../data/pv-01-chatbot-privacy-matrix.csv`

**Alt text:** Table for personal accounts. Gemini: trains by default unless Keep Activity is off; temporary chats kept up to 72 hours; human-reviewed chats kept up to 3 years; not used for ads. ChatGPT: trains by default unless 'Improve the model' is off; temporary chats up to 30 days; safety review; ads on Free and Go plans can use past chats with personalization on. Claude: user chooses; if on, data kept up to 5 years; incognito not used for training; flagged chats reviewed; no ads. Copilot new app: not used to train foundation models; retention not stated; personalized ads can use chat history. Meta AI: trains on interactions; retention not published; chats used for ads since Dec 16, 2025 excluding seven sensitive topics.

**Source:** Company policies (Oct 2026)

### How developers trust AI output
`ai-10-developer-trust` · Report Figure 25 · Data: `../data/ai-10-developer-trust.csv`

**Alt text:** Horizontal bars: I trust it when I can easily verify the output 48.0%; for many tasks but not important decisions 16.3%; for low-risk tasks only 16.3%; do not trust it for most work tasks 12.3%; for many tasks including important decisions 6.6%.

**Source:** Stack Overflow Developer Survey 2026

### Measured productivity effects of AI across studies
`ai-11-measured-productivity-effects` · Report Figure 23 · Data: `../data/ai-11-measured-productivity-effects.csv`

**Alt text:** Dot chart of effects for the AI group, with right meaning better. Speed: Noy and Zhang 40% less time; Dell'Acqua inside-frontier tasks 25% faster; METR early 2025 19% slower (95% CI 2–39% slower); METR late 2025 returning developers 18% faster but inconclusive. Output: Brynjolfsson +15% issues per hour; Cui +26% pull requests (CI +6 to +46%); Dell'Acqua +12% tasks. Quality: Noy and Zhang +18%; Dell'Acqua outside-frontier task 19% less likely correct; Cui build success −5.5% (not significant). Learning: Bastani −17% exam score after unguarded AI practice; Shen and Tamkin quiz 50% vs 67%.

**Source:** Multiple peer-reviewed and working papers (see report)

### Felt faster, measured slower (METR 2025)
`ai-12-felt-faster-measured-slower` · Report Figure 24 · Data: `../data/ai-12-felt-faster-measured-slower.csv`

**Alt text:** Diverging bars of change in task time with AI for 16 experienced open-source developers in early 2025: expected beforehand 24% faster; felt afterward 20% faster; measured 19% slower (95% interval 2% to 39% slower).

**Source:** METR (2025, 2026)

### Errors in AI assistants' news answers
`ai-13-ai-news-answers-errors` · Report Figure 27 · Data: `../data/ai-13-ai-news-answers-errors.csv`

**Alt text:** Left: 45% of AI assistant answers to news questions had at least one significant issue, 31% had significant sourcing problems and 20% significant accuracy problems. Right: share with a significant issue by assistant: Gemini 76%, Copilot 37%, ChatGPT 36%, Perplexity 30%.

**Source:** EBU & BBC (2025)

### Verified isn't the same as meaningful
`ai-14-verified-isnt-meaningful` · Report Figure 26 · Data: `../data/ai-14-verified-isnt-meaningful.csv`

**Alt text:** Funnel on a log scale: 700 open Erdős problems attempted by an AI agent; 212 answers its own verifier marked correct; 63 judged technically correct by experts; 13 judged meaningfully correct.

**Source:** Feng et al. (2026), arXiv:2601.22401

## Vetting OSS and GitHub
Folder: `06-vetting-and-github/`

### Seven checks before installing open source software
`oss-06-vet-before-you-install` · Report Figure 39

**Alt text:** Seven cards: 1 Identity (does the official site link to this repo?), 2 License (is there an open source LICENSE file?), 3 Maintenance (recent releases, real replies to issues?), 4 Distribution (official site or app store), 5 Security (security policy and advisories?), 6 People (more than one or two active maintainers?), 7 Fit (platforms, accessibility, data export). Weak evidence on its own: stars, download counts, and free in the name.

**Source:** Workshop checklist; OpenSSF; CHAOSS

### Popularity signals can be faked or flooded
`oss-03-popularity-signals-can-lie` · Report Figure 40 · Data: `../data/oss-03-popularity-signals-can-lie.csv`

**Alt text:** Three stat tiles: 6 million suspected fake GitHub stars (about 26,000 repos before cleanup, 18,617 after); 1 in 6 popular repos ran fake-star campaigns at the July 2024 peak; under 5% of curl's 2025 bug reports were real, down from over 15%, and the bounty ended January 31, 2026.

**Source:** He et al. (ICSE 2026); Stenberg (2026)

### Maintainer concentration in widely used packages
`oss-02-few-maintainers` · Report Figure 41 · Data: `../data/oss-02-few-maintainers.csv`

**Alt text:** Cumulative bars: among top non-npm packages, 17% had one developer writing over 80% of 2023 commits; 40% had two or fewer; 64% four or fewer; 81% ten or fewer.

**Source:** Census III (2024)

### Open source license changes, 2021–2025
`oss-04-licenses-change` · Report Figure 42 · Data: `../data/oss-04-licenses-change.csv`

**Alt text:** Timeline: Jan 2021 Elasticsearch Apache to SSPL/Elastic License (OpenSearch fork); Aug 2023 Terraform MPL to Business Source License (OpenTofu fork); Mar 2024 Redis BSD to RSAL/SSPL (Valkey fork); Aug 2024 Elasticsearch adds AGPL; Oct 2024 Bitwarden client pulled in a proprietary SDK, fixed in about a week; Apr 2025 Open WebUI moves to a custom license with a branding clause; May 2025 Redis 8 adds AGPL; May 2025 Jan moves from AGPL to Apache-2.0.

**Source:** Project announcements

### Code hosts and AI training
`oss-05-where-your-code-trains-ai` · Report Figure 43 · Data: `../data/oss-05-where-your-code-trains-ai.csv`

**Alt text:** Table of code-hosting sites. GitHub: terms grant GitHub and Microsoft the right to train AI on your content; the opt-out doesn't cover public repos; Copilot interactions are used for training unless you opt out since April 24, 2026; Microsoft subsidiary. Codeberg: pledges never to train on users' code, blocks AI crawlers; German non-profit. SourceHut: terms forbid collecting data to train ML models; small paid company. GitLab.com: public-content training not addressed; Duo inputs and outputs not used to train; open-core public company.

**Source:** GitHub ToS (2026); Codeberg (2026); SourceHut; GitLab

## Discovery tool
Folder: `07-discovery-tool/`

### Discovery tool criteria mapped to standards
`oss-07-discovery-tool-criteria` · Report Figure 44 · Data: `../data/oss-07-discovery-tool-criteria.csv`

**Alt text:** Table mapping the presenter's discovery-tool criteria to existing measures and cautions: commits and active developers to CHAOSS Contributor Absence Factor and Scorecard Contributors; license to Scorecard License and SPDX; releases and issues to Scorecard Maintained and CHAOSS metrics; organization backing to foundation membership; hidden proprietary parts to dependency license scans; AI-generated commits has no standard yet; AI privacy to the seven privacy questions.

**Source:** OpenSSF; CHAOSS; presenter's notes
