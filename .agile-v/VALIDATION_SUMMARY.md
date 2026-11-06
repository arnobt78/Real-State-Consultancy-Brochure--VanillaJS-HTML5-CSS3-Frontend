# VALIDATION SUMMARY

## 2026-11-07 — responsive frames, touch and copy (`REQ-0024`–`REQ-0026`)

- Local and independent Chrome checks covered all five slideshow images and captions in both languages at phone and desktop widths, including the updated fourth image, timing and touch-emulated holds, cancellation, scrolling and reduced motion. Native long-press behavior on physical phones remains unverified.
- About and six project frames passed size, centering and contain checks from 320 to 1920px, including short viewports; YouTube playback and narrow-screen fallback passed. About spacing measured 28px with fallback hidden; visible fallback spacing did not overlap or double the gap.
- All 15 routes passed local HTTP and language-switching checks. Contact validation, Bangla digits, service preselection, WhatsApp handoff and edit passed; no message was sent. `node --check public/js/site.js` and `git diff --check` passed. No published English advice variants remained in the source scan.
- Existing layout overflow remains at 240px; short landscape viewports may require scrolling. Production, physical devices, other browsers and performance benchmarks were not tested. The repository has no lint, typecheck, automated test suite or build command.

## 2026-11-06 — About video preview and link styling (`REQ-0023`)

- Local and independent Chrome checks passed for the YouTube thumbnail, keyboard and touch activation, blocked player, disabled JavaScript, languages, themes and fallback at 240–1440px, including resize across the narrow breakpoint. The video played in headless Chrome; YouTube controls its branding and related videos.
- Footer styles and horizontal fit passed on all 15 routes at 390 and 1440px. Roadmap hover and keyboard focus, contact validation, Bangla digits, service preselection, WhatsApp handoff and edit passed locally. No message was sent. `node --check public/js/site.js` and `git diff --check` passed.
- PR review identified that color alone distinguished the roadmap links. A small external-link cue was added; local Chrome checks passed in both languages at 320 and 1440px, including layout, hover and focus.
- One parallel local-server run failed to initialize JavaScript but passed sequentially. Existing layouts overflow below 280px. Production, physical devices, other browsers and comparative performance were not tested. No repository lint, typecheck, automated test suite or build command exists.

## 2026-11-05 — About video and vision (`REQ-0022`)

- Local Chrome and independent checks covered About and Home at 280, 320, 390, 768 and 1440px in Bangla and English, light and dark themes. Video framing, fallback, content, card icons and glow, social links, navigation, home slideshow and horizontal overflow passed.
- The embedded YouTube video played in local Chrome with playback time advancing; an earlier headless attempt timed out. All 15 routes loaded at 390 and 1440px with local HTTP and navigation checks passing. `git diff --check` and `node --check public/js/site.js` passed.
- Following PR review, local and independent checks covered the 200-by-200 minimum player viewport and direct-link fallback on smaller widths, the roadmap's visible focus color, and the bilingual privacy and cookies disclosures. The video remains 16:9 where space permits and is taller on narrow phones; it played at 320px in local Chrome. Existing page layouts overflow at widths below 280px.
- Production, other browsers, physical devices and performance were not tested. The static site has no lint, typecheck, unit-test suite or build command.

## 2026-11-05 — hero, company links and page copy (`REQ-0020`, `REQ-0021`)

- Local Chrome and independent checks covered all 15 routes at 320, 390, 768 and 1440px in Bangla and English. The changed FAQ answers matched their structured data, the solar badge and navigation worked, and no visible stray `>` characters or horizontal overflow were found.
- All five hero transitions, including loop wraparound, passed in local Chrome with the three-second display interval retained. Sampled transitions showed no early line movement, blank caption frames or overlapping text; mouse and touch holds, reduced motion and no-JavaScript behavior passed. Across all 15 pages, company links and organization records matched the supplied company URL, and founder records retained the personal profile.
- An initial concurrent run reported an overflow that did not recur in 20 focused reloads; a shared local-server connection reset also did not recur on an isolated server. `git diff --check` and `node --check public/js/site.js` passed. Production, other browsers, physical devices, performance and authenticated LinkedIn access were not tested.

## 2026-11-05 — home caption alignment (`REQ-0019`)

