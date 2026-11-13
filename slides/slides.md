---
theme: default
colorSchema: light
title: Every App Is an Argument
fonts:
  sans: Recursive
  mono: Recursive
  provider: none
transition: fade
layout: cover
class: cover-slide
---

# Every app is an argument

A practical framework for judging software, open source, and AI

<p class="byline">Will Mitchell, oSTEM 2026</p>

<!--
**[Before start] Cover**
- v2 of the deck (Oct 23). The original is untouched in the `slides/` folder.
- Swap in your registered session title if it's different. The speaker kit asks you to follow the posted description.
- As people sit down, ask them to get out paper or a notes app for the audit. No account or install needed.
- Content note, said out loud before starting (the speaker kit asks for one): today touches on surveillance, outing risk, and bias in AI. Step out anytime; nobody has to share anything personal.
-->

---
layout: statement
---

# Hands up if you own a <span class="g">smart TV</span>.

<v-click>

<p class="muted big">Keep your hand up if you've turned off its viewing-data setting.</p>

</v-click>

<!--
**[0:00–0:45] Opening question: show of hands**
- [Hands] Expect most of the room.
- [Click] Expect most hands to go down.
-->

---
layout: center
---

## Many smart TVs identify what's on your <span class="g">screen</span>

<p class="muted">The feature is called ACR: automatic content recognition.</p>

<p class="src">Texas v. Samsung, Sony, LG, Hisense, TCL (filed Dec 15, 2025); The Record</p>

<!--
**[0:45–2:00] The TV case**
- ACR matches what's on screen so the data can be used for ads and analytics. It reads the screen, not your internet traffic.
- Dec 15, 2025: Texas sued five TV makers. The suits allege ACR collects viewing data without informed consent.
  - They say it can capture content from laptops plugged in over HDMI, from AirPlay/Cast streams, and from doorbell camera feeds.
  - They say the data can be combined to infer race, sex, and religious or political beliefs.
- These are allegations, not court findings. Say "Texas alleged."
- Samsung settled Feb 26, 2026. LG's agreement was announced May 11, 2026: a pop-up disclosure, no collection "without their informed consent," and "a clear and simple way to opt out" (Texas AG). A secondary source says it still needs court approval. Sony, Hisense and TCL cases continue.
-->

---
layout: statement
---

# Who turned that setting on: you, or the <span class="g">manufacturer</span>?

<!--
**[2:00–2:30] Defaults**
- Most people never see the setting.
- A default is a decision someone else made for you. Hold that thought: we come back to this TV at the end of Part 1.
-->

---
layout: fact
---

# 1969

Your TV's code is secret. The notes that designed the internet are public, starting with the first.

<p class="src">RFC 1, "Host Software," S. Crocker, 7 April 1969: the first ARPANET Request for Comments; rfc-editor.org</p>

<!--
**[2:30–3:15] The hopeful turn: software keeps public records**
- A TV's firmware is closed. Much of the internet was built in the open: its standards (RFCs), mailing-list discussions, and code histories are public. The internet's development is documented on the internet.
- RFC 1 was written for ARPANET, the network before the internet, so don't call it "the first internet document."
- Open source works the same way. Signal's Android app has about 21,000 public commits (21,164 when counted Oct 21).
- That public record is what makes checking software possible. The rest of the talk is about how to read it.
-->

---
layout: center
class: about
---

## Hi, I'm Will <span class="muted">(he/they)</span>

- Queer CS + math student, Montana State
- Formal methods: <span class="g">proving</span> software does what it claims
- oSTEM @ MSU president, open source maintainer

<v-click>

<p class="muted">Fun fact: I was a voice actor on PAW Patrol.</p>

</v-click>

<!--
**[3:15–3:45] About me**
- One line each; the next slide shows the details.
- OERCA internship: built an LLM knowledge base. I build with AI, so this isn't an anti-AI talk.
- TA for 35+ students a semester. oSTEM MSU has funded 12-student cohorts to this conference for three years.
- [Click] Fun fact. Quick laugh, then move on.
-->

---
layout: center
class: logos-slide
---

## My research and open source

<div class="logos four">
  <img src="/personal/forge-lab.png" alt="FORGE: Foundations of Reasoning and Generative Engineering. Our research helps people write software that executes as intended. Directed by Charlie Murphy, Gianforte School of Computing, Montana State University." />
  <img src="/personal/hypermedia-group.png" alt="The HyperMedia Research Group at cs.montana.edu" />
  <img src="/personal/open-source-msu.png" alt="Open Source @ MSU: the Open Source Group at the Gianforte School of Computing, Montana State University, with the MSU Bobcat logo." />
  <img src="/personal/pika-orm.png" alt="PikaORM: a simple ORM for Java, designed for the Montana State University Databases class. It follows the ActiveRecord pattern and allows dropping to raw SQL." />
</div>

<!--
**[3:45–4:30] Research and open source**
- FORGE Lab (Dr. Charlie Murphy): formal methods, helping people write software that runs as intended. I work with Lean 4 and SMT solvers (cvc5) and am building an open source Rust symbolic reasoning kit.
- Hypermedia Research Group: co-authored a paper on HTMX and AI agents via MCP (under review, ACM Hypertext).
- Open Source Group at MSU's Gianforte School of Computing. PikaORM: a Java ORM I co-built with Carson Gross (creator of HTMX) for MSU's Databases class, on Maven Central. It comes back near the end, when my own site gives it a D.
- Why it matters today: my research is about checking that software does what it claims, which is what this workshop teaches at everyday scale.
-->

---
layout: statement
---

# That was my <span class="g">ethos</span>: why you should believe me.

## Don't take it on faith. Every number today has its source on the slide.

<!--
**[4:30–5:00] Disclosures, framed as the first use of the framework**
- In rhetoric, what I just did is ethos: giving you reasons to trust the speaker. You'll use that word all hour.
- Disclosures: I use AI tools, and I built the site I'll show you with AI help (Claude Code). That's a current debate in open source, and it comes up later.
- I'm not a lawyer. I'll report legal cases, not argue them.
- The full research report is available if anyone wants the sources.
-->

---
layout: center
---

## Techno-queer

<p class="big">A rhetorically aware user of technology whose intentional choices weigh privacy, inclusion, safety, and community.</p>

<p class="muted">In practice: Queering the Map, Queer in AI</p>

<p class="src">The term has an academic history: Edmond Y. Chang, <em>Technoqueer</em> (University of Washington, 2012)</p>

<!--
**[5:00–6:00] Techno-queer (working definition, Oct 23; still to refine)**
- Moved up from the end of Part 1 (v2): this is the reason for the framework, so it comes before it.
- Your wording: "A rhetorically aware user of technology, that folds into its intentional decisions, conscious metrics about privacy, inclusion, safety and community." The slide has a tightened version.
- "Rhetorically aware" is what the four questions build. "Conscious metrics" is what OSS Fidelity makes concrete at the end.
- Prior use: Edmond Y. Chang's 2012 dissertation, *Technoqueer: Re/Con/Figuring Posthuman Narratives*, uses the term for queer readings of technology against a "technonormative matrix." Mine is practical: how we pick and build tools. Credit him if anyone asks.
- Examples of queer-built infrastructure:
  - Queering the Map (launched 2017): over 500,000 anonymous queer stories pinned to places by June 2023.
  - Queer in AI: 1,000+ members; runs workshops at major AI conferences; partners with oSTEM on grad-application aid.
-->

---
layout: center
---

## Documented risks for queer people

- App use that reveals orientation
- Location data near LGBTQ+ places
- AI that misreads queer people

<!--
**[6:00–6:30] The queer-specific stakes**
- The research shows specific, documented ways data harms queer people. It doesn't show that every app is dangerous.
  - App use revealing orientation: Grindr (next two slides).
  - Location data: three FTC orders (Apr 2024 to Jan 2025) specifically protected location data tied to LGBTQ+-serving places such as bars and service organizations. Law-firm analyses say the 2026 Kochava order's list doesn't name them (secondary). Report the difference factually; don't speculate on why (oSTEM 501(c)(3) guidance). Table in backup.
  - AI misreading queer people: Part 2.
-->

---
layout: statement
---

# Norway's regulator ruled that using Grindr is itself data that reveals sexual <span class="g">orientation</span>.

<!--
**[6:30–7:00] Being on an app is sensitive**
- The issue wasn't messages or photos. It was the fact that someone uses the app.
- Datatilsynet treated it as special-category data under GDPR Article 9.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/risk-02-grindr-data-timeline.png" alt="Vertical timeline: 2018, researchers find HIV status shared with two app vendors; Jan 2020, Norwegian Consumer Council complains about Grindr and five ad-tech firms; Dec 2021, Norway fines Grindr NOK 65 million; 2023–2025, appeals board, district court and Court of Appeal uphold the fine; Sep 2026, UK group claim settled for £26 million with no admission of liability; Oct 2026, Norway fines Xandr NOK 92 million over the same data flows." />

