# Cosa mangio — App piano alimentare (PWA)

App installabile per consultare il piano alimentare: scegli il pasto, rispondi
alle domande a scelta multipla e vedi cosa puoi mangiare. Funziona anche offline
una volta installata.

## File contenuti

| File | A cosa serve |
|---|---|
| `index.html` | L'app vera e propria |
| `manifest.webmanifest` | Definisce nome, icone e comportamento da app |
| `sw.js` | Service worker: fa funzionare l'app offline |
| `icon-192.png`, `icon-512.png` | Icone standard |
| `icon-maskable-512.png` | Icona "maskable" (Android adatta la forma) |
| `apple-touch-icon.png` | Icona per iPhone/iPad |
| `favicon-64.png` | Icona della scheda browser |

**Importante:** tutti i file devono stare nella stessa cartella e l'app va
aperta da un indirizzo `https://` (o `http://localhost`). Aprendo `index.html`
con doppio clic dal file system il service worker non si attiva e non diventa
installabile — serve un hosting.

## Pubblicazione con GitHub Pages (consigliato)

1. Crea un nuovo repository su GitHub (es. `piano-alimentare`), pubblico.
2. Carica **tutti** i file di questa cartella nella radice del repo
   (`Add file` → `Upload files` → trascina tutto → `Commit`).
3. Vai su **Settings → Pages**.
4. In *Build and deployment*, alla voce *Source* scegli **Deploy from a branch**.
5. Seleziona il branch `main` e cartella `/ (root)`, poi **Save**.
6. Dopo 1–2 minuti l'app sarà online a un indirizzo tipo:
   `https://<tuo-utente>.github.io/piano-alimentare/`

## Installazione sul telefono

**Android (Chrome):** apri l'indirizzo → menù `⋮` → *Installa app* /
*Aggiungi a schermata Home*.

**iPhone (Safari):** apri l'indirizzo → tasto Condividi → *Aggiungi a Home*.

L'icona comparirà nella schermata home e l'app si aprirà a schermo intero,
senza barra del browser.

## Alternative di hosting

- **Netlify Drop** (netlify.com/drop): trascini la cartella, ottieni un link
  https immediato. Zero configurazione.
- **Cloudflare Pages** / **Vercel**: colleghi il repo GitHub e pubblica in automatico.

## Aggiornare l'app

Se modifichi `index.html`, cambia anche la versione della cache in `sw.js`
(es. `piano-alimentare-v1` → `piano-alimentare-v2`): così i telefoni scaricano
la nuova versione invece di usare quella salvata in cache.

---
Contenuti del piano a cura della Dott.ssa Gotti Gloria — Biologa Nutrizionista.
App a uso personale.
