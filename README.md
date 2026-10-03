# Portfolio — Michele Campanello

Sito portfolio di uno sviluppatore web alle prime armi, creato semplicemente con HTML e CSS puri, senza framework o librerie esterne.
L'obiettivo del sito è quello di promuovere i miei progetti e attirare l'attenzione di potenziali clienti o aziende interessate ad assumermi.
Il sito presenta infatti un form di contatto funzionante grazie a formspree

## Caratteristiche

- Due pagine: home (hero, progetti, contatti) e `chi-sono.html`
- Tema scuro con colore d'accento definito da variabili CSS
- Layout responsive, dal mobile al desktop
- Animazioni di ingresso e header che si solidifica allo scroll, tutte con CSS scroll-driven (nessun JS)
- Rispetto di `prefers-reduced-motion`
- Accessibilità: skip link, landmark semantici, `aria-current`, focus visibile, testi alternativi
- Form di contatto con [Formspree](https://formspree.io/) e campo honeypot anti-spam
- Utilizzo della nuova funzione di annidamento di CSS. Prima era possibile solo con un preprocessore come SASS o SCSS

## Struttura della cartella

```
.
├── index.html          # Home
├── chi-sono.html       # Pagina "Chi sono"
└── assets/
    ├── css/
    │   ├── style.css       # Variabili, reset, motion; importa gli altri file
    │   ├── header.css
    │   ├── hero.css
    │   ├── section.css     # Layout e titoli condivisi delle sezioni
    │   ├── projects.css
    │   ├── about.css
    │   ├── contact.css
    │   └── footer.css
    └── img/                # Screenshot dei progetti, foto profilo, icone social
```

## Avvio in locale

Il sito è statico: basta servire la cartella con un qualsiasi server o con l'esensione Live Server di Visual Studio Code.

## Personalizzazione

### Colori, spaziature e font

Tutto parte dalle variabili in `:root` di `assets/css/style.css`:

```css
--bg: #090a0a;
--accent: #c8ff3d;
--container: 1100px;
--font-sans: Inter, ui-sans-serif, system-ui, sans-serif;
```

Cambiando `--accent` si aggiornano pulsanti, link attivi, bordi in hover e bagliori.

### Form di contatto

Il form invia i dati all'endpoint Formspree indicato nell'attributo `action`.

## Compatibilità

Il sito è pensato per i browser moderni. Alcune funzioni sono miglioramenti progressivi: dove non sono supportate, i contenuti si vedono comunque, senza animazioni.

- Animazioni allo scroll e header dinamico: `animation-timeline` (`scroll()` / `view()`)
- Evidenziazione della voce di menu corrente: `:target-current`
- Stato di errore dei campi del form: `:user-invalid`

## Contatti

- Sito: [michelecampanello.github.io/Portfolio-HTML-CSS](michelecampanello.github.io/Portfolio-HTML-CSS)
- GitHub: [michelecampanello](https://github.com/michelecampanello)
- LinkedIn: [Michele Campanello](https://www.linkedin.com/in/michele-campanello-82365325a/)
