# Vercel Deploy — Tierarzt-Pitch

## Erste Deployment (5 min)

```bash
cd /Users/johannesjaissle/Desktop/02-firma-retter/03-TELEFON-RETTER/sales-kit-2026-05-13/deck-deploy/

# 1. Login bei Vercel (Browser öffnet sich)
npx vercel login

# 2. Erst-Deploy (interaktive Fragen)
npx vercel
# - Set up project? Y
# - Scope: dein Account
# - Link to existing project? N
# - Project name: telefon-retter-tierarzt-pitch
# - Code directory: ./
# - Override settings? N

# 3. Production-Deploy
npx vercel --prod
```

Ergebnis: Public-URL wie `telefon-retter-tierarzt-pitch.vercel.app`. Diese URL in Email-Templates als Link einbauen.

## Updates später

Nach Änderungen am HTML:
```bash
cp ../deck/tierarzt-pitch.html ./index.html
npx vercel --prod
```

## Custom-Domain später (telefon-retter.de oder Sub)

Vercel-Dashboard → Project → Settings → Domains → "pitch.telefon-retter.de" hinzufügen.
DNS-Eintrag bei Hetzner: CNAME `pitch` → `cname.vercel-dns.com`.
