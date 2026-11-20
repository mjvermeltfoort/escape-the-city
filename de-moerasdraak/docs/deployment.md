# Deployen

`npm run build` bouwt de app en het dashboard naar `dist/`. Publiceer die map op een statische host met HTTPS. De spelersapp gebruikt hash-routes en het dashboard opent via `dashboard.html`.

Standaard draait de build vanaf `/`. Stel `VITE_PUBLIC_BASE_URL` in als je de app onder een subpad host, bijvoorbeeld `/de-moerasdraak/`.

## GitHub Pages

1. Selecteer GitHub Actions onder **Settings → Pages → Source** in de nieuwe repository.
2. Stel voor online synchronisatie de repositoryvariabelen `SUPABASE_URL` en `SUPABASE_PUBLISHABLE_KEY` in voor het aparte Supabase-project. Zie [Supabase instellen](supabase-setup.md).
3. Een push naar `main` met wijzigingen aan De Moerasdraak, de startpagina of de deployworkflow start de publicatie. Je kunt **Deploy De Moerasdraak to GitHub Pages** ook handmatig starten onder **Actions**, bijvoorbeeld na een wijziging aan de repositoryvariabelen.

De workflow bepaalt het basispad vanuit de Pages-instellingen. De startpagina verwijst door naar `de-moerasdraak/` binnen de site.
