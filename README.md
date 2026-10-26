# Kana Games – Webseiten

Statische Seiten von Kana Games (HTML/CSS/JS, kein Build-Schritt). Jeder Ordner ist ein eigenes
Vercel-Projekt mit eigener Domain.

| Ordner             | Seite                                     | Domain                      | Vercel-Projekt       |
| ------------------ | ----------------------------------------- | --------------------------- | -------------------- |
| `loesung/`         | Lösungs-App für Kennst Du's? (PWA)        | loesung.kanagames.de        | kana-loesung-site    |
| `amen-nein/`       | AMEN!/NEIN!-Karten für Sag's laut! (PWA)  | amen-nein.kanagames.de      | kana-amen-nein       |
| `erklaervideo-kd/` | Erklärvideo Kennst Du's?                  | play-kennstdus.kanagames.de | kana-video-kennstdus |
| `erklaervideo-sl/` | Erklärvideo Sag's laut!                   | play-sagslaut.kanagames.de  | kana-video-sagslaut  |

## Änderungen veröffentlichen

1. Datei im passenden Ordner bearbeiten (meist `index.html`).
2. Lokal ansehen, z. B. `npx serve loesung` und dann http://localhost:3000 öffnen.
3. Committen und pushen:
   ```
   git add .
   git commit -m "Lösungs-App: Frage 42 korrigiert"
   git push
   ```
4. Vercel baut jedes Projekt, dessen Ordner sich geändert hat, automatisch neu. Nach etwa einer Minute ist
   die Änderung live.

Jedes Vercel-Projekt ist mit diesem Repo verbunden und hat sein **Root Directory** auf den passenden Ordner
gesetzt (Settings → Build and Deployment). Framework Preset: _Other_, kein Build Command.

## Hinweise

- **Service Worker (`loesung/sw.js`):** Wenn sich gecachte Dateien ändern, `CACHE_NAME` hochzählen
  (z. B. `kana-loesungen-v3`), damit installierte Apps die neue Version sicher bekommen.
- **Öffentliches Repo:** Keine Passwörter, API-Keys oder `.env`-Dateien hier ablegen.
- **Domains** liegen bei IONOS (DNS: CNAME auf `cname.vercel-dns.com`) und sind in Vercel unter
  Settings → Domains des jeweiligen Projekts eingetragen.
