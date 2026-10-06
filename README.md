# HTML Playground

Playground di codice live in stile **CodePen** — HTML, CSS e JavaScript in un unico file statico (`index.html`), senza build step, senza dipendenze da installare, senza server richiesto: si apre e basta.

> ⚠️ Progetto in fase **embrionale**: funzionalità di base già presenti, in evoluzione.

<!-- ![screenshot](assets/screenshot.png) -->

## Caratteristiche

- **3 editor affiancati** (HTML / CSS / JS) con numerazione righe, evidenziazione riga attiva e syntax highlighting (via `highlight.js`, incorporato offline — nessuna richiesta esterna)
- **Anteprima live** in `<iframe>` sandboxato, con esecuzione automatica o manuale (`▶ esegui`)
- **Pannello errori JavaScript** che intercetta e mostra gli errori runtime dell'anteprima
- **4 temi colore** per l'editor: Dracula, Atom One Dark, Monokai, GitHub (chiaro)
- **Dimensione carattere regolabile** con slider
- **Due layout**: editor affiancati oppure editor sopra / anteprima sotto, con pannelli ridimensionabili
- **Formattazione codice** rapida (`Alt+Shift+F`)
- **Export**: download singoli file (`index.html`, `style.css`, `script.js`), file HTML unico con tutto incluso, oppure archivio ZIP
- **Salvataggio automatico** dello stato degli editor

## Utilizzo

Nessuna installazione richiesta: basta aprire il file nel browser.

```bash
open index.html
```

In alternativa, per servirlo da un mini server locale (utile per test più realistici):

```bash
npm start
```

che esegue `npx serve .` sulla porta `5173`.

## Struttura del progetto

```
.
├── index.html              # l'intera applicazione (markup + CSS + JS, incluso highlight.js)
├── .github/workflows/
│   └── pages.yml            # deploy automatico su GitHub Pages ad ogni push su main
├── package.json
├── LICENSE
└── README.md
```

## Deploy

Il repo include un workflow GitHub Actions che pubblica automaticamente il contenuto su **GitHub Pages** ad ogni push sul branch `main`. Basta abilitare Pages nelle impostazioni del repository (Settings → Pages → Source: GitHub Actions).

## Roadmap / idee future

- [ ] Persistenza su file/gist condivisibili
- [ ] Supporto a preprocessori (Sass, TypeScript) via CDN opzionale
- [ ] Multi-progetto / tab di sessioni diverse
- [ ] Test automatici di base sull'anteprima

## Licenza

Distribuito sotto licenza [MIT](LICENSE).
