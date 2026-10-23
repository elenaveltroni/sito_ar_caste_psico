# Sito di Andrea Roberto Castellani

Sito web statico di Andrea Roberto Castellani, psicologo e psicoterapeuta a Pisa e online (Instagram: [@ar.caste_psico](https://www.instagram.com/ar.caste_psico/)).

Nessun build step né dipendenze: solo HTML, CSS e un po' di JavaScript inline.

## Struttura

```
.
├── index.html      # Home: presentazione, servizi, studio, feed Instagram
├── prenota.html    # Prenotazione colloquio (widget Calendly, in studio / online)
├── contatti.html   # Contatti e modulo (invio tramite mailto:)
├── style.css       # Stili del sito; i colori sono nella sezione :root
├── fonts/          # Figtree (variable, woff2)
├── img/            # Foto (andrea.jpg, studio.jpg) e loghi
└── LEGGIMI.txt     # Appunti da completare prima della pubblicazione
```

## Servizi di terze parti

| Servizio | Uso |
| --- | --- |
| Calendly | Calendario di prenotazione in `prenota.html` |
| Elfsight | Feed Instagram in `index.html` |
| iubenda | Privacy policy, cookie policy e banner cookie |
| Google Fonts | Cormorant Garamond e Poppins |

Instagram, Calendly e iubenda usano cookie di terze parti: se si cambiano o aggiungono servizi, aggiornare la cookie policy.

## Sviluppo in locale

Basta aprire `index.html` nel browser. Per un server locale:

```bash
python -m http.server 8000
```

Poi visitare <http://localhost:8000>.

## Modifiche frequenti

- **Colori**: variabili CSS all'inizio di `style.css` (`:root`).
- **Contatti, indirizzo e P.IVA**: compaiono nel piede di ogni pagina e in `contatti.html`; vanno aggiornati in tutti i file.
- **Link di prenotazione**: gli URL Calendly sono in `prenota.html`.
- **Destinatario del modulo contatti**: costante `EMAIL_DESTINATARIO` nello script di `contatti.html`.

## Pubblicazione

Essendo un sito statico, basta caricare i file su qualsiasi hosting statico (GitHub Pages, Netlify, hosting tradizionale via FTP, ecc.).
