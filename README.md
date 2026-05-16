# Giorgia Braids — Landing Page

Sito statico per **Giorgia Braids**, hair braiding artist a Milano. Funnel di prenotazione interamente via WhatsApp.

Live (una volta deployato): `https://giorgiabraids.vercel.app` (o dominio custom).

---

## ✦ Struttura del progetto

```
.
├── index.html          # Pagina unica — single-page landing
├── css/
│   └── styles.css      # Tutti gli stili (palette, tipografia, responsive)
├── js/
│   └── main.js         # i18n (IT/EN), form, scroll, dock, animazioni
├── assets/             # Immagini ottimizzate
│   ├── logo.png
│   ├── logo-circle.png # Logo ritagliato a cerchio trasparente
│   └── gallery-*.png   # Foto portfolio
├── vercel.json         # Config deploy (cache headers, security headers)
└── README.md
```

## ✦ Sezioni della landing

1. **Hero** — logo, headline script, 3 CTA, social, language toggle IT/EN
2. **Portfolio** — gallery 4/3/2 colonne (desktop/tablet/mobile)
3. **Policy** — megasezione con 3 sottogruppi:
   - 01 · Regole appuntamento (5 regole)
   - 02 · Servizi non disponibili
   - 03 · Gestione treccine (aftercare)
4. **Prenotazione** — form con campi condizionali, genera messaggio WhatsApp
5. **Footer** — logo, nome, social IG/TikTok
6. **Sticky dock mobile** — CTA WhatsApp sempre raggiungibile

## ✦ Funzionalità

- **Bilingue IT/EN** con persistenza in `localStorage`
- **Form di prenotazione** con validazione e generazione automatica del messaggio WhatsApp pre-compilato
- **Reveal on scroll** con IntersectionObserver
- **Mobile-first**, tutti i touch target ≥48px
- **Smooth scroll** in-page tra sezioni
- **Logo come cerchio trasparente** estratto dalla PNG originale

## ✦ Configurazione

Prima del deploy modificare in `js/main.js`:

```js
const WHATSAPP_NUMBER = ''; // numero senza + e senza spazi, es. '393331234567'
```

I link Instagram e TikTok puntano già ai profili reali in `index.html` (hero social row + footer).

## ✦ Deploy su Vercel

### Opzione A — Tramite GitHub (consigliata)

1. Crea una repo GitHub e fai push di questa cartella
2. Vai su [vercel.com/new](https://vercel.com/new)
3. Importa la repo
4. **Framework Preset:** `Other`
5. **Build Command:** _lasciare vuoto o `echo skip`_
6. **Output Directory:** _lasciare vuoto_ (Vercel usa la root)
7. **Install Command:** _lasciare vuoto_
8. Deploy

> ⚠️ Se Vercel chiede "Configure Project" e mostra un framework rilevato, scegli sempre **Other**. Non selezionare Next.js o altri framework.

### Opzione B — Tramite CLI (più rapida)

```bash
npm i -g vercel
vercel        # primo deploy (preview) — quando chiede framework, "other"
vercel --prod # promuove a produzione
```

### Opzione C — Drag & drop

Trascina la cartella (o lo zip) su [vercel.com/new](https://vercel.com/new) e usa "Deploy a static site".

## ✦ Dominio custom

Dal dashboard Vercel → **Settings → Domains** aggiungi il dominio (es. `giorgiabraids.it`) e segui le istruzioni DNS.

## ✦ Test locale

Qualunque server statico:

```bash
# Python
python3 -m http.server 8080

# Node
npx serve .
```

Apri `http://localhost:8080`.

## ✦ Brand

- Palette: charcoal `#1a1815` · greige beige `#EDE4D6` / `#D4C4B0` · brown `#2C2218`
- Type: Cormorant Garamond (display serif) · Sacramento (script) · Inter (body)
- Tono: minimal luxury, italiano elegante

---

© Giorgia Braids · Studio appuntamenti, Milano
