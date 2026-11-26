# CLAUDE.md – Sito della Fondazione Modesto Giusto (FMG)

Recap del lavoro e regole del progetto. Aggiornato al **26/11/2026**.
Tutto il testo del sito è in **italiano**: accenti sempre corretti (à è é ì ò ù), mai sostituiti con ASCII.

## Il progetto

Sito istituzionale della **Fondazione Modesto Giusto**, nata a Crema nel 2018 per volontà testamentaria
dell'avv. **Marco Giusto** (scomparso nel 2017 a 56 anni), in memoria del padre **Modesto**.
Sostiene **sport** (pallacanestro, calcio, sci, alpinismo) e **salute** (iniziative medico-sanitarie).
Motto: **«Una memoria che vive nello sport e nella cura»**.

Fase attuale: **una sola landing page** statica (HTML + CSS + poco JS, nessun build). Le altre pagine verranno dopo.

## Cartelle

- `materiale_FMG/` – materiale di partenza (progetto V5): `LEGGIMI.txt`, `01_Documenti/Progetto_sito_V5.docx` e
  `Bozza_homepage_V5.docx` (testi, mappa del sito, fonti), `02_Anteprima/Homepage_desktop_V5.png` (simulazione con
  immagini generate da IA, **non** da copiare), `03_Ritratti/` (Marco e Modesto, ~500×700 px), `04_Logo/` (`FMG.ai` è un PDF vettoriale).
- `sito/index.html` – la landing page.
- `sito/css/style.css` – unico foglio di stile.
- `sito/img/fmg-logo.svg`, `fmg-marchio.svg` – ricavati dal `.ai` con `pdftocairo -svg` e viewBox ritagliato
  (logo completo e solo marchio).
- `sito/img/marco-giusto.jpg`, `modesto-giusto.jpg` – ritratti originali.
- `sito/img/foto/` – foto **illustrative** Unsplash (da sostituire con foto autorizzate prima della pubblicazione).

Anteprima: aprire `sito/index.html` direttamente (percorsi relativi, funziona da `file://`).
Verifica visiva usata finora: `google-chrome --headless=new --screenshot=... --window-size=1440,9000` e `390,...` per il mobile.

## Struttura della pagina (in ordine)

1. **Intestazione** sticky: marchio + «Fondazione Modesto Giusto»; menu: La Fondazione · Progetti (tendina:
   Progetti realizzati, Progetti futuri, Proponi un progetto) · Contatti e trasparenza · **Sostienici** (bottone rosso).
   Su mobile (≤960px) pulsante «Menu», la tendina diventa sottoelenco sempre aperto.
2. **Apertura** (fondo azzurro): **logo FMG completo** a sinistra (centrato in verticale su motto + testo) + motto grande (h1, **EB Garamond corsivo**, righe bilanciate) a destra; sotto, una frase
   che integra gli ambiti («…la Fondazione sostiene lo **sport**, con pallacanestro, calcio, sci e alpinismo, e la
   **salute**, con iniziative medico‑sanitarie»; «sport» in blu, «salute» in rosso) + bottone blu «Leggi la nostra storia».
   I vecchi blocchi separati Sport/Salute sono stati tolti su richiesta.
3. **Le nostre origini** (fondo perla): a sinistra titolo + **ritratti di Marco e Modesto** (in bianco e nero, colonna 5/12, sticky su desktop),
   a destra il testo completo della bozza V5.
4. **Progetti realizzati**: cronologia per anni **2021 → 2022 → 2023–24 → 2026** (i tre progetti 2023–24 restano insieme:
   le fonti non danno l'anno preciso, scelta confermata dall'utente). Il **2026** contiene il sostegno alla ricerca
   clinica onco-ematologica (Data Manager all'Oncologia dell'Ospedale di Crema, da
   `01_Documenti/Fondazione_Modesto_Giusto_Progetto_Ricerca_Oncoematologica.docx`): anno confermato dall'utente, il documento
   non lo riporta; nessuna fonte pubblica. Ogni voce: ambito, titolo, testo, fonte con link, foto.
   Bottone «Vai all'archivio dei progetti realizzati».
5. **Progetti futuri** (fondo perla, linee **tratteggiate** = non ancora avvenuto): direzioni Sport / Salute, nota
   sulle decisioni degli organi, bottone «Scopri i progetti futuri»; in fondo riquadro **Proponi un progetto**
   (`#proponi`, bordo rosso, elenco di cosa scrivere nell'email, bottone rosso «Invia la tua proposta»; niente modulo).
6. **Sostienici con il 5×1000** (`#sostienici`, fondo blu): a sinistra spiegazione (quota IRPEF, non sostituisce
   8×1000 e 2×1000; 730, Redditi o scheda CU); a destra **facsimile del riquadro** del modulo con firma e caselle del CF,
   marcatori rossi 1 e 2 che corrispondono ai due passaggi.
7. **Footer** (fondo perla, filetto rosso in alto): logo + motto · Contatti (Sede legale, Email, Codice fiscale; etichette sopra i valori)
   · Trasparenza (Statuto, Organi, Bilanci e documenti) · Il sito (link rapidi). Riga finale:
   «© 2026 Fondazione Modesto Giusto – Tutti i diritti riservati» a sinistra, Privacy policy e Cookie policy a destra
   (a sinistra su mobile), link sottolineati con area di tocco ≥44px.

## Linguaggio visivo

- **Palette** (`:root`): `--blu #193C55`, `--blu-medio #4F7499`, `--rosso #CD2B32`, `--antracite #383838`,
  `--grigio #646A71`, `--perla #EEF1F3`, `--filetto #D3DAE0`.
- **Regola di colore con significato**: **blu = sport, rosso = cura/salute** (le due foglie del marchio). Il rosso è
  anche il colore delle azioni (Sostienici, Proponi).
- **Caratteri** (oggi da Google Fonts): **EB Garamond corsivo** (`--motto`) solo per il motto, nell'apertura e nel footer (scelto dall'utente
  tra 4 varianti; scartato un font calligrafico vero); **Source Serif 4** per titoli e racconto; **Archivo** (con `font-stretch: 125%`,
  richiama la scritta «FMG» del logo) per anni, etichette, menu e testo d'interfaccia.
