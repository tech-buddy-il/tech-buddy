# Tech Buddy

Website for **Tech Buddy (טק באדיז)** — a volunteer network that connects Israeli nonprofits (עמותות) with experienced tech professionals for accurate, fast, direct technology advice. "Always available, and no question is too small."

The site is Hebrew-only (RTL) and uses the visual system from [code-left-lp](https://github.com/usemojo/code-left-lp): ivory/celadon paper aesthetic, Newsreader + Inter + Plus Jakarta Sans + IBM Plex Mono, polaroid photos, sticker cards, hand-drawn SVG accents.

## Site structure

| Path | Page |
|------|------|
| `/` (`index.html`) | Tech Buddy homepage — hero, what we can/can't help with, team, workshop promo, request form, contact popup |
| `/workshop/` | **הסדנה** — the AI Buddy workshop landing page (process-automation workshop with AI Agents for nonprofits) |

Everything is plain static HTML — one self-contained file per page (inline CSS + JS), no build step.

## Local preview

```bash
npx --yes serve .
```

Then open `http://localhost:3000` (homepage) and `http://localhost:3000/workshop/`.

## Project layout

| File | Role |
|------|------|
| `index.html` | Tech Buddy homepage (Hebrew, RTL) |
| `assets/` | Tech Buddy logos (placeholders) + `assets/team/` portrait placeholders |
| `workshop/` | AI Buddy workshop LP with its own `assets/` and `llms*.txt` |
| `llms.txt` / `llms-he.txt` | Short LLM-oriented site summaries |
| `robots.txt` | Crawler rules |

## Forms

All forms submit to the Mojo forms API (`api.usemojo.ai`), same pattern as code-left-lp. Status:

| Form | Mojo form ID | Status |
|------|--------------|--------|
| Main request form (homepage `#cta`) | `6aa92a48e6a9d3020ff8e2d2` (v1) | ✅ wired |
| Workshop form (`/workshop/`) | `6a68ea2d872e217f8d98f5d8` (v3) | ✅ wired |
| «צור קשר» popup (homepage) | `6aa92a48e6a9d3020ff8e2d2` (v1, same as main form) | ✅ wired |

Project ID for all: `694318737276d03eef9a0505`. The popup asks the same questions as the main form and submits to the same Mojo form. Answer keys sent: `name`, `work_email`, `phone`, `org_name`, `org_website`, `org_revenue`, `org_employees`, `why`.

## Team images

`assets/team/*.svg` are placeholders. Final images are generated portraits following the AI Buddy visual style (originals + generation prompt provided separately). See [assets/team/README.md](assets/team/README.md) for the swap instructions.

## Still to wire

- Real team images (generated from originals + prompt)
- Final Tech Buddy logo / OG image (text-based SVG placeholders for now)
- LinkedIn + Facebook page URLs in the footer (currently `#`)
- Domain + deploy target; `git init` (the `.git` folder is a broken stub)

## Source design

Visual system adapted from [code-left-lp](https://github.com/usemojo/code-left-lp) (`ai-buddy` page). Content migrated from the previous WordPress site.
