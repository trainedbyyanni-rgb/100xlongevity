# 100X Longevity — Project Context

## What this is
A static HTML site for 100X Longevity (formerly "100X Yanni"), a personal brand covering cognitive science, neuroscience, and performance research. No build step, no framework, no package manager. Plain HTML, CSS, and vanilla JS served as static files.

Owner: Yanni Jereissati (@100xyanni — social handle, unaffected by the site rebrand). Also runs Menkor, a separate RUO nootropic brand. As of the compounds/index.html rebuild, Menkor product links are now permitted specifically on the Compounds page (Semax, Adamax, Selank, linking out to menkorbio.com) — this reverses the earlier "never link Menkor" rule for that page only. Do not add Menkor links or mentions to any other page without explicit confirmation.

## Site structure
- index.html — homepage: age gate, hero, philosophy strip, video, reasoning cards, learn grid
- coaching.html — 1:1 coaching offer + application CTA
- videos.html — YouTube video index
- sources.html — full citation library
- admin.html — blog post editor (localStorage-based, see Known Issues)
- assets/style.css — shared stylesheet
- blog/index.html, blog/post.html, blog/post-template.html
- cognitive/index.html — lesson hub
- cognitive/*.html — individual lessons
- compounds/index.html — rebuilt Compounds quick-reference page (Semax, Adamax, Selank), links out to Menkor product pages (see exception above)

## Design system
- Headings: Bebas Neue. Body: DM Sans. Serif accents: DM Serif Display.
- Palette: white #fff, near-black #111, grey #999/#bbb, borders #ececec
- Blue #0066cc only for citation superscripts and external source links
- Flat design. No shadows, gradients, or rounded corners beyond 0.08rem
- Grid borders made with 1px gap on grey background, not border properties

## Writing tone (IMPORTANT)
- Open lessons with "Hey friends and researchers."
- Full complete sentences that flow into each other. Never fragmented phrases.
- No em dashes or en dashes. Use commas, semicolons, or restructure.
- Calm, precise, scientifically grounded. No motivational or hype language.
- Mechanism before conclusion.
- Every factual claim needs a numbered citation linking to a real source. Never invent one.

## Content scope — three pillars only
1. Longevity  2. Brain health  3. Cognitive function

Anything outside these is out of scope. Earlier anabolic/peptide/body-composition content is deprecated. Do not add to it.

## Content scope — androgen & hormone pharmacology (added)
A deliberate, separate exception to the deprecation rule above: androgen and hormone pharmacology is in scope when it ties back to longevity, mood, or brain mechanisms. This covers testosterone/DHT/estrogen neurochemistry, DHT-targeting compounds (e.g. hair loss pharmacology), PDE5 inhibitors, and mortality/longevity data involving androgens (e.g. castration studies, anabolic steroid outcomes). Pages currently live in this area:
- cognitive/testosterone-neurochemistry.html
- cognitive/hair-loss-dht.html
- cognitive/non-negotiables-pde5.html
- cognitive/longevity-soma-theory.html (includes eunuch/AAS mortality sections)
- cognitive/lifestyle/testosterone-optimization.html

The old peptide/body-composition content referenced in compounds/index.html remains deprecated — this exception is specifically for hormone/androgen pharmacology framed through longevity or brain mechanisms, not a reopening of the earlier anabolic-focused version of the site.

## Lessons that actually exist
- cognitive/acetylcholine.html — Lesson 01, 27 references
- cognitive/bdnf.html — Lesson 02, ~21 references
- cognitive/ssri.html
- cognitive/amphetamines.html
- cognitive/wakefulness.html

Everything else in the cognitive hub is a roadmap card, not a real page.

## Known issues / open work
1. Blog is architecturally broken. admin.html writes to localStorage key `100xyanni_posts`; blog/index.html and blog/post.html read from it. localStorage is per-browser, so posts are invisible to visitors and not indexable. Needs replacing with real static .html files per post. Preferred: keep the admin form but have it generate a downloadable .html file.
2. Video embeds. Only one confirmed-valid YouTube ID exists: g7FVEpNlcwI. Channel: https://www.youtube.com/@yannislongevity. Never guess or invent a video ID. Embeds will not load over file:// — test with `python3 -m http.server 8000`.
3. Duplicated CSS. The same social strip / nav override / reset block is inlined in 10+ files instead of assets/style.css.
4. No domain yet. Local only.
5. Coaching CTA points to href="#" — needs a Tally form URL.

## Rules
- Never invent citations, PubMed IDs, study findings, or YouTube video IDs.
- Never claim a link works just because the target file exists. Verify the content matches.
- No stock photography, testimonials, or placeholder testimonials.
- No pricing on the coaching page.
- Keep the medical disclaimer in the footer of every page.
- Ask before creating new pages.
