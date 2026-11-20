# Escape the City

- Deze map bevat de React/Vite-spelersapp, het teamdashboard en de Supabase-migraties voor Het Geheim van de Moerasdraak.
- Gebruik de Node-versie in `.nvmrc` en installeer via `npm ci`. Controleer wijzigingen met `npm run lint`, `npm test` en `npm run build`.
- Gebruik `import.meta.env.BASE_URL` voor publieke assets in TypeScript. Het basispad is configureerbaar met `VITE_PUBLIC_BASE_URL`. Bij een nieuwe release moeten de versies in `package.json`, `package-lock.json` en `public/manifest.webmanifest` overeenkomen.
- Houd scoreberekening en toegangscontrole server-side in de bestaande Supabase-RPC's. Geef browserrollen geen directe toegang tot tabellen in `city_game`. Houd de bestaande read-only projecties voor het dashboard onder RLS.
- Commit alleen publieke Supabase-configuratie. Houd geheime sleutels, databasewachtwoorden, lokale exports en spelergegevens buiten Git.