- Local Chrome and independent checks sampled caption bounds and side-line alignment through crossfades in Bangla and English at widths from 280 to 1440px. No text clipping or horizontal overflow was observed; representative phone and desktop screenshots were inspected.
- A detected jump in side-line expansion was fixed; frame-by-frame checks confirmed smooth sampled expansion and shrink. Mouse hover and touch holds, reduced motion, disabled JavaScript and skipping failed slideshow images passed local checks. All 15 routes loaded at 390 and 1440px with navigation and local runtime checks passing on rerun.
- One concurrent local route run returned transient 404s for concrete images; the files existed and subsequent checks returned 200. The cause was not determined. `git diff --check` and `node --check public/js/site.js` passed. Production, other browsers, physical devices and performance were not tested.

## 2026-11-05 — home caption lines and holds (`REQ-0018`)

- Local Chrome checks covered all five captions in both languages at widths from 280 to 1440px; lines remained visible, text fit and no document overflow was detected. Independent checks covered 320, 390, 768 and 1440px in both languages.
- Mouse hover froze and resumed a crossfade; touch hold and release on the image and caption, touch cancellation, simulated visibility changes, remaining display time and reduced motion passed independent checks. All 15 routes loaded at 390 and 1440px; navigation, back, local HTTP and page-error checks passed.
- A separate local Chrome check confirmed that the caption width transition and image fade both freeze during hover and resume afterward.
- `git diff --check` and `node --check public/js/site.js` passed. Production, other browsers, physical devices and performance were not tested. The repository has no lint, typecheck, unit-test suite or build command.

## 2026-11-03 — hero stacking and shared frame glow (`REQ-0017`)

- Local Chrome checks covered all nine affected routes at 320, 390, 768, and 1440px in light and dark themes: requested shadows, image loading, card navigation, and document overflow passed. The independent verifier checked 352 affected instances and clicked menu and card links.
- The hero and open mobile menu were checked after 23 actual slideshow transitions, reaching image layer 24; navigation remained clickable. Both languages and reduced motion were included in the hero checks. All 15 routes loaded at 390 and 1440px, with navigation and back/forward checks passing.
- `git diff --check` and `node --check public/js/site.js` passed. A parallel local-server run had connection resets; sequential reruns passed. Production, other browsers, and performance were not tested. No repository lint, typecheck, unit-test suite, or build command exists.

## 2026-11-03 — enquiry fallback and image alternatives (`REQ-0016`)

- Local Chrome checks at phone and desktop widths passed with JavaScript disabled, delayed, blocked, and working. The fallback remains visible until the submit handler is ready; phone and WhatsApp links remain available. Bilingual messaging, light/dark error styling, and no horizontal overflow were checked.
- Across all 15 routes, 35 informative image instances switched between Bangla and English alternatives. All nine service selections in both languages, invalid fields, Bangla digits, message preview, copy and edit passed. Independent verification confirmed the fallback, language persistence, safe preview and no sample enquiry values in browser network requests.
- `git diff --check` and `node --check public/js/site.js` passed. No WhatsApp message was sent, and production was not tested. The repository has no lint, typecheck, unit-test suite, or build command.

## 2026-11-03 — search and sharing metadata (`REQ-0015`)

- Parsed all 15 page heads: unique titles and descriptions, canonical and Open Graph URLs, Twitter cards, JSON-LD, founder and organization links, and sitemap entries passed. The five project dates match 2026-11-02. Page bodies match `HEAD` and local image paths resolve.
- Forty-five local crawler-style GETs passed. Independent review checked 458 root-absolute references and the Vercel headers schema subsection and host matcher. Live Vercel edge behavior and social previews remain unverified until deployment.
- Local Chrome at 390px and 1440px loaded all 15 routes and images; language persistence, project navigation, enquiry validation, and WhatsApp preview passed, with no observed console, page, or local HTTP errors. `git diff --check` and JavaScript syntax checks passed. No repository lint, typecheck, unit-test suite, or build command exists.

## 2026-11-02 — responsive layout (`REQ-0014`)