<!--
**[7:00–7:45] Grindr timeline**
- Data shared with ad partners: GPS location, IP address, ad ID, age, gender, and the fact of using Grindr.
- NOK 65M fine (Dec 2021), upheld by an appeals board and two courts, most recently Oct 21, 2025. Secondary sources say it's now final and Grindr paid in Feb 2026; say "upheld" unless you've confirmed with Datatilsynet.
- Oct 2026: Norway fined Xandr (an ad-tech company Microsoft now owns) NOK 92M over the same data flows. Not final; Xandr can appeal.
- UK group claim settled Sep 2026 for £26M, with no admission of liability.
- We come back to how this case started under logos.
-->

---
layout: statement
---

# More software options than ever. Less <span class="g">control</span> over what we see.

<!--
**[7:45–8:15] The problem, in one line (from your outline)**
- This is framing, not a statistic. If someone asks: Hugging Face hosted about 2.96 million public model repositories by mid-2026, and a federal court found that users "rarely" change defaults (Part 1).
- Rhetoric is how you take some control back: understanding how these systems persuade you, and where to look for alternatives.
-->

---
layout: statement
---

# Every app makes a case for why you should use it.

<v-click>

<p class="muted big">Being techno-queer means answering that case on purpose.</p>

</v-click>

<!--
**[8:15–8:45] Thesis**
- Software persuades through defaults, popularity, and claims like "free," "private," and "open."
- Credit out loud: the title borrows from *Everything's an Argument* (Lunsford & Ruszkiewicz), the first-year writing textbook many of you used. The idea that software argues through what it does is Ian Bogost's "procedural rhetoric" (*Persuasive Games*, 2007).
- What's new today: you turn it around and audit the app's argument.
- [Click] The goal isn't to switch everything. It's to evaluate a tool and decide.
-->

---
layout: center
---

## The goal: rhetorical <span class="g">self-efficacy</span>

<p class="big">Confidence that you can judge a tool's case for itself.</p>

<v-click>

<p class="muted">Practice builds it, so a third of today is hands-on.</p>

</v-click>

<p class="src">Self-efficacy: Bandura (1977), Psychological Review 84(2)</p>

<!--
**[8:45–9:15] What you'll leave with**
- Bandura (1977): self-efficacy is confidence that you can do a specific task. Doing the task yourself ("mastery experiences") is an especially influential source. Check the exact wording in the paper before quoting it.
- "Rhetorical self-efficacy" is my term: confidence that you can judge a tool's case.
- [Click] You'll practice on your own apps, an AI model, a GitHub project, and my site.
- Pew 2026: among U.S. adults who don't use AI chatbots, 54% cite concern about personal information as a major reason. Only 29% say they don't know how. Most hesitation is about trust, not skill.
-->

---
layout: center
---

## Today

1. Four questions for any software
2. Use them on AI and your own apps
3. Use them on open source, and on my site

<!--
**[9:15–9:30] Roadmap**
- About a third of the hour is hands-on, with two short demos: a local AI model and my site.
- Paper or notes app ready.
-->

---
layout: section
transition: slide-up
---

# Part 1

## Four questions for any software

<!--
**[9:30] Part 1: the framework (~8 min)**
-->

---
layout: center
class: framework framework-lg
---

<div class="grid4">
  <div class="card ap-pathos"><span class="label">Pathos</span><span class="q">Why do I want it?</span><span class="x" v-click="1">Exploit: wants get engineered</span></div>
  <div class="card ap-ethos"><span class="label">Ethos</span><span class="q">Who's behind it?</span><span class="x" v-click="1">Exploit: trust gets faked</span></div>
  <div class="card ap-logos"><span class="label">Logos</span><span class="q">What can I check?</span><span class="x" v-click="1">Exploit: evidence gets gamed</span></div>
  <div class="card ap-kairos"><span class="label">Kairos</span><span class="q">Why now? Is it still true?</span><span class="x" v-click="1">Exploit: the ask is timed; facts expire</span></div>
</div>

<p class="framework-note">Three appeals from Aristotle, plus kairos from the sophists</p>

<!--
**[9:30–10:30] The framework**
- Aristotle's *Rhetoric* names three appeals (ethos, pathos, logos) and insists there are no others. Kairos, "the right moment," comes from the sophists (Gorgias, Isocrates). Don't call these "Aristotle's four."
- Each one becomes a question you ask back at the app:
  - Pathos: convenience, belonging, friends already using it.
  - Ethos: who makes it, who maintains it, who pays for it, and who else vouches for it.
  - Logos: license file, privacy terms, whether you can export your data.
  - Kairos: when did it ask for your yes, and is what you read still current?
