# STATE

## 2026-11-06 — About video preview commit preparation

- `REQ-0023` is implemented and independently verified; see `REQUIREMENTS.md` and `VALIDATION_SUMMARY.md`. The user authorized feature-branch push, PR and squash merge subject to checks. Next: complete and verify that workflow; verify deployment separately. Preserve the branch.

## 2026-11-06 — awaiting the next request

- Cycle `C1`. The user will provide a new task; no new implementation is approved. Read the project protocol, instructions, state, checkpoints, approvals and requested Agile V skills. The pending `CP-0001` is historical: `GATE-0001` was superseded by `DEC-0005`.
- The earlier `REQ-0022` commit-preparation note predates its merge. Remote `main` points to `f6f1491` (About video and company vision); the retained local branch `feat/about-video-vision` is clean at `b25a5fc` before this state update. No deployment or behavior was checked in this readiness session.
- Next: receive the request, inspect the affected source and requirements, update relevant planning records, and present a scoped plan for approval before coding. Preserve existing work.

## 2026-11-05 — About video and vision commit preparation

- `REQ-0022`: see `TASKS.md` and `VALIDATION_SUMMARY.md`. Next exact task: complete and verify the authorized PR workflow, then verify deployment separately. Preserve the feature branch unless deletion is separately authorized.

## 2026-11-05 — hero, company links and page copy commit preparation

- `REQ-0020` and `REQ-0021`: see `TASKS.md` and `VALIDATION_SUMMARY.md`. Next exact task: complete and verify the authorized PR workflow, then verify deployment separately. Preserve the feature branch unless deletion is separately authorized.

## 2026-11-05 — home caption alignment commit preparation

- Completed and independently verified `REQ-0019`; see `REQUIREMENTS.md` and `VALIDATION_SUMMARY.md`. The user authorized the feature-branch, PR and squash-merge workflow subject to checks.
- Next exact task: complete and verify publication through the PR; verify deployment separately. Production, other browsers and physical devices remain unverified. Preserve the feature branch unless deletion is separately authorized.

## 2026-11-05 — home caption interaction commit preparation

- Completed and independently verified `REQ-0018`; see `REQUIREMENTS.md` and `VALIDATION_SUMMARY.md`. The user authorized the feature-branch, PR and squash-merge workflow subject to checks.
- Next exact task: complete and verify publication through the PR, then verify deployment separately. Production, other browsers and physical devices remain unverified. Preserve the feature branch unless deletion is separately authorized.

## 2026-11-05 — awaiting the next request

- Cycle `C1`; awaiting the user's new request and subsequent scope approval. `GATE-0001` is superseded as recorded in `GATES.md` and `DEC-0005`; its pending checkpoint is historical. No new requirement or implementation is approved by this readiness check.
- Read `docs/AGILE_V_PROTOCOL.md` (there is no root-level copy), `CLAUDE.md`, `AGENTS.md`, this state, checkpoints and approvals. The latest recorded work covers `REQ-0015` through `REQ-0017`; their validation evidence is in `VALIDATION_SUMMARY.md`.
- The working tree was clean on `fix/hero-navigation-overlap` at `73e6d4e` before this state update. Remote branch references report that same commit, `main` at `06d71ac`, and `fix/footer-information` at `45a3ff7`. Older branch and deployment instructions below have not been reconciled with remote pull requests or live hosting; do not assume their status. `public/` contains 15 HTML files and `wrangler.toml` serves it.
- No application files were changed or behavior tested in this check. Deployment and pull request status were not verified. Remaining: receive the request, inspect its affected code and requirements, record a scoped plan with risks and dependencies, and wait for approval before coding. Do not switch branches or perform Git publication as part of this readiness check.

## 2026-11-03 — hero stacking and frame glow commit preparation

- Completed `REQ-0017`: isolated the home hero's stacking context and reused its shadow on the requested home, service, and project elements. Local browser and independent verification passed; see `VALIDATION_SUMMARY.md`.
- The user authorized commit, branch push, PR creation, and squash merge subject to checks and protections. Next exact task: complete and verify that workflow; production and cross-browser behavior remain unverified. Preserve branches unless their deletion is separately authorized.

## 2026-11-03 — enquiry fallback commit preparation

- Completed `REQ-0016`: the contact form stays hidden until JavaScript initializes and a bilingual phone/WhatsApp fallback is shown until then. Informative images have Bangla and English alternatives; decorative images remain silent.
- Local browser and independent checks passed; see `VALIDATION_SUMMARY.md`. No message was sent and production was not tested in verification.
- The user authorized commit, branch push, PR, and squash merge after checks. Next exact task: complete and verify that workflow, then verify the live deployment. Do not delete the feature branch without separate authorization.

## 2026-11-03 — metadata commit preparation