- Local Chrome/Playwright checks covered 15 routes in Bangla and English at 17 viewport widths from 280px to 1920px, after fonts loaded: no document-level horizontal overflow. At 280px the contact form and its message preview also fit, including a long unbroken message.
- Language persistence, legacy redirects, project back/forward navigation, the mobile menu, form validation and WhatsApp preview passed. The independent verifier checked all five home captions through transitions in both languages at 320, 521, 861, 1024, 1101 and 1440px; no sampled text clipping remained. Local page-error and failed-request checks showed none.
- `git diff --check` and `node --check public/js/site.js` passed. No repository lint, typecheck, test suite, or build command exists. Production, every browser/device, and a comprehensive security audit were not tested.

## 2026-11-02 — project image refresh (`REQ-0013`)

- Served `public/` locally with `python3 -m http.server 8765 --directory public --bind 127.0.0.1`. A temporary Playwright Core and Chrome check loaded the six detail pages and the projects listing at 1440px and 390px. All main images decoded; gallery counts were 3, 8, 0, 0, 2, and 1 for design, concrete, assessment, interior, solar, and fire respectively. Banners measured 16:9, galleries measured 4:3, six listing links and two actions per detail page were present, and no horizontal overflow was detected. Concrete gallery screenshots were visually inspected at both widths.
- A Python HTML parser checked root-relative image `src` paths across `public/`: zero missing files. HTTP requests returned 200 for the listing, six detail routes, and the contact route with `service=3`. `git diff --check` passed.
- The first check using an old Playwright installation failed due to browser-driver incompatibility; the check was rerun successfully with Playwright Core installed under `/tmp`. Individual links were not clicked and production was not tested. No project test, lint, or build script exists.

Cycle: `C1`
Session: 2026-10-27
eval_gate_status: not applicable (no release candidate, Gate 2 not open)

## Executed

| Check | Command | Result |
|---|---|---|
| Repository inventory | `ls`, `find`, `du`, `file`, `sips` | Pass as inspection only. One HTML file, nine images, no `img/projects/`. |
| Version control | `git status -sb` | Not a git repository. This is a fact, not a failed test. |
| Logo alpha | Python PIL sample of `img/logo.png` | RGBA. Corners are transparent. A white logo plate matches the asset. |
| Source read | `index.html`, protocol, `CLAUDE.md`, `AGENTS.md` | Completed. Findings are in `REQUIREMENTS.md` and `RISKS.md`. |

## Not executed

| Check | Reason |
|---|---|
| Browser walkthrough of routing, language, form, copy, placeholders, dark scheme, narrow layout | No implementation was authorized, and behavior was not exercised. `REQ-0012` covers this after approval. |
| typecheck, lint, unit tests, build | No `package.json` and no scripts. |
| Accessibility audit with a tool | Not run. |
| Security audit or dependency audit | No dependencies are declared. Google Fonts is a runtime link (`RISK-0004`). |

Do not read the 2026-10-27 section as evidence that the page works in a browser.

## 2026-10-28 — public site

Local browser checks on a static server rooted at `public/`:

- Nine routes opened. Bangla is the default. English shows the English address and form labels.
- Contact form prepared a `https://wa.me/8801814116677` message for a valid name and mobile number. It does not store the message.
- Footer and contact icons point at Facebook, the founder LinkedIn profile, and `https://www.youtube.com/@BuildSafe-EC`, each with `target="_blank"` and `rel="noopener"`.
- At a 390px width, the contact page and home page did not scroll sideways.
- JSON-LD on the pages parses. `postalCode` is `1205`.
- No typecheck, lint, unit test, or build script exists, so none was run.
- The live host `https://buildsafe.com.bd/` was still the older single page when last checked. This repo has not been deployed.

## 2026-10-28 — language flash

Local browser checks on a static server rooted at `public/`:

- With `bs-lang` set to `en`, reloading `/contact/?service=3` showed **Concrete Mix Design**. The Bangla select was `display: none`.
- Switching to Bangla showed **কংক্রিট মিক্স ডিজাইন** and kept value `3`. Switching back showed the English label again.
- A valid enquiry prepared a WhatsApp message whose service line matched the visible menu in each language.
- `node --check` on `public/js/site.js` passed. No typecheck, lint, unit test, or build script exists.
- Security review of this diff found no exploitable issue. The site has no backend, auth, or package manifest.

## 2026-10-28 — nav label width

Local browser checks on a static server rooted at `public/`:

