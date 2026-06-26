# FORMA Report Hub
**report.formacorps.com** — Client-facing project report & pitch pages

## URL Structure
```
report.formacorps.com/[TYPE]-[LOCATION]-[YY]
```

## Active Projects
| URL | Project | Status |
|-----|---------|--------|
| /reno-wari79-69 | 19/31 ซอยเลียบวารี 79 Renovation Pitch | ✅ Live |

## Adding New Projects
1. Create folder: `/[type]-[location]-[yy]/`
2. Add `index.html` inside
3. Add route in `vercel.json`
4. Push to main → auto deploy

## Naming Convention
- `reno` = Renovation
- `insp` = Inspection  
- `rep` = Structural Repair
- `roof` = Roofing
- `civil` = Civil Works

## Tech Stack
- Static HTML (no framework)
- Vercel hosting
- Custom domain: formacorps.com (Hostinger DNS)
