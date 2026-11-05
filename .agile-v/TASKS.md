# TASKS

## 2026-11-05 — About video and vision

- `REQ-0022`: See `REQUIREMENTS.md` and `VALIDATION_SUMMARY.md`. The user authorized branch push, PR and squash merge subject to checks. Verify remote status and deployment separately.

## 2026-11-05 — hero, company links and page copy

- `REQ-0020` and `REQ-0021`: See `REQUIREMENTS.md` and `VALIDATION_SUMMARY.md`. The user authorized branch push, PR and squash merge subject to checks. Verify remote status and deployment separately.

## 2026-11-05 — home caption alignment

- `REQ-0019`: See `REQUIREMENTS.md` and `VALIDATION_SUMMARY.md`. The user authorized branch push, PR and squash merge subject to checks. Verify remote status and deployment separately.

## 2026-11-05 — home caption lines and holds

- `REQ-0018`: See `REQUIREMENTS.md` and `VALIDATION_SUMMARY.md`. The user authorized branch push, PR and squash merge subject to checks. Verify remote status and deployment separately.

## 2026-11-03 — hero stacking and frame glow

- `REQ-0017`: See `REQUIREMENTS.md` and `VALIDATION_SUMMARY.md`. The user authorized branch push, a pull request, and squash merge if checks and protections allow. Verify remote status and deployment separately.

## 2026-11-03 — enquiry fallback and image alternatives

- `REQ-0016`: Implemented and independently verified the bilingual form fallback and image alternatives. The user authorized the feature branch, PR, and squash-merge workflow; verify checks and deployments before reporting publication.

## 2026-11-03 — approved metadata update

- `REQ-0015`: Updated the 15 page heads, sitemap dates, and host-specific Vercel header. Page bodies, CSS, and JavaScript are unchanged; local validation and independent review passed.
- The user subsequently authorized the branch/PR/squash-merge workflow. Verify the live header and metadata after deployment. The Cloudflare hostname redirect remains prepared but unapplied.

## 2026-11-02 — approved project image refresh

- `REQ-0013`: Replaced the four detail-page banners and galleries, added shared 4:3 gallery framing, and updated the two listing cards. Local validation is recorded in `VALIDATION_SUMMARY.md`.
- `REQ-0014`: Fixed narrow header, footer, contact and caption layout; local verification is recorded in `VALIDATION_SUMMARY.md`.
- Publication is authorized by the user via feature branch and pull request; verify checks and the merged state before reporting completion.

Cycle: `C1`. No task may start until `GATE-0001` is approved for that task’s requirement IDs.

Recommended order if the full proposed set is approved. Wave 2 waits for Wave 1 because verification has to cover the finished page.

## Wave 1 — page and README

| ID | Requirement | Priority | Work | Files |
|---|---|---|---|---|
| TASK-0001 | REQ-0007 | P1 | Move metadata into `<head>`, set initial `lang="bn"`, add the specified description and a favicon link. Do not invent a canonical URL. | `index.html` |
| TASK-0002 | REQ-0008 | P1 | Keep one-page hash routing when JavaScript runs. Without it, show every section and a `tel:` link. Do not let the form pretend to submit. | `index.html` |
| TASK-0003 | REQ-0009 | P2 | Make the existing dark tokens follow the system preference. Keep the white logo plate. Add no toggle unless the gate says otherwise. | `index.html` |
| TASK-0004 | REQ-0010 | P2 | Apply the alt-text rules. Do not rewrite headings. | `index.html` |
| TASK-0005 | REQ-0011 | P3 | Replace the empty README with the short operating note in REQ-0011. | `README.md` |

`TASK-0001` through `TASK-0004` touch the same file. Do them in the order above, in one pass, so the hash router and the no-JS path are not edited twice.

## Wave 2 — evidence

| ID | Requirement | Priority | Work | Files |
|---|---|---|---|---|
| TASK-0006 | REQ-0012, and REQ-0001–REQ-0006 | P1 | Open the page. Walk nav, both languages, reload, an invalid enquiry, a valid WhatsApp preview, copy, project placeholders, the no-JS path, and light/dark scheme at desktop and narrow widths. Record commands and results. | `.agile-v/VALIDATION_SUMMARY.md` |

## Do not schedule

| Item | Why it is waiting |
|---|---|
| Project photo drop-in | Done for the six posters, the three galleries, the concrete, interior, assessment, and fire cards, and the five home pictures. `hero-1.jpeg` is 1024×678, so the frame still crops a little of each side. Design and solar cards wait until the client supplies new 4:3 files. |
| Canonical URL and social preview image | No production origin in the repo (`RISK-0003`). |
| Enquiry database or email | Changes the architecture. Current design hands the message to WhatsApp. |
| Framework, TypeScript, or bundler | `DEC-0002`. The working page is one HTML file. |
| Git init or deployment | Not requested. |
| Messenger prefilled text | `m.me/buildsafe.ec` has no message parameter. The page already tells the visitor to copy the message. |

## Suggested gate choice

Approve `REQ-0007`, `REQ-0008`, `REQ-0009`, `REQ-0010`, `REQ-0011`, and `REQ-0012` together. That hardens the current site without a new stack.

Rejecting the whole proposed set is also coherent: the baseline page is already a complete brochure, and only browser evidence (`REQ-0012`) would then be worth doing.