- Implemented and locally verified `REQ-0015`: consistent business naming and organization data across 15 page heads, five corrected sitemap dates, and a test-host-specific Vercel `noindex, follow` header. Page bodies and the production canonical origin are unchanged.
- Independent verification and local Chrome regression checks passed; see `VALIDATION_SUMMARY.md`. Live Vercel header behavior and social previews require post-deployment verification. The prepared Cloudflare `www` to apex redirect has not been applied.
- The user authorized a feature-branch commit and push, PR creation, and squash merge after checks. Next exact action: complete that workflow without modifying Cloudflare redirect settings; verify the PR, merge, and deployments. Keep the branch unless separately authorized to delete it.

## 2026-11-03 — approved metadata scope

- The user approved `REQ-0015`: update metadata on 15 pages, sitemap dates, and a test-host-only Vercel indexing header; prepare a Cloudflare hostname redirect without deploying it.
- Implementation starts on `fix/footer-information` with the existing readiness-state edit preserved. Keep visible page bodies, CSS, and JavaScript unchanged; do not push, deploy, or modify hosting settings.
- Next exact task: implement `REQ-0015`, validate the local files and crawler responses, and obtain independent verification. Live preview, Vercel header, redirect, and search indexing require separately authorized deployment and external verification.

## 2026-11-03 — awaiting new request

- Loaded the Agile V protocol, project instructions, state, checkpoint, and approval records. `GATE-0001` remains superseded by the later recorded direction; new implementation still requires a scoped plan and approval.
- Local branch `fix/footer-information` is clean at `1b16759` before this state update. `git ls-remote` reports that commit on the remote feature branch and `58d6a22` on remote `main`; local `main` is behind. The prior session recorded PR 17 as squash-merged at `58d6a22` and the Worker build as successful. The PR API could not be reached in this readiness check; live deployment was not rechecked.
- The static publish root is `public/`, with 15 HTML entry points; `wrangler.toml` serves that directory. No application files were changed or tested in this readiness check.
- Remaining: the user has not yet provided the new task. Next exact action: receive it, inspect affected code and requirements, update relevant planning records, identify risks and dependencies, and present a scoped plan. Wait for approval before coding. Do not switch branches or overwrite work during this readiness check.

## 2026-11-02 — commit preparation

- Completed `REQ-0013` image refresh and `REQ-0014` responsive changes. Footer, header, contact form and preview fit narrow screens; home captions wrap within a stable frame during fades.
- Local responsive and workflow checks, independent caption verification, and limitations are recorded in `VALIDATION_SUMMARY.md`. Existing image additions and deletions are intentional for the approved refresh.
- The user authorized committing, pushing `fix/footer-information`, creating a pull request, and squash merging into `main` if checks and protections permit. Do not delete the branch without separate authorization.
- Next exact task: finish the authorized GitHub workflow, verify the resulting PR and merge, and check the deployment separately. Earlier implementation and deployment notes below are historical where they conflict.

## 2026-11-02 — project image refresh

- Completed approved `REQ-0013`: refreshed four project detail banners and galleries, applied shared 4:3 gallery styling, and repaired the design and solar listing images. The assessment and interior pages retain their existing banners and have no galleries.
- Validation: local Chrome checks at desktop and mobile widths, image path and HTTP checks, and `git diff --check` passed; see `VALIDATION_SUMMARY.md` for scope and limitations. Production was not tested.
- Existing user-provided image additions and deletions were preserved. The work remains on `fix/footer-information`; no push, pull request, merge, or deployment was performed.
- Remaining: user review. Next exact task: respond to the user's review or further direction; any remote publication is outside this task. The image-specific portions of older notes below are historical.

## 2026-11-02 readiness checkpoint

- The user will provide a new request. Analyze its scope, update relevant planning records, and present a plan for approval before coding.
- Read `docs/AGILE_V_PROTOCOL.md` (there is no root-level `AGILE_V_PROTOCOL.md`), `CLAUDE.md`, `AGENTS.md`, the Agile V core and pipeline skills, and the existing checkpoint and approval records.
- Local reconciliation: `public/` contains 15 HTML entry points; `wrangler.toml` serves `./public`. The current branch is `fix/footer-information` and the working tree was clean before this state update. The recorded supersession of `GATE-0001` remains in effect; no new work is approved by this readiness checkpoint.
- No application code changed and no behavior or deployment was tested in this readiness check. The earlier deployment note below has not been reverified.
- Next exact task: receive the user's request, inspect its affected code and requirements, identify risks and dependencies, update relevant planning files, and propose a scoped plan. Wait for approval before implementation.

## Resume point