- Bangla header widths followed the words. The gaps between links were 4px.
- English **About** was 71px, not the width of **আমাদের সম্পর্কে**. The gaps were 4px.
- Hover on **Services** used the soft background at the width of that word plus padding.
- Reload with English saved showed English. `/#services` opened `/services/`.
- All nine routes returned 200. A valid contact enquiry prepared a WhatsApp message for Concrete Mix Design.
- At 390px the menu was one language per full-width row, and the page did not scroll sideways.
- No typecheck, lint, unit test, or build script exists, so none was run.

## 2026-10-28 — footer Information column

Local browser checks on a static server rooted at `public/`:

- At 1280px the columns were brand, Pages, Information, and Contact. Information listed Terms, Privacy, Cookies, and FAQ once.
- The footer address computed to 15px, weight 400, and the same color as the phone line. The contact-page office card stayed 16px and weight 600.
- At 761px the four columns stayed in one row. At 760px and at 390px, Pages and Information shared a row and Contact was full width underneath.
- Checked all nine routes in Bangla and English. The matching Information link kept `aria-current="page"` on Terms, Privacy, Cookies, and FAQ.
- `/#services`, `/#about`, `/#projects`, and `/#contact` opened those routes. A short name was rejected. A valid enquiry, including Bangla digits, prepared `https://wa.me/8801814116677`.
- The only 404 responses were the absent optional files `public/img/projects/p1.jpg` through `p6.jpg`. Placeholders stayed. No page errors.
- No typecheck, lint, unit test, or build script exists, so none was run.

## 2026-10-28 — nav link order

Local browser checks on a static server rooted at `public/`:

- All nine routes, in Bangla and English, showed Home, About, Services, Projects, Contact in the header and in the footer Pages list.
- At 1280px those links ran left to right in that order. At 390px the open phone menu ran them top to bottom in that order.
- `/about/` marked About. `/services/` marked Services. Legal pages did not mark a header link.
- The home button still said আমাদের সেবাসমূহ / Our services.
- No typecheck, lint, unit test, or build script exists, so none was run.

## 2026-10-28 — office footer and share picture

Local browser checks on a static server rooted at `public/`, after the footer change and again after the picture split:

- All nine routes, in Bangla and English, at 1280px and 390px, showed Pages as Home, About, Services, and Projects. Information showed FAQ and Contact. Office showed the phone, `contact.buildsafe@gmail.com`, and the Dilara Tower address.
- The contact page email card used `mailto:contact.buildsafe@gmail.com`. Structured data on every page included that email.
- The slogan was “Partner with build safe to turn your vision into reality”. The words vision and reality computed to `rgb(227, 146, 114)` and weight 600 in the dark footer.
- On every page, `og:image`, `twitter:image`, and the structured-data image were `https://buildsafe.com.bd/img/meta-logo.jpg`, with width 2000, height 2000, and type `image/jpeg`. The structured-data logo was `https://buildsafe.com.bd/img/logo.png`.
- The header image was `/img/logo.png` and had a visible width. The home photo was `/img/hero.jpg` with the engineers alt text. Other pages had no hero image. The favicon and apple-touch icon were unchanged.
- `meta-logo.jpg` measured 2000 by 2000 JPEG and returned HTTP 200. `public/sitemap.xml` still listed nine page URLs and no images.
- The only 404 responses were the absent optional files `public/img/projects/p1.jpg` through `p6.jpg`.
- No typecheck, lint, unit test, or build script exists, so none was run.

## 2026-10-29 — FAQ list and contact copy

Local browser checks on a static server rooted at `public/`:

- The FAQ title stayed `প্রশ্নোত্তর | Build Safe Engineering & Consultancy`. The visible heading was “বাড়ি নির্মাণের আগে যে প্রশ্ন আসে” in Bangla and “Frequently asked questions” in English. The old short-answers line was absent.
- Fifteen visible questions matched the Bangla `FAQPage` structured data, including the answers. The first item had 20px of padding and an 8px gap before the answer. The heading weight was 700.
- The home page still had three `.q` items. The global section padding rule was still present, and the FAQ items were not `section` elements.
- At 1280px the footer row kept space between the copyright and the slogan “Partner with BUILD SAFE to turn your vision into reality”. At 390px both lines were centered.
- The contact email matched the phone number at 19px and weight 600, kept `mailto:contact.buildsafe@gmail.com`, and copied that address. The notice sat 16px from the right edge.
- No unexpected failed requests. The only known 404s remain the absent optional files `public/img/projects/p1.jpg` through `p6.jpg`.
- No typecheck, lint, unit test, or build script exists, so none was run.

