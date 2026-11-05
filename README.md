# Tar State Mobile Tech — tarstate.worklabshq.com

Mobile auto repair, maintenance, and detailing site for **Tar State Mobile Tech**, serving Guilford & Alamance County, NC.

Static site (plain HTML + CSS), hosted on **GitHub Pages** at **[tarstate.worklabshq.com](https://tarstate.worklabshq.com)**.

## Services

- **Repairs & Maintenance** — brakes (standard systems only, no ESP), coolant/radiator & power steering flushes, battery, bulbs, wipers, tire rotation, audio/head-unit upgrades, code reading (scan tool pending).
- **Detailing** — full car wash, tire shine & rim cleaning, interior shine.

## Structure

```
.
├── index.html      # Single-page site
├── css/style.css   # All styles (Carolina blue + white theme)
├── CNAME           # GitHub Pages custom domain
├── .nojekyll       # Bypass Jekyll processing (plain static files)
└── .gitignore
```

## Local preview

No build step. Serve the folder:

```bash
python3 -m http.server 8081
# then open http://localhost:8081
```

## Contact info (in page)

- Phone: (336) 601-7969
- Email: tarstatemobilemechanic@gmail.com
- Hours: Mon–Fri 9am–5pm; weekends by appointment only

## Deploy

Pushing to `main` triggers a GitHub Pages build automatically.

- Repo → **Settings → Pages**
- Source: **Deploy from a branch** → `main` → `/ (root)`
- Custom domain: `tarstate.worklabshq.com` (handled by `CNAME` file)

## DNS (Cloudflare — record set to *DNS only / grey cloud*)

| Type | Name | Content |
|------|------|---------|
| CNAME | `tarstate` | `sshaar08.github.io` |

## Editing

- Content lives in `index.html`.
- Colors are CSS variables in `css/style.css` under `:root` (Carolina blue `--primary: #4b9cd3`, white backgrounds).