- **Fondi alternati** (richiesta utente): azzurro `--azzurro #E1ECF6` e grigio chiaro `--grigio-chiaro #F0F1F2`
  (apertura azzurro, origini grigio, progetti azzurro, futuri grigio, 5×1000 blu, footer grigio). **Bianco solo
  nell'intestazione**: niente sezioni o riquadri bianchi.
- Centratura senza contenitori annidati: `padding-inline: var(--lato)`.
- Tono **sobrio ed editoriale**. Sono stati **tolti su richiesta** (non reintrodurli): etichette sopra i titoli,
  barrette rosse decorative, parole del titolo in altro colore, numeri giganti sbiaditi di sfondo, file di icone,
  frasi pubblicitarie inventate, sezione News vuota, sezione «Cosa sosteniamo» separata, voce 2017 nella cronologia,
  bottoni «Copia codice fiscale» / «Invia al commercialista», frase sul rendiconto 5×1000, nota sulle foto Unsplash nel footer.
- Preferenze dell'utente: niente stile template/«AI slop»; privacy e cookie come **link**, non bottoni.

## Collegamenti e segnaposto

- Le pagine future non esistono ancora: i link hanno `href="#"` (riportano alla home) e un attributo
  `data-pagina="progetti-realizzati.html"` / `"progetti-futuri.html"` che indica la destinazione futura.
  Stessa cosa per i link di Trasparenza, Privacy e Cookie.
- **Dati ufficiali** (forniti dall'utente il 26/11/2026): sede legale **Via Stazione 9/B – 26013 Crema (CR)**,
  email **fondazionemodestogiusto@gmail.com** (anche nel bottone «Invia la tua proposta», mailto con oggetto),
  codice fiscale **91041060194**. **PEC non esiste**: non aggiungerla. **Telefono**: nel footer c'è
  un numero **inventato** (`0373 123456`, richiesto dall'utente come segnaposto, con commento nell'HTML, senza link `tel:`):
  sostituirlo con quello reale prima di pubblicare.
- La **categoria del 5×1000** non è nota: tolta dal passaggio 1 su richiesta («Metti la tua firma nella scheda del 5×1000»).
  Probabilmente è «Sostegno degli enti del Terzo settore» (se iscritta al RUNTS): reinserirla solo se l'utente la conferma.
- Il **codice fiscale del 5×1000** è in `id="cf-fmg"`: lo script in fondo a `index.html`
  genera le caselle del facsimile (`[data-cf-caselle]`). Quello del footer è scritto a parte.
- JS inline in fondo a `index.html`: menu mobile, tendina Progetti (clic, Esc, clic fuori), caselle del CF.

## Contenuti da verificare prima di pubblicare (dal LEGGIMI)

- Ammissione al 5×1000 e categoria, dominio, autorizzazioni per le foto.
- **Dynaschool**: non pubblicare «1.000 bambini» e «€ 7.500» (obiettivo e contributo richiesto, non consuntivi):
  c'è un commento nell'HTML.
- Criteri di «Proponi un progetto» (chi può proporre, eventuali scadenze o regolamento).

## Foto illustrative attuali (Unsplash, licenza free dedotta dall'host: confermare sulla pagina della foto)

| File | Soggetto | ID Unsplash |
|---|---|---|
| `progetto-2021-sanita.jpg` | postazione di ventilazione/anestesia (ritaglio manuale) | `photo-1664902273035-82c35762a0b1` |
| `progetto-2022-anziani.jpg` | operatrice con anziana in residenza (Age Cymru) | `photo-1773227055624-07b515ba87c5` |
| `progetto-2023-baita.jpg` | baita al tramonto | `photo-1542718610-a1d656d1884c` |
| `progetto-2023-sci.jpg` | sciatore in pista | `photo-1551698618-1dfe5d97d256` |
| `progetto-2023-basket.jpg` | bambini al minibasket in palestra (ritaglio manuale) | `photo-1777613017000-b517b56efc3e` |
| `progetto-2026-oncologia.jpg` | tre ricercatori in camice guardano un tablet (National Cancer Institute) | `photo-1631556759511-6ce895fbf0ad` |

## Prossimi passi proposti

Spunti presi dal sito `../TIPOGRAFIA_LOCATELLI/sito_locatelli_v3` (altro genere: riprendere la base tecnica, non lo stile):

1. **Font self-hosted** (woff2 in `assets/fonts/`, niente Google Fonts per il GDPR) – priorità alta.
2. Riordino in `assets/` (`fonts/`, `img/`, `scripts/`, `styles/`); **JS in file esterno** (niente script inline, per la CSP).
3. `privacy.html`, `404.html`, `.htaccess` (header di sicurezza, CSP, cache, HTTPS/www commentati fino all'SSL).
4. SEO: Open Graph, JSON-LD da fondazione/organizzazione, `sitemap.xml`, `robots.txt`, `site.webmanifest`, favicon.
5. `README.md` con checklist di messa online.
6. Possibili extra: voce di menu attiva durante lo scroll; ingresso animato del motto (unica animazione,
   con `prefers-reduced-motion`).
7. Pagine successive: `progetti-realizzati.html` (archivio), `progetti-futuri.html`, La Fondazione, Sostienici.