## 2026-10-29 — FAQ in the header and Pages

Local browser checks on a static server rooted at `public/`:

- All nine routes, in Bangla and English, showed Home, About, Services, Projects, FAQ, Contact in the header and in Pages. Footer headings were Pages and Office. There was no Information column.
- At 1280px the footer was three columns. At 760px and at 390px the brand, Pages, and Office each filled the row.
- At 390px the open phone menu listed those six links top to bottom. `/faq/` marked FAQ in the header and on the Pages link. `/contact/` marked Contact the same way. Legal pages did not mark a header link.
- Facebook, LinkedIn, and YouTube stayed inside the office column.
- The only 404 responses were the absent optional files `public/img/projects/p1.jpg` through `p6.jpg`. No page errors.
- No typecheck, lint, unit test, or build script exists, so none was run. An independent file check matched the same header, Pages list, `aria-current` placement, and three-column footer.

## 2026-10-29 — consult, consulting, and consultancy

A local static server rooted at `public/` returned the nine pages. None of the served HTML contained the previous guidance noun or verb. The planned English lines were present, including “We consult based only on test reports”, “Material Selection Consultancy” with option value `8`, “This is not legal consulting”, and “Independent consulting”. Bangla spans beside those lines were unchanged. The FAQ structured data stayed Bangla. A repository search found none of that previous wording. No browser tool was available for this check. No typecheck, lint, unit test, or build script exists, so none was run.

## 2026-10-29 — project cards and detail pages

A local static server rooted at `public/` and a browser check covered all 15 routes.

- The six project cards loaded their posters. Interior and fire no longer showed a dashed placeholder. At desktop width the grid was three columns. At 390px it was one column.
- `/#projects` opened `/projects/`. Each detail page showed its facts and its pictures. Contact links were service 1, 2, 3, 5, 6, and 7.
- `/contact/?service=7` selected Solar System Design & Installation. A short number was rejected. A valid number prepared a WhatsApp link to `8801814116677` and did not store the message.
- The FAQ page still had 15 questions, including “সোলার সিস্টেমে কী থাকে?”. No project image request failed. The nine project JPEGs had no EXIF and no GPS data.
- No typecheck, lint, unit test, or build script exists, so none was run.

## 2026-10-30 — home photo cycle and project pictures

A local static server rooted at `public/` and a browser check:

- All 15 HTML routes returned HTTP 200. Every local image, stylesheet, script, and font named by those pages was on disk. The home page had no broken images and no failed resource requests.
- The home frame ratio was 1.5. The cycle class was `hero-cycle`, and the visible picture started as `hero.jpg`. English and Bangla both rendered. An earlier check in the same session, at 1280px, placed the extra frame height above the caption, and at 390px the frame stayed one column.
- The projects intro matched the showcase line in both languages. The concrete card was `project-1-card.jpeg` at 1600×1200, and its box ratio was 1.333.
- The concrete detail banner was `project-1-poster.png`. The facts list computed to `display: none`. The six gallery pictures matched their own ratios. The card collage was not on that page.
- A 3-digit phone number kept the contact form and showed the valid-number message. A valid number hid the form and set a link to `https://wa.me/8801814116677`. `/#projects` opened `/projects/`.
- No page errors were recorded on the concrete detail page or the contact page. No typecheck, lint, unit test, or build script exists, so none was run. An independent file check matched the hero markup, the six detail pages, and the asset list. Page-load timing was not measured.

## 2026-10-30 — home crossfade, captions, and card pictures

Pull request 11.

A local static server rooted at `public/` and a browser check:

