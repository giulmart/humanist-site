# Humanist AI — humanist.works

Version 1 of the robots-as-a-service website for Humanist AI. One static page, no build step, no dependencies beyond Google Fonts (Inter).

## Files

- `index.html` — the whole site (HTML, CSS and a few lines of JS in one file)
- `README.md` — this file

## Deploy on Vercel

1. Push this repo to GitHub (`giulmart/humanist-site`).
2. In Vercel: **Add New → Project → Import** the repo. Framework preset: **Other**. Root directory: `./`. No build command, no output directory. Deploy.
3. In the Vercel project: **Settings → Domains → Add** `humanist.works` and accept the `www.humanist.works` suggestion. Vercel shows the exact records to add.

## DNS at Spaceship (keep Spaceship nameservers)

Domain Manager → humanist.works → **Advanced DNS**. Add:

| Type  | Host | Value                                  |
|-------|------|----------------------------------------|
| A     | @    | `76.76.21.21` (or the IP Vercel shows) |
| CNAME | www  | the project CNAME Vercel shows (looks like `xxxx.vercel-dns-017.com`) |

Do not change the nameservers. Email (MX) records for info@humanist.works go in the same Advanced DNS panel later.

## Palette ("Werkplaats")

| Role            | Hex       |
|-----------------|-----------|
| Background      | `#F4F2EE` |
| Background 2    | `#ECEAE5` |
| Ink (text)      | `#1B1D21` |
| Ink 2           | `#4A4F57` |
| Aluminium line  | `#C9CDD3` |
| Aluminium fill  | `#E6E8EC` |
| Accent          | `#FF5A1F` |
| Accent (hover)  | `#D9430C` |
| Dark section    | `#0F1114` |

All colours are CSS variables at the top of `index.html`.

## Copy to confirm before launch

The copy is a first draft. These statements are promises and need to be true before the site goes live:

- "Live in days" and "Site survey, install and training included"
- "Four weeks, one robot, one task, a fixed fee" (pilot format)
- "Cancel monthly" and "No lock-in"
- "We reply within one working day"
- `info@humanist.works` must exist (set up mail on the domain first)
- Use cases marked "Pilots open" vs "Exploring"

## Editing

Edit `index.html`, commit, push. Vercel redeploys automatically on every push to `main`.
