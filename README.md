# Sito della Fondazione Modesto Giusto

Sito istituzionale della **Fondazione Modesto Giusto** (Crema), che sostiene lo sport e la salute
in memoria di Modesto Giusto.

> «Una memoria che vive nello sport e nella cura»

Per ora il sito è **una sola landing page** statica: HTML, CSS e poco JavaScript, senza dipendenze
né passaggi di build. Le altre pagine verranno aggiunte in seguito.

## Anteprima

Aprire `sito/index.html` nel browser. I percorsi sono relativi, quindi la pagina funziona anche da `file://`.

## Struttura

```
sito/
├── index.html          landing page (lo script per menu, tendina e caselle del CF è in fondo)
├── css/style.css       unico foglio di stile
└── img/
    ├── fmg-logo.svg    logo completo
    ├── fmg-marchio.svg solo marchio
    ├── marco-giusto.jpg, modesto-giusto.jpg   ritratti
    └── foto/           foto illustrative dei progetti
```

Le sezioni della pagina sono: intestazione, apertura con il motto, Le nostre origini,
Progetti realizzati, Progetti futuri (con Proponi un progetto), Sostienici con il 5×1000 e footer.

Le regole di design e i dettagli sui contenuti sono in [`CLAUDE.md`](CLAUDE.md).

## Prima della pubblicazione

- [ ] Sostituire il **telefono** segnaposto nel footer (`0373 123456`) con quello reale.
- [ ] Sostituire le **foto illustrative** Unsplash in `sito/img/foto/` con foto autorizzate.
- [ ] Confermare l'ammissione al **5×1000** e la categoria.
- [ ] Verificare i dati di **Dynaschool**: non pubblicare obiettivi e contributi richiesti come se fossero consuntivi.
- [ ] Definire i criteri di **Proponi un progetto** (chi può proporre, scadenze, regolamento).
- [ ] Ospitare i **font** in locale invece di usare Google Fonts (GDPR).
- [ ] Aggiungere privacy policy, cookie policy, pagina 404, favicon e metadati SEO.
- [ ] Scegliere il dominio e attivare HTTPS.

## Contatti

Fondazione Modesto Giusto · Via Stazione 9/B, 26013 Crema (CR)
fondazionemodestogiusto@gmail.com · C.F. 91041060194

---

© 2026 Fondazione Modesto Giusto. Testi, logo e ritratti appartengono alla Fondazione.