- [Click] Each appeal can be exploited, and each example that follows shows one:
  - Pathos: wants get engineered (defaults, "free").
  - Ethos: trust gets faked (xz).
  - Logos: evidence gets gamed (a checked box that isn't consent).
  - Kairos: the ask is timed for when you won't read it, and facts expire (licenses).
- Pathos isn't bad. Keeping Instagram because your friends are there is a real reason. The point is to name it.
- This slide comes back at the end.
-->

---
layout: center
---

<div class="appeal ap-pathos">Pathos</div>

## Guess: how much did Google pay in 2021 to be the <span class="g">default</span> search engine?

<!--
**[10:30–11:00] Pathos: wants get engineered**
- First: "Did you choose your web browser, or did it come with your device?" [Hands] Most software arrives by default, in a bundle, or because friends use it.
- Then: [Take 3–4 guesses from the room.] Advance.
-->

---
layout: center
class: graphic
---

<div class="appeal ap-pathos">Pathos</div>

<img src="/graphics-lav/rh-01-defaults-are-paid-for.png" alt="Three stat tiles: Google paid $26.3 billion in 2021 to be the default search engine; $20 billion went to Apple in 2022; the court found users rarely switch defaults and many don't know a default exists." />

<!--
**[11:00–11:45] Default placement costs billions**
- $26.3B in 2021; about $20B to Apple in 2022 (U.S. v. Google).
- The court found that users can switch, but "the market reality is that users rarely do so," and many don't know a default exists.
- Status: final judgment Dec 5, 2025; on appeal. Say "a federal court found."
- Companies pay this much because defaults change behavior. Defaults also borrow ethos: people tend to read a default as a recommendation (McKenzie et al., 2006; pull the paper before quoting it).
- The "six reasons software gets popular" chart is now in backup.
-->

---
layout: center
---

<div class="appeal ap-ethos">Ethos</div>

## xz-utils, 2024

<p class="big">A contributor spent years gaining trust, then hid a <span class="g">backdoor</span> in a release.</p>

<v-click>

<p class="muted">An engineer caught it after noticing SSH using extra CPU.</p>

</v-click>

<p class="src">Tukaani Project; Freund, oss-security (Mar 29, 2024)</p>

<!--
**[11:45–12:30] Ethos: trust gets faked**
- xz is a compression tool included in most Linux systems.
- "Jia Tan" contributed for years (from about 2021), gained trust, then put a backdoor into release tarballs 5.6.0 and 5.6.1.
- In 2022 the original maintainer wrote that long-term mental health issues limited how much he could do, while suspected sock-puppet accounts pushed him to hand over control. Mention this with care: he's a person, not a cautionary tale.
- [Click] Andres Freund found it while investigating unusual CPU use and Valgrind errors in SSH on a test system. Ethos was faked for years; a measurement (logos) caught it.
- Census III: among the top non-npm packages, 40% had one or two people writing over 80% of 2023 commits (chart in backup). Who maintains this, and how many people are there?
-->

---
layout: center
---

<div class="appeal ap-ethos">Ethos</div>

## Ask who else <span class="g">vouches</span> for it

<p class="big">Fact-checkers leave a site to judge it. Students and historians mostly stayed on the page.</p>

<v-click>

<p class="muted">After four online modules, 67 of 87 students checked other sources, up from 3.</p>

</v-click>

<p class="src">Wineburg &amp; McGrew (2019), Teachers College Record; Breakstone et al. (2021), HKS Misinformation Review</p>

<!--
**[12:30–13:15] Ethos, done well: lateral reading**
- Wineburg & McGrew compared 10 historians, 10 professional fact-checkers and 25 Stanford students. Historians and students "often fell victim to easily manipulated features of websites, such as official-looking logos and domain names." Fact-checkers opened new tabs to see what others said about the source. That's called lateral reading.
- [Click] Breakstone et al. (2021): 87 University of North Texas students, four one-hour online modules, no control group. A 2022 district-wide study with a control group also found gains (Wineburg et al., Journal of Educational Psychology).
- For software: does the official site link to this repo? What do security advisories, reviews, or my site say? Don't judge a project only by its own README.
-->

---
layout: center
---

<div class="appeal ap-logos">Logos</div>

## A checked box isn't proof of <span class="g">consent</span>

<p class="big">Norway's regulator and courts found Grindr's consent invalid: you had to accept to use the app.</p>

<v-click>

<p class="muted">The case began when a consumer group traced where the data went.</p>

</v-click>

<p class="src">Borgarting Court of Appeal (Oct 21, 2025), via Datatilsynet; Forbrukerrådet complaint (Jan 14, 2020)</p>

<!--
**[13:15–14:00] Logos: evidence gets gamed**
- Back to Grindr. Users "agreed," but accepting the privacy policy was the price of using the app, so the consent didn't count.
- [Click] The Norwegian Consumer Council traced where Grindr's data went and filed the complaint (Jan 2020). Checking is what changed the outcome.
- Logos question: what can I check? Who receives the data, whether consent was a real choice, whether I can delete it.
-->

---
layout: statement
---

<div class="appeal ap-kairos">Kairos</div>

# When did your TV ask to track what you <span class="g">watch</span>?

<v-click>

<p class="muted big">Texas alleges makers "deceptively guide consumers to activate ACR."</p>

</v-click>

<p class="src">Texas v. Samsung et al. (Dec 2025), as reported by The Record; allegations, not findings</p>

<!--
**[14:00–14:30] Kairos, part 1: why now?**
- [Hands] Who remembers when the TV asked? Most people saw it once, when they first set it up and just wanted to watch.
- [Click] The suits allege the makers "deceptively guide consumers to activate ACR." Allegations, not findings.
- Kairos has two halves: why now (when the ask was timed), and is it still true (next slide).
-->

---
layout: center
class: graphic
---

<div class="appeal ap-kairos">Kairos</div>

<img src="/graphics-lav/oss-04-licenses-change.png" alt="Timeline: Jan 2021 Elasticsearch Apache to SSPL/Elastic License (OpenSearch fork); Aug 2023 Terraform MPL to Business Source License (OpenTofu fork); Mar 2024 Redis BSD to RSAL/SSPL (Valkey fork); Aug 2024 Elasticsearch adds AGPL; Oct 2024 Bitwarden client pulled in a proprietary SDK, fixed in about a week; Apr 2025 Open WebUI moves to a custom license with a branding clause; May 2025 Redis 8 adds AGPL; May 2025 Jan moves from AGPL to Apache-2.0." />

<!--
**[14:30–15:15] Kairos, part 2: is it still true? Licenses change**
- A license or privacy policy you checked last year may not match the current one.
- Terraform changed to a restrictive license (Aug 2023). The community forked it as OpenTofu within six weeks (Linux Foundation, Sep 20, 2023).
- Redis did the same (Mar 2024). The Valkey fork launched 8 days later. Redis later added an open license back (AGPL, May 2025).
- Bitwarden users noticed a proprietary component in the desktop client, and it was fixed in about a week.
- Those forks were possible because the code was open. If a project changes, others can continue it.
- Terms change too: Part 2 has AI privacy terms that changed this year.
-->

---
layout: center
---

## Open source

- The code is public
- The license allows use, changes, and sharing
- Others can <span class="g">fork</span> it if it changes

<v-click>

<p class="muted">xz was open source, too.</p>

</v-click>

<!--
**[15:15–15:45] Definitions**
- Open source: the code is public, and its license allows anyone to use, study, change, and share it.
- License: the legal file that says what you're allowed to do. "Free" in the name isn't a license. Obsidian is free but closed source.
- Fork: a copy of a project that someone else continues.
- [Click] Openness makes checking possible. It doesn't do the checking. Using some proprietary tools is fine.
-->

---
layout: center
---

## Why do we care about <span class="g">open source</span>?

- Ad-funded apps run on your data
- Gemini keeps reviewed chats up to 3 years, deleted or not

<v-click>

<p class="muted big">A product is built to keep you. A commons lets you leave.</p>

</v-click>

<p class="src">Google, Gemini Apps Privacy Hub (updated Oct 19, 2026)</p>

<!--
**[15:45–16:30] Why do we care about open source? Connect it to them**
- This is my argument, not a neutral finding, so say it as one. It's about how software gets paid for, not about candidates or bills, so it stays within oSTEM's 501(c)(3) guidance.
- The business model: most "free" consumer software is paid for by advertising, so its incentive is to keep you and use what you do. Examples already in this talk:
  - Google paid $26.3B in 2021 to be the default search engine.
  - Grindr shared users' data with ad-tech partners (the Norway fine).
  - ChatGPT ads (since Feb 2026) can use past chats when ad personalization is on.
  - Meta uses AI-chat interactions for ads (since Dec 16, 2025).
- Retention: Gemini keeps human-reviewed chats up to 3 years, disconnected from your account, and doesn't delete them when you delete your activity. Claude keeps chats up to 5 years (de-identified) if you allow training. A local model keeps nothing off your device unless you add sync or plugins.
- [Click] Open source works more like a commons. The code is public, much of it runs on your own device, and when a company changes the deal, the community can fork it and leave (OpenTofu, Valkey).
- Honest tradeoffs, so it isn't a purity test:
  - Open source isn't automatically private: an open app can still call a cloud model.
  - Companies build a lot of it (IBM's Granite, Google's Gemma).
  - A commons needs upkeep: many maintainers are unpaid (Tidelift survey, secondary).
- Ask: "Which of your daily apps is a product, and which is a commons?"
-->

---
layout: center
class: framework framework-sm
---

## The TV, <span class="g">four</span> ways

<div class="grid4">
  <div class="card ap-pathos"><span class="label">Pathos</span><span class="lq">Why do I want it?</span><span class="a">It came on by default</span></div>
  <div class="card ap-ethos"><span class="label">Ethos</span><span class="lq">Who's behind it?</span><span class="a">The maker, and the ads the data feeds (alleged)</span></div>
  <div class="card ap-logos"><span class="label">Logos</span><span class="lq">What can I check?</span><span class="a">The setting itself; Texas's complaints</span></div>
  <div class="card ap-kairos"><span class="label">Kairos</span><span class="lq">Why now? Still true?</span><span class="a">Samsung, LG settled in 2026; others still in court</span></div>
</div>

<p class="src">The Record (Dec 2025, Feb 2026); Texas Attorney General (May 11, 2026)</p>

<!--
**[16:30–17:15] Worked example: the four questions on one thing**
- This is the pattern you'll use on your own apps.
- Pathos: it came on by default, and turning it off takes effort.
- Ethos: the maker, and the advertising and analytics the data feeds (alleged).
- Logos: check the setting yourself. LG calls it "Live Plus"; Samsung calls it "Viewing Information Services" (Tom's Guide, Jan 2026). Read the complaints.
- Kairos: asked once, at setup. Samsung settled Feb 26, 2026; LG's agreement was announced May 11, 2026; Sony, Hisense and TCL cases continue.
- Next: we do this together on AI, then you do it on your own apps.
-->

---
layout: section
transition: slide-up
---

# Part 2

## Use them on AI and your own apps

<!--
**[17:15] Part 2: AI, the audit, alternatives, and the local-model demo (~23 min)**
-->

---
layout: statement
---

# Hands up if you used an AI chatbot this <span class="g">week</span>.

<v-click>

<p class="muted big">Keep it up if you fully trust what it tells you.</p>

</v-click>

<!--
**[17:15–17:45] Show of hands**
- [Hands] Probably most of the room.
- [Click] Expect most hands to go down. The next slides show that's common.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/ai-09-use-and-pessimism-by-age.png" alt="Dot plot by age group. Ever use AI chatbots / expect a negative impact on society: ages 18–29, 66% / 48%; 30–49, 61% / 39%; 50–64, 42% / 38%; 65 and older, 23% / 35%." />

<!--
**[17:45–18:30] Use and distrust together**
- Pew (Feb 2026, n = 5,119): adults 18–29 use chatbots the most (66%) and are the most likely to expect a negative impact on society (48%).
- Overall, 49% of U.S. adults have used a chatbot, and 71% say AI will make personal information less secure.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/qa-03-lgbtq-youth-ai-outlook.png" alt="Paired bars, LGBTQ+ vs cisgender and straight 14–22-year-olds: expect a mostly negative impact 28% vs 17%; expect a mostly positive impact 9% vs 18%; among never-users, avoid it over inaccuracy and bias 34% vs 14%." />

<!--
**[18:30–19:00] LGBTQ+ young people are more skeptical (optional)**
- Hopelab / Common Sense / Center for Digital Thriving (survey late 2023): LGBTQ+ 14–22-year-olds were more likely to expect AI to hurt their lives (28% vs 17%).
- Among people who'd never used it, 34% vs 14% cited inaccuracy and bias.
- How often they used AI didn't differ. The skepticism has specific reasons.
-->

---
layout: statement
---

<div class="appeal ap-ethos">Ethos</div>

# AI affects you even if you never use a <span class="g">chatbot</span>.

<!--
**[19:00–19:30] Ethos: who controls the AI that affects you?**
- 60% of U.S. adults read AI summaries at the top of search results (Pew 2026).
- Meta uses AI-chat interactions for ads (since Dec 16, 2025). Sexual orientation is excluded as an ad topic; gender identity isn't on the excluded list.
- A widely used training-data filter removed text mentioning sexual orientations more often than text mentioning race or ethnicity (Dodge et al., 2021).
- GitHub's AI-training terms come up in Part 3.
- Content moderation is also automated (next slide).
-->

---
layout: center
class: graphic
---

<div class="appeal ap-ethos">Ethos</div>

<img src="/graphics-lav/qa-07-moderation-drag-queens.png" alt="Range chart of average toxicity scores per Twitter account from Google's Perspective API in 2019: 80 drag queens ranged from 16.68% to 37.81%; four white nationalist figures from 21.30% to 28.87%; Donald Trump 21.84%." />

<!--
**[19:30–20:15] Moderation AI and queer speech**
- 2019: Google's Perspective API scored 80 drag queens' Twitter accounts (114,204 tweets). Many scored as more "toxic" than white nationalist leaders.
- It couldn't tell in-group humor or reclaimed words from abuse.
- Authors: Dias Oliva, Antonialli & Gomes (some papers misname them).
- Related: Keyes (2018) found 94.8% of 58 gender-recognition papers treated gender as binary (backup slide).
-->

---
layout: statement
---

<div class="appeal ap-logos">Logos</div>

# Thumbs up if you think AI makes experienced developers <span class="g">faster</span>.

<!--
**[20:15–20:30] Logos: thumbs up, down, or sideways**
- [Thumbs] Then advance.
-->

---
layout: center
class: graphic
---

<div class="appeal ap-logos">Logos</div>

<img src="/graphics-lav/ai-12-felt-faster-measured-slower.png" alt="Diverging bars of change in task time with AI for 16 experienced open-source developers in early 2025: expected beforehand 24% faster; felt afterward 20% faster; measured 19% slower (95% interval 2% to 39% slower)." />

<!--
**[20:30–21:30] What the study measured**
- METR (Jul 2025): 16 experienced open-source developers, 246 tasks in their own repos, early-2025 tools, randomized.
- They expected to be 24% faster, felt 20% faster, and were measured 19% slower.
- Say it in the past tense. METR's original page now says these results "no longer reflect the current impact." Its Feb 2026 follow-up suggests speedups but calls its own data "very weak evidence."
- Logos point: how fast something feels isn't a measurement.
-->

---
layout: two-cols
class: contention
---

<div class="appeal ap-logos">Logos</div>

### Benefit

<p class="stat">+26%</p>

<p class="muted">completed pull requests for developers using an AI coding assistant</p>

<p class="src">Cui et al., Management Science (three company experiments)</p>

::right::

### Cost

<p class="stat">&lt;5%</p>

<p class="muted">of bug reports sent to curl in 2025 were valid</p>

<p class="src">Stenberg, "The end of the curl bug-bounty" (Jan 26, 2026)</p>

<!--
**[21:30–22:15] AI made code cheaper to produce, and cheaper to fake**
- Benefit: Cui et al. ran field experiments at Microsoft, Accenture and a Fortune 100 company (4,867 developers). Developers who used the assistant completed 26% more pull requests (roughly +6% to +46%). Build success fell 5.5% (not statistically significant).
- Outside code: customer-support agents resolved 15% more issues per hour on average, about 30% more for the least experienced (Brynjolfsson, Li & Raymond, QJE 2025; the 30% is in the paper's body, not its abstract).
- Cost: curl ended its bug bounty Jan 31, 2026. Valid reports fell from over 15% to under 5% from 2025 as AI-generated reports increased. Sonatype counted 454,600+ new malicious open source packages in 2025.
- With more software being produced, evaluating it becomes a more important skill.
-->

---
layout: center
class: graphic
---

<div class="appeal ap-logos">Logos</div>

<img src="/graphics-lav/ai-10-developer-trust.png" alt="Horizontal bars: I trust it when I can easily verify the output 48.0%; for many tasks but not important decisions 16.3%; for low-risk tasks only 16.3%; do not trust it for most work tasks 12.3%; for many tasks including important decisions 6.6%." />

<!--
**[22:15–23:00] Developers trust output they can check**
- Stack Overflow 2026: the most common answer (48%) was "I trust it when I can easily verify the output." Only 6.6% trust it for important decisions.
- From my research (formal methods): I write proofs in Lean. A proof checker confirms that a proof matches its statement. It doesn't confirm that the statement was the right question.
  - DeepMind's agent on 700 open Erdős problems: its own verifier marked 212 answers correct; experts found 63 correct and 13 meaningful (backup slide).
- From your notes: use AI to find human sources, not to interpret for you.
-->

---
layout: statement
---

<div class="appeal ap-logos">Logos</div>

# I built my site with AI. Then I <span class="g">checked</span> it.

<v-click>

<p class="muted big">A review found a project with no license could still score an A. Now a missing license caps Reliability at F.</p>

</v-click>

<p class="src">OSS Fidelity outside review (Oct 21, 2026) and fix (decision D26)</p>

<!--
**[23:00–23:45] Using AI to build tools that keep you in control**
- Replaces the NVDA reverse-engineering slide. I couldn't find a primary source for it; the closest is a July 2026 social-media debate about using AI to write Linux drivers for simple USB devices, reported secondhand.
- I built OSS Fidelity with Claude Code. An outside review ran the scoring formula on test cases: LLVM with its license removed still got Reliability A and Fidelity A.
- [Click] Now a missing license caps Reliability at F (39), and a source-available license caps it at D.
- That's the point from my notes: AI scales usefully only as far as you verify the output.
- Keep this practical (staying in control, verifying output) rather than political, per oSTEM guidance.
-->

---
layout: center
---

<div class="appeal ap-kairos">Kairos</div>

## AI privacy terms changed this year

- ChatGPT ads: Feb 2026
- New Copilot app: Aug 2026

<p class="muted">Check your current settings.</p>

<p class="src">OpenAI Help Center, "Ads in ChatGPT"; Microsoft Copilot privacy docs (Aug 18, 2026)</p>

<!--
**[23:45–24:30] Kairos applied to AI**
- ChatGPT: ads began as a U.S. test Feb 9, 2026 (Free and Go plans) and now run in 89 countries. With ad personalization on, ads can use past chats and memory.
- Copilot's new app (Aug 18, 2026): chats "aren't used to train foundation models," but personalized ads can use chat history.
- Claude: you choose whether chats are used for training. If on, data is kept up to 5 years de-identified; if off, 30 days.
- The full comparison is on a backup slide. School accounts have different terms.
-->

---
layout: center
---

## Your turn: audit your apps <span class="muted">(4 min)</span>

1. List 5 apps you open daily
2. Place each one on the grid
3. Star one you'd consider <span class="g">leaving</span>

<p class="muted">Paper or phone.</p>

<!--
**[24:30–25:15] Instructions**
- This is the practice part.
- Include an AI tool if you use one.
- Nobody will ask you to share your list.
- The grid stays on screen while you work. [Start a visible 4-minute timer.]
-->

---
layout: center
class: audit-slide
---

## The audit: two of the four questions

<div class="audit">
  <div class="ay"><span class="e">A company</span><span class="t"><span class="ax-lab ap-ethos">Ethos</span> Who controls this data?</span><span class="e">Me</span></div>
  <div class="cells">
    <div class="cell"><b>Rented</b><span>A company holds it, but you could export and leave.</span></div>
    <div class="cell hot"><b>Locked in</b><span>A company holds it and leaving is hard. Start swaps here.</span></div>
    <div class="cell"><b>Yours</b><span>On your device, in open formats. Keep it.</span></div>
    <div class="cell"><b>Stuck format</b><span>On your device, but only one app can read it. Plan an export.</span></div>
  </div>
  <div class="ax"><span class="e">Easily</span><span class="t"><span class="ax-lab ap-kairos">Kairos</span> If the terms change, could I leave?</span><span class="e">Hard</span></div>
</div>

<!--
**[25:15–29:15] Work time: 4 minutes**
- Two of the four questions: ethos (who controls this data?) and kairos (if the terms change tomorrow, could I leave: export it, take my contacts, open my files somewhere else?).
- "Controls" instead of "owns," because most terms grant a company a license to use your content, not ownership.
- Then the star is pathos: why do I still want it?
- Walk the room. Common "Locked in" apps: Instagram, iMessage, Google Docs, ChatGPT history, Notion.
- If someone is stuck: "What happens to your files if this app shuts down tomorrow?"
-->

---
layout: center
class: graphic
---

<div class="appeal ap-logos">Logos</div>

<img src="/graphics-lav/dg-03-seven-privacy-questions.png" alt="Seven cards: 1 Training (are my chats used to improve models?, highlighted), 2 Processing (where does the model run?), 3 Retention (what is kept and for how long?), 4 Human access (can reviewers or staff read it?), 5 Connected services (what do search, plugins and sync send out?), 6 Deletion (what does delete really remove?), 7 Authorization (who else can retrieve my files?)." />

<!--
**[29:15–30:00] For AI apps: what can I check?**
- These seven are the logos questions for an AI app.
- If you listed an AI app, start with question 1: are my chats used for training? Most consumer chatbots do this by default unless you turn it off (Gemini: "Keep Activity"; ChatGPT: "Improve the model for everyone").
- "Not used for training" answers one of seven questions.
- My site's AI privacy page scores all seven for the major chatbots.
-->

---
layout: statement
---

# Tell a neighbor: one app you'd keep and one you'd leave.

## Which question decided it?

<!--
**[30:00–32:00] Pair discussion: 2 minutes**
- Hearing how someone else decided helps people trust their own reasoning.
- Point back to the four questions.
-->

---
layout: center
---

## Did any app land in <span class="g">"Locked in"</span>?

<p class="muted">Which of the four questions put it there?</p>

<!--
**[32:00–33:30] Debrief: hands, then 2–3 volunteers**
- [Hands] Who found at least one Locked-in app?
- Ask 2–3 people: which app, and which question?
- Keeping an app is a valid result. Keeping Instagram because your friends are there is a pathos reason, and now it's a deliberate choice.
-->

---
layout: center
class: picks-slide
---

## Start here: one swap per <span class="g">category</span>

<div class="picks">
  <div class="pick"><span class="label">Messaging</span><b>Signal</b><span class="lic">AGPL-3.0</span><span class="t">Needs a phone number</span></div>
  <div class="pick"><span class="label">Passwords</span><b>Bitwarden</b><span class="lic">GPL-3.0</span><span class="t">You trust its cloud</span></div>
  <div class="pick"><span class="label">Notes</span><b>Joplin</b><span class="lic">AGPL-3.0</span><span class="t">Plainer than Notion</span></div>
  <div class="pick"><span class="label">Art</span><b>Krita</b><span class="lic">GPL-3.0</span><span class="t">No iPad version</span></div>
</div>

<p class="src">Licenses, platforms and releases checked Oct 21, 2026; full tables in backup</p>

<!--
**[33:30–34:45] Alternatives, one per category, each with its tradeoff**
- Keep your starred app in mind.
- Signal: end-to-end encrypted by default (only you and the person you're messaging can read it). It still needs a phone number, which matters if you aren't out. Use a username and set "Who can find me by number" to Nobody. If a phone number is a problem: SimpleX Chat (most of your friends probably aren't on it).
- Bitwarden: the biggest security improvement for most people. KeePassXC if you want no cloud at all.
- Joplin: plainer than Notion; end-to-end encryption is opt-in. Joplin Server uses a non-open license.
- Krita: no iPad version. For video, Kdenlive. For documents, LibreOffice (export to PDF before submitting).
- Browser: Firefox; one setting turns off most telemetry.
- Messaging apps only work if your friends switch too.
- Local AI comes next, with a demo.
-->

---
layout: center
---

<div class="appeal ap-logos">Logos</div>

## Free to download isn't <span class="g">open source</span>

<p class="big">Obsidian, LM Studio, Llama</p>

<p class="muted">Good tools. Just know which is which.</p>

<p class="src">Obsidian, LM Studio and Llama 4 license terms, checked Oct 2026</p>

<!--
**[34:45–35:30] Free doesn't mean open source**
- Obsidian: closed source, though free for any use since Feb 2025.
- LM Studio: proprietary; its terms call its source code a trade secret.
- Llama 4: open weights under a custom license (700M-user cap, attribution, use policy). Meta's newer Muse Spark Open has a custom license too.
- Using them is fine. Read the license file, not the name. Full table in backup.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/dg-05-local-vs-cloud.png" alt="Two flows. Cloud chatbot: your device, then the internet (encrypted in transit), then the provider's servers where the model runs, subject to retention, human review, training and legal requests under the provider's policy. Local AI app: the model runs on your device, but chat history, logs, backups and sync, and plugins or web search can still store or send data." />

<!--
**[35:30–36:15] Where your prompt goes**
- Cloud: your prompt is stored and handled under the provider's policy (retention, human review, training, legal requests).
- Local: the model runs on your laptop. You still need to check chat history, logs, sync, and plugins.
- Ollama's cloud models and web search send data off your device (set OLLAMA_NO_CLOUD=1). AnythingLLM's telemetry is on until you turn it off.
- Accurate wording: "A correctly configured local setup can avoid sending prompts to a model provider."
-->

---
layout: center
class: framework framework-sm
---

## Before we run it: four questions for <span class="g">Granite 4.2</span>

<div class="grid4">
  <div class="card ap-pathos"><span class="label">Pathos</span><span class="lq">Why do I want it?</span><span class="a" v-click="1">Works offline, no account</span></div>
  <div class="card ap-ethos"><span class="label">Ethos</span><span class="lq">Who's behind it?</span><span class="a" v-click="1">IBM: 95/100 on Stanford's transparency index, the top score</span></div>
  <div class="card ap-logos"><span class="label">Logos</span><span class="lq">What can I check?</span><span class="a" v-click="1">Apache-2.0 license; signed model files</span></div>
  <div class="card ap-kairos"><span class="label">Kairos</span><span class="lq">Why now? Still true?</span><span class="a" v-click="1">Out Aug 2026. That 95 rated Granite 3.3</span></div>
</div>

<p class="src">Stanford CRFM, Foundation Model Transparency Index (Dec 2025); IBM Granite page; Hugging Face model card</p>

<!--
**[36:15–37:45] We do: the four questions on a model, together**
- [Ask the room for each question before clicking.] [Click] reveals all four answers.
- Pathos: it runs on my laptop with Wi-Fi off, with no account.
- Ethos: IBM. In Stanford's 2025 Foundation Model Transparency Index, IBM scored 95/100, the highest in the index's history (average 41). It was the only company that gave enough detail for outside researchers to replicate its training data. IBM's AI management system is ISO/IEC 42001 certified.
- Logos: Apache-2.0 license. Since Apr 29, 2026, IBM cryptographically signs released Granite models, so you can verify the file came from IBM.
- Kairos: Granite 4.2 came out Aug 25, 2026. The 95 was for Granite 3.3, so whether it still holds for 4.2 is an open question. That's kairos in action.
- Size: the 8B model is a 5.3 GB download (Ollama: granite4.2:8b). On an 8 GB laptop, use the 3B (2.2 GB).
- Granite 4.2 is "a strong candidate" for OSI's Open Source AI Definition, not certified.
- [CONFIRM] Swap the model if you demo something else.
-->

---
layout: statement
---

# Demo: Granite running with Wi‑Fi <span class="g">off</span>

<!--
**[37:45–39:15] Live demo: local model offline**
- Night before:
  - Jan (v0.8.7, Apache-2.0): load Granite 4.2 8B from Hugging Face (GGUF). Jan support for 4.2 isn't confirmed, so test it. If it doesn't load, use the Ollama app: `ollama pull granite4.2:8b`, with OLLAMA_NO_CLOUD=1 set.
  - Turn thinking mode off (in Ollama: /set nothink), or the room waits on its reasoning.
  - Test in airplane mode and take the fallback screenshot.
- On stage: turn Wi-Fi off where people can see, then ask it something practical (e.g. "turn these notes into a study guide").
- Jan: analytics are opt-in and data stays on the laptop. Jan's local models don't run on Intel Macs.
- If it fails, go to the next slide.
-->

---
layout: center
class: placeholder-slide
---

<div class="placeholder">

### Demo fallback

[Screenshot: Granite answering with Wi-Fi off]

</div>

<!--
**Fallback (skip if the demo worked)**
- Take this screenshot during your test run and put it in public/.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/om-01-open-vs-closed-gap.png" alt="Dot chart of the gap between the top closed and top open model on Chatbot Arena: 8.0% in Jan 2024, 0.5% in Aug 2024, 1.7% in Feb 2025, 3.3% in Mar 2026." />

<!--
**[39:15–40:00] Open models are good enough for a lot**
- Gap between the top closed and top open model on Chatbot Arena: 8.0% (Jan 2024), 3.3% (Mar 2026). It narrowed, then widened slightly.
- Olmo 3.1 (Ai2) publishes its weights, code, and training data, and matches Grok 4 on several benchmarks with about 90× fewer parameters (AI Index 2026).
- What fits: 8 GB RAM handles 1–4B models comfortably and 7–8B tightly; 16 GB up to about 14B (laptop chart in backup). Phones: PocketPal AI (MIT) runs small models on the device.
- For many everyday tasks, open models are usable now, and your data stays with you.
-->

---
layout: center
---

## Write one alternative next to your <span class="g">starred</span> app.

<p class="muted">Show of hands by category: messaging, notes, AI, creative</p>

<!--
**[40:00–40:45] Pick an alternative**
- 30 seconds to write it down.
- [Hands by category] See where the room landed.
- "I'm keeping it" is a valid answer if you can say which question decided it.
-->

---
layout: section
transition: slide-up
---

# Part 3

## Use them on open source, and on my site

<!--
**[40:45] Part 3: evaluating open source projects, then OSS Fidelity (~14 min)**
-->

---
layout: center
---

## Three terms

- **Repo:** a project's home on GitHub
- **Fork:** a copy someone else continues
- **Release:** a version ready to install

<!--
**[40:45–41:15] Definitions**
- GitHub: the largest site for hosting code (owned by Microsoft).
- OpenTofu and Valkey (Part 1) are forks.
-->

---
layout: center
class: game
---

## Which would you <span class="g">install</span>?

| | Project A | Project B |
|---|---|---|
| Stars | 52,000 | 900 |
| People | 1 | 6 |
| License | none | GPL-3.0 |
| Released | 2 years ago | last month |

<p class="src">Invented examples</p>

<!--
**[41:15–43:15] Table activity: 90 seconds, then vote**
- [Tables discuss] Pick A or B and name the question that decided it.
- [Hands] A? B?
- Answer: B. A's only advantage is stars, which are weak evidence (next slide).
- With no license file, you have no legal right to use or change A's code ("all rights reserved" by default).
-->

---
layout: center
class: graphic
---

<div class="appeal ap-ethos">Ethos</div>

<img src="/graphics-lav/oss-03-popularity-signals-can-lie.png" alt="Three stat tiles: 6 million suspected fake GitHub stars (about 26,000 repos before cleanup, 18,617 after); 1 in 6 popular repos ran fake-star campaigns at the July 2024 peak; under 5% of curl's 2025 bug reports were real, down from over 15%, and the bounty ended January 31, 2026." />

<!--
**[43:15–44:00] Stars can be faked: trust gets faked**
- He et al. (ICSE 2026): about 6 million suspected fake stars. At the July 2024 peak, 1 in 6 popular repos had fake-star campaigns, mostly promoting short-lived phishing and malware repos.
- Stars feel like a crowd vouching for a project (pathos dressed up as ethos). They aren't evidence (logos).
-->

---
layout: center
class: checks-slide
---

## Seven checks, sorted by <span class="g">question</span>

<div class="checks">
  <div class="col ap-pathos"><span class="label">Pathos</span><div class="ck"><b>Fit</b>My devices? Accessible? Exports?</div></div>
  <div class="col ap-ethos"><span class="label">Ethos</span><div class="ck"><b>Identity</b>Official site links here?</div><div class="ck"><b>People</b>More than 1–2 maintainers?</div></div>
  <div class="col ap-logos"><span class="label">Logos</span><div class="ck"><b>License</b>Open license file?</div><div class="ck"><b>Security</b>Policy, advisories?</div><div class="ck"><b>Distribution</b>Official download?</div></div>
  <div class="col ap-kairos"><span class="label">Kairos</span><div class="ck"><b>Maintenance</b>Recent releases, real replies?</div></div>
</div>

<p class="muted small">Weak on their own: stars, downloads, "free" in the name</p>

<p class="src">Adapted from OpenSSF's Concise Guide for Evaluating Open Source Software (2025) and CHAOSS project-health metrics</p>

<!--
**[44:00–45:00] Seven checks, grouped by question**
- Pathos: Fit. Does it work on your devices, meet your accessibility needs, let you export your data?
- Ethos: Identity (does the official site link to this exact repo? avoids copycat repos) and People. Identity is a lateral-reading check.
- Logos: License, Security, Distribution (install from the official site or app store, not a re-upload).
- Kairos: Maintenance. A quiet, mature project isn't necessarily abandoned.
- The original seven-card graphic is in backup.
-->

---
layout: statement
---

<div class="appeal ap-kairos">Kairos</div>

# GitHub's terms allow AI training on public <span class="g">repositories</span>.

## The opt-out does not apply to them.

<p class="src">GitHub Terms of Service, effective Apr 27, 2026, §D.4 and §J.3; not legal advice</p>

<!--
**[45:00–45:45] GitHub's terms (not legal advice)**
- §D.4: you license GitHub and its affiliates (including Microsoft) to use your content "for the purpose of training, developing, and improving artificial intelligence."
- §J.3: the opt-out covers Copilot inputs and outputs, "not … Content stored in public repositories."
- Copilot interaction data has been used for training since Apr 24, 2026, unless you turn it off in settings.
- These terms are from this year (kairos).
-->

---
layout: center
class: hosts-slide
---

## Where your code lives decides who trains <span class="g">AI</span> on it

<div class="hosts">
  <div class="host"><b>GitHub</b><span>Terms allow AI training; the opt-out excludes public repos</span><span class="who">Microsoft</span></div>
  <div class="host hl"><b>Codeberg</b><span>Won't train on your code. Members voted 358–144 to refuse mostly AI-written projects</span><span class="who">German nonprofit</span></div>
  <div class="host"><b>SourceHut</b><span>Terms ban ML-training scrapes and new LLM-written projects</span><span class="who">Small paid company</span></div>
</div>

<p class="src">GitHub ToS (Apr 27, 2026); Codeberg blog (Jul 23, 2026); SourceHut terms (Sep 10, 2026)</p>

<!--
**[45:45–46:45] Other places to host code, and the AI split in open source**
- Codeberg: nonprofit, free for open projects, pledges never to train AI on users' code, blocks AI crawlers. In July 2026 members voted 358–144 (14 abstentions). Its terms now say: "You must not share projects that mostly consist of code written by 'generative AI'-tools."
- SourceHut: paid; terms forbid collecting data to train ML models; from Sep 10, 2026, new projects can't contain LLM-written content.
- GitLab.com: its policy doesn't address training on public content. Self-hosted Forgejo: full control, but you run a server.
- Disclosure: my site was built with AI help, which affects where I can host it. The site says so.
- Open source communities disagree about AI. GitHub went one way; Codeberg and SourceHut went the other.
-->

---
layout: center
class: qr
---

## OSS Fidelity runs these checks for <span class="g">you</span>

<img class="qr-img qr-sm" src="/qr-ossfidelity.png" alt="QR code linking to ossfidelity.com" />

<p class="url">ossfidelity.com</p>

<!--
**[46:45–47:45] Introduce the site; open it on your phone**
- Built from the research behind this talk. It turns the checks into grades and shows the evidence for each.
- Leave this up for 60 seconds.
- The morning of: check that ossfidelity.com loads. If DNS isn't live, use qr-github-io.png (willmitchellcodes.github.io/ossfidelity) instead.
- Rate limit: each live check makes about 15–30 GitHub requests, and GitHub allows 60 per hour per network. On shared venue Wi-Fi the room will hit the limit quickly unless the proxy is deployed. Ask the audience to browse the weekly list; you run the live checks.
-->

---
layout: center
---

## Three grades, each with its evidence

- Reliability <span class="muted">(ethos)</span>: will it still be here and open?
- Maintenance <span class="muted">(kairos)</span>: is someone fixing it?
- Visible security <span class="muted">(logos)</span>: what can we <span class="g">see</span>?

<v-click>

<p class="muted">Pathos is never scored: no stars, no downloads.</p>

</v-click>

<!--
**[47:45–48:45] How the grades map to the framework**
- Reliability ≈ ethos (people, backing, license). Maintenance ≈ kairos (is it still current?). Visible security ≈ logos (what can be checked on GitHub).
- [Click] The site deliberately refuses to score pathos. Stars and downloads are never counted. Every weight and source is on the Method page.
- The site also covers open-weight model openness and the 7-question AI privacy matrix.
-->

---
layout: center
---

## Activity: predict the grade

1. At your table, pick a tool you use
2. Predict its letter grade
3. I'll check it live

<!--
**[48:45–51:45] You do: about 3 minutes**
- 60 seconds at tables to pick a tool and predict A–F. Each table calls out its tool and prediction.
- Run live checks on 2 of their picks (only you run live checks, to stay under the rate limit).
- Already on the weekly list: Signal, Jan, Element, SimpleX, Bitwarden, Joplin, KeePassXC, OBS, Audacity, Penpot, Ollama, PocketPal AI. Add any other project the deck mentions to projects.yml before the talk.
- After each result: "Which grade surprised you, and which of the four questions explains it?"
-->

---
layout: center
class: result-card
---

<div class="result">
  <div class="r-head"><span class="r-name">Signal (Android)</span><span class="r-fid">66 C</span></div>
  <div class="r-row"><span>Reliability</span><span>90 A</span></div>
  <div class="r-row"><span>Maintenance</span><span>96 A</span></div>
  <div class="r-row hl"><span>Visible security</span><span>13 F</span></div>
</div>

<p class="src">OSS Fidelity cached grades, week of Oct 22, 2026; demo fallback</p>

<!--
**[Fallback if the site won't load]**
- Your local copy of the Oct 22 weekly run marks all 14 projects "stale": GitHub's search API returned HTTP 403, so the grades were carried forward from the previous run. Re-run the weekly job with the GitHub App token, then re-check these numbers the morning of.
- Replace with a real screenshot if possible.
- Why Signal gets an F: 98% of last year's commits came from signal.org with few visible pull requests; no SECURITY file on GitHub; no Dependabot config.
- Signal does publish reproducible builds and a security contact outside GitHub. The grade only measures what's visible on GitHub, which is why it's called "Visible security."
-->

---
layout: two-cols
class: contention
---

### Signal

<p class="stat">13 F</p>

<p class="muted">visible security; Signal's security work is mostly off GitHub</p>

<p class="src">OSS Fidelity, signalapp/Signal-Android</p>

::right::

### My own project

<p class="stat">44 D</p>

<p class="muted">adding three small files would raise it</p>

<p class="src">OSS Fidelity, msu/pika-orm; outside review (Oct 21, 2026)</p>

<!--
**[51:45–53:00] Limits of the grades, using my own project**
- PikaORM (github.com/msu/pika-orm, from the personal slides): Fidelity 44 D. Reliability 55, Maintenance 76, Visible security 0.
- The outside review found that adding SECURITY.md, a Dependabot config, and a workflow file raised its Security grade from 0 to about 60 under the formula at the time. The code-review fix since then changes that number, so check the current one in the site's "Why?" panel. Small files can move grades a lot.
- So treat a grade as a starting point. Open the "Why?" breakdown and decide for yourself.
-->

---
layout: center
class: framework framework-sm
---

## Now check <span class="g">my</span> site

<div class="grid4">
  <div class="card ap-pathos"><span class="label">Pathos</span><span class="lq">Why do I want it?</span><span class="a">One letter feels final; you get three, with reasons</span></div>
  <div class="card ap-ethos"><span class="label">Ethos</span><span class="lq">Who's behind it?</span><span class="a">Me, with AI help (disclosed)</span></div>
  <div class="card ap-logos"><span class="label">Logos</span><span class="lq">What can I check?</span><span class="a">Weights on the Method page; blind to work off GitHub</span></div>
  <div class="card ap-kairos"><span class="label">Kairos</span><span class="lq">Why now? Still true?</span><span class="a">Weekly; old grades marked stale</span></div>
</div>

<!--
**[53:00–54:30] Audit the auditor**
- The last use of the framework: on my own tool. A tool that judges evidence can only judge evidence it can see.
- Pathos: a single letter is satisfying, which is exactly why the site shows three grades and the reasons behind each.
- Ethos: built by one student with AI help. That's disclosed on the site.
- Logos: every weight and source is on the Method page, so you can disagree with it. Its blind spot is anything off GitHub (Signal's F).
- Kairos: grades refresh weekly, and old ones are labeled stale. (They were this week.)
- Ask: "What would you want it to check that it doesn't?"
-->

---
layout: center
class: framework framework-lg
---

## The four questions

<div class="grid4">
  <div class="card ap-pathos"><span class="label">Pathos</span><span class="q">Why do I want it?</span></div>
  <div class="card ap-ethos"><span class="label">Ethos</span><span class="q">Who's behind it?</span></div>
  <div class="card ap-logos"><span class="label">Logos</span><span class="q">What can I check?</span></div>
  <div class="card ap-kairos"><span class="label">Kairos</span><span class="q">Why now? Is it still true?</span></div>
</div>

<v-click>

<p class="muted framework-note">You used them on a TV, your apps, a model, a GitHub project, and my site.</p>

</v-click>

<!--
**[54:30–55:15] Recap**
- Four questions, and the ways each gets exploited: wants engineered, trust faked, evidence gamed, the ask timed.
- [Click] You've now practiced them five times.
-->

---
layout: center
---

## Before you leave, write down:

- One app to switch
- One question to ask before installing
- One setting to change this week

<p class="muted">Then tell a neighbor.</p>

<!--
**[55:15–57:00] Next step (attendee goal 4)**
- App: the one you wrote next to your starred app.
- Question: whichever of the four you'll use next time you install something.
- Setting: e.g. turn off chatbot training, check your TV's ACR setting, turn off Firefox telemetry.
- 60 seconds to tell a neighbor.
-->

---
layout: fact
---

# $750

oSTEM and Queer in AI grad-school application aid, due <span class="g">Nov 3</span>

<p class="src">queerinai.com/grad-app-aid</p>

<!--
**[57:00–57:45] Grad application aid**
- Up to US$750 per applicant toward grad application fees. The 2026/27 round closes Nov 3, 2026.
- Queer in AI reports 160 recipients and about $128K paid in earlier rounds.
-->

---
layout: end
transition: slide-up
---

# Thank you

<p class="url">ossfidelity.com</p>

<p class="muted">github.com/willmitchellcodes</p>

<!--
**[57:45–60:00] Questions**
- Backup slides follow: chatbot privacy matrix, AI app layers, model openness, model licenses, productivity studies, AI news errors, verification results, gender-recognition research, pronoun counts, GLAAD index, re-identification, why people skip AI, public concerns, LGBTQ+ adults' concerns, discovery tool criteria, six popularity forces, maintainer concentration, FTC location orders, full swap tables, free vs. open source, laptop model sizes, seven checks, code hosts.
-->

---
layout: section
transition: slide-up
---

# Backup

<!--
Q&A slides. Open the slide overview (press o) to jump to one.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/pv-01-chatbot-privacy-matrix.png" alt="Table for personal accounts. Gemini: trains by default unless Keep Activity is off; temporary chats kept up to 72 hours; human-reviewed chats kept up to 3 years; not used for ads. ChatGPT: trains by default unless 'Improve the model' is off; temporary chats up to 30 days; safety review; ads on Free and Go plans can use past chats with personalization on. Claude: user chooses; if on, data kept up to 5 years; incognito not used for training; flagged chats reviewed; no ads. Copilot new app: not used to train foundation models; retention not stated; personalized ads can use chat history. Meta AI: trains on interactions; retention not published; chats used for ads since Dec 16, 2025 excluding seven sensitive topics." />

<!--
Backup: chatbot privacy for personal accounts (Oct 2026). School accounts differ: Gemini for Education isn't human-reviewed or used for training; with Copilot work/school accounts, institution admins can see logs.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/dg-02-ai-three-layers.png" alt="Three stacked cards. 1: the app you click (interface and runtime): is its code open source, does it send telemetry? 2: the model (weights): what does the weight license allow, is training-data information published? 3: connected services (cloud models, web search, plugins, sync): what leaves your device and under whose privacy policy?" />

<!--
Backup: one AI app has three separate sets of terms. An open source app can call a closed cloud model; a closed app can run open weights locally.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/om-03-how-open-is-open.png" alt="Four columns. Closed (use only through the company's app or API; e.g. ChatGPT, Gemini, Claude): none of weights, open license, training code or data information. Open weights with custom license (e.g. Llama 4, Gemma 3, Muse Spark Open): weights only. Open weights with standard license (Apache-2.0 or MIT; e.g. Gemma 4, Qwen3, Mistral Small 4, DeepSeek, gpt-oss): weights and open license. Open source AI per OSI (e.g. OLMo, Pythia): weights, open license, training code and training-data information." />

<!--
Backup: four levels of openness in AI models (OSI Open Source AI Definition 1.0).
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/om-05-model-license-register.png" alt="Table of open-weight model families: Llama 4 (Llama 4 Community License; 700M-user cap, attribution, EU limit on multimodal; no data/code); Muse Spark Open (Muse Model License; deal for >$20M-revenue API resellers); Gemma 4 (Apache-2.0); Qwen3/Qwen3.8 (Apache-2.0, largest 3.8 models custom); Mistral Small 4 and Large 3 (Apache-2.0; Medium 3.5 Modified MIT with revenue cap); DeepSeek V4/R1 (MIT); gpt-oss (Apache-2.0 plus usage policy); Olmo 3/3.1 (Apache-2.0, releases data, code and checkpoints)." />

<!--
Backup: open-weight model licenses, checked Oct 21, 2026. Granite 4.2 (Apache-2.0, Aug 2026) isn't in this chart.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/ai-11-measured-productivity-effects.png" alt="Dot chart of effects for the AI group, with right meaning better. Speed: Noy and Zhang 40% less time; Dell'Acqua inside-frontier tasks 25% faster; METR early 2025 19% slower (95% CI 2–39% slower); METR late 2025 returning developers 18% faster but inconclusive. Output: Brynjolfsson +15% issues per hour; Cui +26% pull requests (CI +6 to +46%); Dell'Acqua +12% tasks. Quality: Noy and Zhang +18%; Dell'Acqua outside-frontier task 19% less likely correct; Cui build success −5.5% (not significant). Learning: Bastani −17% exam score after unguarded AI practice; Shen and Tamkin quiz 50% vs 67%." />

<!--
Backup: measured productivity effects. Don't average these into one number. For studying: students who practiced with unrestricted GPT scored 17% lower on the exam afterward; a tutor version that gave hints instead of answers avoided most of that (Bastani 2025).
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/ai-13-ai-news-answers-errors.png" alt="Left: 45% of AI assistant answers to news questions had at least one significant issue, 31% had significant sourcing problems and 20% significant accuracy problems. Right: share with a significant issue by assistant: Gemini 76%, Copilot 37%, ChatGPT 36%, Perplexity 30%." />

<!--
Backup: EBU and BBC (2025), 2,709 answers. Use AI to find sources, then open and read them.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/ai-14-verified-isnt-meaningful.png" alt="Funnel on a log scale: 700 open Erdős problems attempted by an AI agent; 212 answers its own verifier marked correct; 63 judged technically correct by experts; 13 judged meaningfully correct." />

<!--
Backup: verification checks correctness, not whether the result matters (Feng et al., 2026).
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/qa-06-misgendering-machines.png" alt="Three stat cards from a review of 58 automatic gender recognition papers: 94.8% treated gender as binary, 72.4% as immutable, 60.3% as physiological." />

<!--
Backup: Keyes (2018). Describes how researchers modeled gender, not how accurate deployed products are.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/qa-05-wikipedia-pronouns.png" alt="Log-scale bar chart of pronoun mentions in English Wikipedia (March 2021): he over 15 million, they 4.9 million (mostly plural), she 4.8 million, ze 7,400, xe 4,500, ey 2,900." />

<!--
Backup: raw string counts. Most "xe" and "ze" matches weren't pronouns at all (Dev et al., 2021).
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/risk-01-glaad-safety-scores.png" alt="Dot plot of GLAAD policy scores out of 100, 2025 to 2026: TikTok 56 to 56; Instagram 45 to 41; Facebook 45 to 40; Threads 40 to 39; YouTube 41 to 30; X 30 to 29." />

<!--
Backup: GLAAD's index scores published policies, not enforcement or anyone's chance of harm.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/qa-09-three-facts-identify-you.png" alt="ZIP code plus gender plus date of birth: 87% of the U.S. population likely unique using 1990 Census data (Sweeney 2000); 63% in a re-check using 2000 Census data (Golle 2006)." />

<!--
Backup: "anonymous" data often isn't. Small queer datasets are especially easy to re-identify.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/ai-03-why-people-abstain.png" alt="Stacked bar chart among U.S. adults who don't use AI chatbots. Not interested: 60% major reason, 83% major or minor. Concerned about personal information: 54% major, 79% total. Don't trust the accuracy: 45% major, 76% total. Don't know how to use them: 29% major, 55% total. Worried what others would think: 3% major, 14% total." />

<!--
Backup: reasons people don't use AI chatbots (Pew 2026). Concern about personal information outranks not knowing how.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/ai-04-public-concerns.png" alt="Horizontal bar chart of U.S. adults: 71% say AI will make personal information less secure; 67% have little or no confidence the government will regulate AI well; 63% say AI is advancing too quickly; 59% have little or no confidence companies will develop AI responsibly." />

<!--
Backup: public concerns about AI (Pew 2026).
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/qa-04-lgbtq-adults-ai-concerns.png" alt="Horizontal bars, LGBTQ+ U.S. adults somewhat or very concerned: spreading misinformation 73%, replacing human oversight in safety systems 73%, privacy risks that could expose LGBTQ+ identities 72%, bias in content moderation 71%, bias in algorithms 68%." />

<!--
Backup: LGBT Tech / Data for Progress (Apr 2025, n = 1,286). About 73% also saw benefits. Survey by an advocacy organization.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/oss-07-discovery-tool-criteria.png" alt="Table mapping the presenter's discovery-tool criteria to existing measures and cautions: commits and active developers to CHAOSS Contributor Absence Factor and Scorecard Contributors; license to Scorecard License and SPDX; releases and issues to Scorecard Maintained and CHAOSS metrics; organization backing to foundation membership; hidden proprietary parts to dependency license scans; AI-generated commits has no standard yet; AI privacy to the seven privacy questions." />

<!--
Backup: how OSS Fidelity's criteria map to OpenSSF Scorecard and CHAOSS.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/dg-04-why-popular-isnt-best-fit.png" alt="Six cards with audience questions: Defaults (was it preinstalled or picked for you?), Network effects (is it only useful because friends use it?), Switching costs (can you export your data?), Bundling (did it come with school, work or your device?), Friction (is accepting easier than refusing?), Compatibility (will collaborators open your files?)." />

<!--
Backup (moved from Part 1 in v2): six reasons software gets popular. None is about whether the tool is good for you. Jan 2021: WhatsApp delayed a privacy-policy update after user confusion, and Signal and Telegram saw large sign-up spikes.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/oss-02-few-maintainers.png" alt="Cumulative bars: among top non-npm packages, 17% had one developer writing over 80% of 2023 commits; 40% had two or fewer; 64% four or fewer; 81% ten or fewer." />

<!--
Backup (moved from Part 1 in v2): Census III (Linux Foundation + Harvard, Dec 2024). Tidelift survey (secondary): about 60% of maintainers are unpaid.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/risk-03-ftc-location-orders.png" alt="Table of FTC location-data broker orders: X-Mode/Outlogic (final Apr 2024) names LGBTQ+-serving places; InMarket (May 2024) does not but bans selling any precise location data; Gravy Analytics/Venntel (Jan 2025) yes, in a separate section; Mobilewalla (Jan 2025) yes; Kochava (Jun 2026) no, narrower sensitive-location list." />

<!--
Backup (moved from Part 1 in v2): FTC location-data orders. Kochava's list comparison comes from law-firm analyses (secondary).
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/sw-01-start-here-everyday.png" alt="Table: ChatGPT app to Jan (Apache-2.0); ChatGPT on phone to PocketPal AI (MIT); WhatsApp or iMessage to Signal (AGPL-3.0, needs phone number); without a phone number, SimpleX Chat (AGPL-3.0); Chrome to Firefox (MPL-2.0, telemetry on by default); LastPass to Bitwarden (GPL-3.0 apps); Microsoft Office to LibreOffice (MPL-2.0); Notion or OneNote to Joplin (AGPL-3.0)." />

<!--
Backup (moved from Part 4 in v2): full everyday swaps table.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/sw-02-start-here-creative.png" alt="Table: Procreate to Krita (GPL-3.0, no iPad); Photoshop photo editing to GIMP 3.2 (GPL-3.0+); Illustrator to Inkscape; Premiere or CapCut to Kdenlive (GPL-3.0); Maya to Blender (Apple Silicon Macs only); Figma to Penpot (MPL-2.0, browser); Audition to Audacity 4 (GPL-3.0); GitHub for open projects to Codeberg." />

<!--
Backup (moved from Part 4 in v2): full creative swaps table. GIMP has no official App Store version, so App Store listings are third-party copies. Audacity 4 has a new interface; older tutorials won't match.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/sw-03-free-isnt-open-source.png" alt="Table of tools that look open but aren't: LM Studio (proprietary), Msty (proprietary, non-commercial free tier), Obsidian (closed source, free), Anytype (source-available), Open WebUI v0.6.6+ (custom license with branding clause), Llama and Muse Spark Open (custom model licenses)." />

<!--
Backup (moved from Part 4 in v2): full "free isn't open source" table.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/om-04-what-fits-on-a-laptop.png" alt="Horizontal bars of 4-bit model download sizes with reference lines at 8 GB and 16 GB of RAM: Llama 3.2 3B 2.0 GB; Qwen3 4B 2.5 GB; Phi-4-mini 2.5 GB; Gemma 3 4B 3.4 GB; Llama 3.1 8B 4.9 GB; Qwen3 8B 5.2 GB; Qwen3 14B 9.3 GB; gpt-oss 20B 14 GB; Gemma 3 27B 17 GB; Qwen3 30B MoE 19 GB." />

<!--
Backup (moved from Part 4 in v2): what runs on a student laptop. Granite 4.2 isn't in this chart: 3B is 2.2 GB, 8B is 5.3 GB, 30B is 18 GB (Ollama library).
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/oss-06-vet-before-you-install.png" alt="Seven cards: 1 Identity (does the official site link to this repo?), 2 License (is there an open source LICENSE file?), 3 Maintenance (recent releases, real replies to issues?), 4 Distribution (official site or app store), 5 Security (security policy and advisories?), 6 People (more than one or two active maintainers?), 7 Fit (platforms, accessibility, data export). Weak evidence on its own: stars, download counts, and free in the name." />

<!--
Backup (moved from Part 5 in v2): the original seven-checks graphic.
-->

---
layout: center
class: graphic
---

<img src="/graphics-lav/oss-05-where-your-code-trains-ai.png" alt="Table of code-hosting sites. GitHub: terms grant GitHub and Microsoft the right to train AI on your content; the opt-out doesn't cover public repos; Copilot interactions are used for training unless you opt out since April 24, 2026; Microsoft subsidiary. Codeberg: pledges never to train on users' code, blocks AI crawlers; German non-profit. SourceHut: terms forbid collecting data to train ML models; small paid company. GitLab.com: public-content training not addressed; Duo inputs and outputs not used to train; open-core public company." />

<!--
Backup (moved from Part 5 in v2): full code-host comparison, including GitLab.com.
-->
