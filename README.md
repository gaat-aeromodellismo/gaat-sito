# GAAT - sito pilota Cloudflare Pages

## Contenuto
- `index.html`: home responsive e sezioni iniziali.
- `content/news.json`, `content/events.json`: contenuti letti dalla home.
- `admin/`: pannello Decap CMS (configurazione non ancora attiva).

## Anteprima rapida
Pubblicare la cartella `gaat-site` con Cloudflare Pages (Direct Upload) per vedere la home. In alternativa: `python3 -m http.server 8000` dalla cartella e aprire http://localhost:8000.

## Per attivare il CMS
1. Creare un repository GitHub privato o pubblico con questi file.
2. Creare un progetto Cloudflare Pages con integrazione Git, collegato al repository e directory output `/`.
3. In `admin/config.yml`, sostituire `NOME_ACCOUNT/NOME_REPOSITORY` con il repository reale.
4. Configurare un servizio OAuth GitHub per Decap CMS, protetto e con callback corretta; impostare `base_url` al relativo endpoint. Il solo caricamento dei file non rende operativo il login.
5. Autorizzare i soci tramite gli accessi al repository e verificare i permessi minimi.
6. Testare modifica di una notizia e deployment automatico.

**Importante:** non modificare DNS di gaat.it durante questa fase. Non inserire credenziali nel repository. Prima di pubblicare materiale ufficiale, verificare testi, foto, regolamenti e documenti.
