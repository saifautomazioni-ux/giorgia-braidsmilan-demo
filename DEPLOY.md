# Deploy Giorgia Braids — guida semplicissima

## ⓵ Crea una NUOVA repo su GitHub

1. Vai su https://github.com/new
2. **Repository name:** `giorgia-braids` (o quello che vuoi)
3. **Public** o **Private** — come preferisci
4. **NON** spuntare "Add a README" né "Add .gitignore" né "Add license"
   (il nostro zip ne ha già di pronti)
5. Clicca **Create repository**

## ⓶ Carica i file nello zip

Dopo aver creato il repo, GitHub ti mostrerà una pagina vuota. In alto vedrai un link:

> **uploading an existing file**

Clicca su quello. Poi:

1. Apri lo zip che hai scaricato sul tuo computer
2. Seleziona **tutto** quello che c'è dentro:
   - `index.html`
   - cartella `css/`
   - cartella `js/`
   - cartella `assets/`
   - `vercel.json`
   - `package.json`
   - `README.md`
   - `robots.txt`
   - `.gitignore`
3. Trascinali tutti insieme sulla pagina di GitHub
4. Scorri in fondo, scrivi `Initial site` come commit message
5. Clicca **Commit changes**

## ⓷ Connetti Vercel

1. Vai su https://vercel.com/new
2. Clicca **Import** sul repo `giorgia-braids` appena creato
3. Nella pagina **Configure Project**:
   - **Framework Preset:** scegli **`Other`**
   - **Build Command:** lascia vuoto
   - **Output Directory:** lascia vuoto
   - **Install Command:** lascia vuoto
4. Clicca **Deploy**

Aspetta 30 secondi. Avrai il sito live su `giorgia-braids-xxx.vercel.app` 🎉

## ⓸ (Prima di andare online davvero)

Apri `js/main.js` su GitHub, clicca l'icona della **matita** ✏️ in alto a destra, cerca la riga:

```js
const WHATSAPP_NUMBER = '';
```

Mettici il tuo numero **senza + e senza spazi**, esempio:

```js
const WHATSAPP_NUMBER = '393331234567';
```

Scrolla giù, **Commit changes**. Vercel ridepleya automaticamente in 30 secondi.

## ⓹ (Opzionale) Dominio custom

Vercel dashboard → progetto → **Settings → Domains** → aggiungi `giorgiabraids.it` (o quello che hai).

---

### Aiuto

Se qualcosa non funziona, mandami uno screenshot della schermata che vedi e ti dico io cosa fare.
