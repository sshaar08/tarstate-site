# CLAUDE.md

Guidance for AI coding agents working in this repository.

## Project

Static marketing site for Tar State Mobile Tech — plain **HTML + CSS**, no framework, no build step, no JS. Deployed via GitHub Pages to `tarstate.worklabshq.com`.

## Key facts

- Entry point: `index.html` (single page, section anchors: `#services`, `#detailing`, `#contact`).
- All styling: `css/style.css`. Theme uses CSS variables in `:root` (Carolina blue + white palette; `--primary: #4b9cd3`).
- `CNAME` — must stay `tarstate.worklabshq.com`.
- `.nojekyll` — required; do not delete (Pages build fails without it).
- Deploys on push to `main` via GitHub Pages ("Deploy from a branch").

## Business details (keep in sync in the page)

- Phone: (336) 601-7969 → `tel:+13366017969`
- Email: tarstatemobilemechanic@gmail.com
- Service area: Guilford & Alamance County
- Hours: Mon–Fri 9am–5pm; weekends by appointment only
- Brakes note: standard systems only, **no ESP/electronic stability systems**

## Conventions

- Keep it dependency-free. Do not add a build tool, package manager, or framework unless explicitly requested.
- Edit content directly in `index.html`; keep semantic HTML and existing section ids.
- Reuse existing CSS classes/variables; avoid inline styles except trivial one-offs.
- Maintain responsive behavior (mobile breakpoint at `max-width: 768px`).
- Accessibility: interactive elements are real `<a>`/`<button>`; links have descriptive text.

## Do not

- Do not rename `main` (Pages source is pinned to it).
- Do not remove/edit `CNAME` or `.nojekyll`.
- Do not commit `.DS_Store` (gitignored).

## Verify changes

```bash
python3 -m http.server 8081   # preview at http://localhost:8081
```