Cycle: `C1`
Phase: The home frame is 4:3. From 861px up the diamond row and the caption share one line, and the frame sits just above that line. It crossfades `public/img/home-hero/hero-1.jpeg` through `hero-5.jpeg`, and each picture fades its own Bangla and English caption. `hero-2.jpeg` through `hero-5.jpeg` are 1024×768. `hero-1.jpeg` is 1024×678, so the frame still crops a little of each side. The side rules follow the current line. The office-photo caption stays. The other four are the licensed-partner, construction-support, test-report, and inside-the-home slogans. Detail pages keep 28px above and below the two buttons. The hold is 3 seconds. The next picture is decoded before it fades in. The cycle pauses on hover and while the tab is hidden. Reduced motion keeps the first picture and its caption. The projects intro is the showcase line in both languages. Concrete, interior, assessment, and fire cards use `project-1-card.jpeg`, `project-5-card.jpeg`, `project-3-card.jpeg`, and `poster-6-card.jpeg`. Design and solar cards still use their posters. Each detail page opens with a 16:9 banner, then the existing title. The facts list stays in the HTML and is hidden. Gallery pictures keep their own ratio. The design banner is `hero-1.png`. The other five banners are their posters, and those posters are not repeated in the gallery. A picture line appears only for design, concrete, and solar, and those lines no longer say “this”. Each detail page’s opening paragraph describes the category. Pull requests 11 through 14 are on `main`. Pull request 15 is on `main`. Worker `divine-dream-20ba` is connected to GitHub repository `arnobt78/Real-State-Consultancy-Brochure--VanillaJS-HTML5-CSS3-Frontend`, production branch `main`, with no build command and deploy command `npx wrangler deploy`. Preview builds are off. The GitHub app can see only that repository. The API token stays in Cloudflare and is not in this repo. The live deployment is still the manual upload `e6b06886`. Pull request 16 is the push that starts the first Git build. Vercel Production follows `main` and stays the test site. The official address stays `https://buildsafe.com.bd`.
Branch: `fix/footer-information` is the only feature branch. Do not open another branch. Older branches were removed after their pull requests merged.
Remote: `https://github.com/arnobt78/Real-State-Consultancy--VanillaJS-HTML5-CSS3.git`
Gate: `GATE-0001` was superseded. Do not wait on token `C1-HG1-7f3a`. Do not revert `public/` because that token is missing.

Next exact action: after pull request 16 is on `main`, merge `main` back into `fix/footer-information` and leave that branch. Watch the Worker Deployments tab. The live pages change only after a Git deploy shows Ready. Do not click New deployment. Do not drag-upload `public/`. Do not open another branch. Do not push new implementation straight to `main`. Design and solar card pictures stay until the client supplies new 4:3 files. `hero-1.jpeg` is 1024×678, so the home frame still crops a little of each side. Do not follow `docs/VERCEL-PLAIN-JS-DEPLOY.md`. A Vercel test deploy uses output directory `public` with no build command.

## What the project is

Verified from the repository on 2026-10-28:

Build Safe Engineering & Consultancy is a bilingual Bangla/English brochure. The pages are static files in `public/`. Shared files are `public/css/site.css` and `public/js/site.js`. There is no package manager, backend, database, authentication, test runner, or build step.

The 2026-10-27 notes below describe the old single `index.html`. That file is no longer the site.

Public contact data in the pages (intentional, not a secret):

- Phone and WhatsApp: `+880 1814-116677` / `https://wa.me/8801814116677`
- Office: Dilara Tower, 77 Sonargaon Road, Hatirpool, Dhaka-1205
- Facebook: `https://www.facebook.com/buildsafe.ec`
- LinkedIn: `https://www.linkedin.com/in/md-mamunoor-rashid/`
- YouTube: `https://www.youtube.com/@BuildSafe-EC`
- Messenger: `https://m.me/buildsafe.ec`
- Email: `contact.buildsafe@gmail.com`

## Architecture (current)

