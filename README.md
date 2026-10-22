# Humanist AI — humanist.works

Website for Humanist AI: humanoids as a service. One static page, no build step, no dependencies beyond Google Fonts.

## Files

- `index.html` — the whole site (HTML, CSS and a few lines of JS in one file)
- `assets/hero-humanoid.jpg|webp` — hero render (original humanoid, generated, no third-party IP)
- `assets/band-detail.jpg|webp` — torso crop of the same render for the fleet band
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

## Design system ("Showroom")

Black, steel, aluminium and chrome. Matte surfaces, one chrome gradient for display type and the primary button, no colour accent.

| Role                | Hex / value |
|---------------------|-------------|
| Background          | `#050607` |
| Background 2        | `#0B0D10` |
| Surface             | `#121417` → `#0B0D10` (card gradient) |
| Line                | `#23272D`, hover `#2E333A` |
| Steel (labels)      | `#8E939B` |
| Aluminium           | `#C9CDD3`, light `#E6E8EC` |
| Chrome gradient     | `#F6F7F9` → `#DADDE2` → `#9DA3AB` (display type, primary button) |
| Text                | `#ECEDEF`, secondary `#A6ABB3`, muted `#6E737B` |
| Display font        | Inter Tight 600, tracking -0.045em |
| Body font           | Inter 400/500/600 |
| Label font          | JetBrains Mono 500, 11–12px, tracking 0.14em, uppercase |

All colours are CSS variables at the top of `index.html`.

## Imagery

The hero render is an original humanoid generated for this site (Higgsfield, Nano Banana 2, 896×1200). It is not a Tesla Optimus or any other manufacturer's robot: third-party renders are copyrighted and would suggest an affiliation that does not exist. For higher resolution or more angles, regenerate at 2k/4k with the same prompt (in the project notes) and replace the files in `assets/`.

## Copy to confirm before launch

The copy is a first draft. These statements are promises and need to be true before the site goes live:

- "Installed and run by us", "Install · monitor · maintain"
- "Certified units", "Safety-tested before deployment", "Swap guarantee"
- "One unit, one task, a fixed fee" (pilot format), "Cancel monthly", "No lock-in"
- "We reply within one working day"
- `info@humanist.works` must exist (set up mail on the domain first)
- Use cases marked "Pilots open" vs "Exploring"

## Editing

Edit `index.html`, commit, push. Vercel redeploys automatically on every push to `main`.
