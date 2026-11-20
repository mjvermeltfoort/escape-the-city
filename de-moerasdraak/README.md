# Escape the City · Het Geheim van de Moerasdraak

React-PWA voor het stadsspel in Den Bosch, met gps, offline speelmodus en een teamdashboard. Deze map bevat de app, spelbestanden en Supabase-migraties voor het stadsspel. De code is overgenomen uit `mjvermeltfoort/vriendenweekend-2026` op commit `ea1ccd12f3bb1792d90be092fdaf856d25f09cc0`.

## Lokaal starten

Gebruik Node.js 26.5.0 of hoger binnen de 26.x-reeks. De versie staat in `.nvmrc`.

```bash
cd de-moerasdraak
npm ci
npm run dev
```

Zonder Supabase bewaart de spelersapp het team en de voortgang op het apparaat. Voor teamcodes, synchronisatie en het dashboard heb je een Supabase-project nodig.

## Online spelen en beheren

1. Maak een apart Supabase-project en schakel Anonymous Auth in.
2. Voer alle meegeleverde [migraties](supabase/migrations/) op volgorde uit.
3. Kopieer `.env.example` naar `.env` en vul `VITE_SUPABASE_URL` en `VITE_SUPABASE_ANON_KEY` (de publieke sleutel) in.

Het teamdashboard open je via `dashboard.html` op dezelfde host en onder hetzelfde basispad als de app. Iedereen die de URL kent kan de zichtbare teams beheren. Zie [Supabase instellen](docs/supabase-setup.md) en [Teamdashboard](docs/public-dashboard.md).

## Controleren en publiceren

```bash
npm run lint
npm test
npm run build
npm run preview
```

Zie [Deployen](docs/deployment.md) voor statische hosting en GitHub Pages.