- `node --check public/js/site.js` passed. No typecheck, lint, unit test, or build script exists, so none was run.
- All 15 HTML routes returned HTTP 200. The only 404s were two guessed project paths that are not links on the site.
- At 1280px the home frame ratio was 1.333. During the crossfade, picture opacity and the matching caption opacity stayed paired, and each pair summed to 1. The diamond row and the caption differed by 1px. The frame glow was the brown and grey shadow.
- English showed the visible caption and hid the Bangla line. At 390px the hero was one column, the frame ratio stayed 1.333, and the caption side rules were hidden.
- Reduced motion kept `hero.jpg` and the first caption at opacity 1, with the transition duration at 0s.
- `/#projects` opened `/projects/`. Interior, assessment, and fire cards were 1024×768 with a box ratio of 1.333. Their detail banners stayed `project-5-poster.jpeg`, `project-3-poster.jpeg`, and `project-6-poster.jpeg`, each 1600×900.
- A 3-digit phone number kept the contact form and showed the phone error. A valid number hid the form and set a WhatsApp link to `https://wa.me/8801814116677` that included the name.
- An independent file check matched the caption lines, the fade classes, and the three card sources. Page-load timing was not measured.

## 2026-10-30 — caption rules, slogans, and detail spacing

Pull request 12.

A local static server rooted at `public/` and a browser check:

- `node --check public/js/site.js` passed. No typecheck, lint, unit test, or build script exists, so none was run.
- All 15 HTML routes returned HTTP 200. No image request on the checked pages failed.
- In Bangla the caption cell matched the visible line, and the side gaps were equal. Switching to English eased the cell toward the English line, and the side gaps stayed equal. The picture opacity sum stayed 1.
- At 390px the hero was one column, the frame ratio was 1.333, and the side rules were hidden.
- On the fire detail page, the space above the buttons and the space below them were both 28px. The banner stayed `project-6-poster.jpeg`.
- A 3-digit phone number kept the contact form. A valid number hid the form and set a WhatsApp link to `https://wa.me/8801814116677` that included the name.
- An independent file check matched the four slogans, the caption-width rules, and the button spacing. Page-load timing was not measured. The live Vercel and Cloudflare headers were not opened.

## 2026-10-30 — home pictures

Pull request 13.

A local static server rooted at `public/` and a browser check:

- `node --check public/js/site.js` passed. No typecheck, lint, unit test, or build script exists, so none was run.
- All 15 HTML routes returned HTTP 200. The five new home pictures returned 200. `hero.jpg` and `hero-2.png` through `hero-4.png` returned 404, and the home page did not request them.
- At 1280px the frame ratio was 1.333 and `object-fit` was cover. Each caption changed with its picture. Natural sizes were 1024×678, then four files at 1024×768.
- At 390px the hero was one column, the frame ratio was 1.333, and the side rules were hidden. Reduced motion kept `hero-1.jpeg` and the office caption at opacity 1.
- `/#projects` opened `/projects/`. The design banner stayed `hero-1.png` at 2560×1440. Project cards had no broken pictures.
- A 3-digit phone number kept the contact form. A valid number hid the form and set a WhatsApp link to `https://wa.me/8801814116677` that included the name.
- An independent file check matched the five sources, the deletions, and the design banner. Page-load timing was not measured. The live Vercel and Cloudflare headers were not opened.

## 2026-10-30 — category wording on project pages

Pull request 14.

A local static server rooted at `public/` and a browser check:

- No typecheck, lint, unit test, or build script exists, so none was run.
- Both languages were opened on all six detail pages. Each opening paragraph and the three picture lines matched the category wording. `সব প্রকল্প` / `All projects` stayed.
- The projects index, services, and FAQ were left unchanged. Page-load timing was not measured.

## 2026-10-31 — Cloudflare asset config

Pull request 15.

- `wrangler.toml` parses. The Worker name is `divine-dream-20ba`. The asset directory is `./public`. There is no token, route, or Worker script.
- `public/index.html` and `public/about/index.html` exist. `public/404.html` does not. A missing page is an empty 404.
- No typecheck, lint, unit test, or build script exists, so none was run. `node --check public/js/site.js` was not required because that file did not change.
- An independent file check matched the config. A security review of this branch found no issue. A browser cannot show the trailing-slash rule or the empty 404 until the Worker is connected. The live site was not changed.

## 2026-10-31 — Cloudflare Git connection

Pull request 16.

- The Worker settings showed the brochure repository, branch `main`, build command None, deploy command `npx wrangler deploy`, and root directory `/`. Preview builds were off. No build variables were set.
- The Deployments tab still showed manual upload `e6b06886` at 100% traffic. No Cloudflare check existed on the commit already on `main`.
- A security review of the connection found no blocking issue. The API token is not in the repo. No typecheck, lint, unit test, or build script exists, so none was run. The live pages had not changed.