- Publish root is `public/`. Nine HTML pages, plus six project detail pages, share `public/css/site.css` and `public/js/site.js`.
- Bangla is the default. English is in the same file and is shown when `data-lang` is `en`. The choice is stored as `bs-lang`. A head script sets that attribute before first paint when the saved value is `en`. Header links follow the visible words, in the order Home, About, Services, Projects, FAQ, Contact. The phone menu uses that same header. Footer Pages lists those same six links. The Office column lists the phone, `contact.buildsafe@gmail.com`, and the Dilara Tower address, with Facebook, LinkedIn, and YouTube under those lines. At 760px and below, the brand, Pages, and Office each take a full row. The footer address matches the other footer lines. On a phone, the copyright line and the slogan are centered. The slogan is “Partner with BUILD SAFE to turn your vision into reality”, in the same color as the rest of the line. The contact email matches the phone number and has a copy button. The copy notice sits at the bottom right. The FAQ page has 15 bilingual questions drawn from the existing pages, with about 20px of padding per item. Link previews use `public/img/meta-logo.jpg`. The structured-data logo and the header image stay `logo.png`. The home frame uses `hero-1.jpeg` through `hero-5.jpeg`. Without JavaScript, only the first picture shows. Terms, Privacy, and Cookies stay public and in the sitemap, and they are not in the footer. The contact service menu is two selects so its label is already in the saved language.
- The contact form validates a name and a Bangladesh mobile number, then prepares a WhatsApp link. It does not post to a server.
- Project cards link to `/projects/design-technical-support/`, `/projects/concrete-mix-design-testing/`, `/projects/detailed-engineering-assessment/`, `/projects/interior-design/`, `/projects/solar-system-design-installation/`, and `/projects/fire-safety-hvac/`. The concrete, interior, assessment, and fire card images are `project-1-card.jpeg`, `project-5-card.jpeg`, `project-3-card.jpeg`, and `poster-6-card.jpeg`. Those card files are not on the detail pages. The old `p1.jpg` through `p6.jpg` probes are gone. `hero-1.png` is the design-page banner only. The home frame uses `hero-1.jpeg` through `hero-5.jpeg`.
- Dark colors follow the system. Fonts are files in `public/fonts/`.
- Serve `public/` with no build command. Do not follow `docs/VERCEL-PLAIN-JS-DEPLOY.md`.

## Architecture (2026-10-27, historical)

- Hash pages: `home`, `services`, `about`, `projects`, `contact`. Non-home pages start with the `hidden` attribute.
- Default language is Bangla, because CSS hides `[lang="en"]` until `data-lang="en"`. The script then sets `data-lang` from `localStorage` key `bs-lang`, falling back to `bn`.
- Eight services (`svc-1` through `svc-8`) use `img/s1.jpg` through `img/s8.jpg`. The hero also uses `img/s1.jpg`.
- The enquiry form does not post to a server. It validates name and an 11-digit BD mobile number, builds a message, and opens WhatsApp with that text. Messenger is a plain link and does not receive the message.
- Project cards look for `img/projects/p1.jpg` through `p6.jpg` and keep the “photo coming soon” placeholder when the file is absent. That directory is absent.
- Dark-theme tokens exist for `prefers-color-scheme: dark` and `[data-theme="dark"]`. No control sets `data-theme`.

`CLAUDE.md` was a blank template that told agents to use TypeScript and server components. That conflicted with the code. It now records this static architecture. `AGENTS.md` still matches the workflow and was left unchanged. `docs/architecture.md` was not added; this file is the architecture record for C1.

## Completed this session

- Worker `divine-dream-20ba` is connected to the brochure repository on branch `main`.
- The first Git build had not started. The active deployment was still manual upload `e6b06886`.

## Active requirement IDs

Baseline, already in `index.html`, not executed in a browser this session:

- `REQ-0001` `REQ-0002` `REQ-0003` `REQ-0004` `REQ-0005` `REQ-0006`

Proposed, blocked on `GATE-0001`:

- `REQ-0007` `REQ-0008` `REQ-0009` `REQ-0010` `REQ-0011` `REQ-0012`

## Files changed this session

- `CLAUDE.md`
- `.agile-v/STATE.md`, `CHANGELOG.md`, `VALIDATION_SUMMARY.md`, `DECISION_LOG.md`

Not changed: `AGENTS.md` and `docs/VERCEL-PLAIN-JS-DEPLOY.md`.

## Validation

No typecheck, lint, test, or build script exists. The home cycle, the project pages, the contact form, and the other routes were checked in a local browser. See `VALIDATION_SUMMARY.md`.

## Blockers

- `GATE-0001` was superseded. Do not halt new page work on token `C1-HG1-7f3a`.
- Canonical pages use `https://buildsafe.com.bd/`. The Worker is connected to GitHub. The first Git deploy had not replaced manual upload `e6b06886` when this note was written.
- `REQ-0005` now uses the six named project folders. The old `p1.jpg` through `p6.jpg` names are not requested.

## Unresolved questions

1. Which proposed requirement IDs are in scope for C1?
2. Theme: follow the system, lock light, or add a toggle? Recommendation is in `REQ-0009`.
3. Without JavaScript, is a phone fallback enough, or should every section stay visible? Recommendation is in `REQ-0008`.
4. What is the public site URL, if any?
5. Design and solar cards still use posters that are not 4:3. `hero-1.jpeg` is 1024×678, so the home frame still crops a little of each side. Do not replace those until the client supplies the new files.

## Deferred

Recorded in `TASKS.md` as out of scope until a later approval: enquiry storage, a framework or backend, deployment, and git initialization.
