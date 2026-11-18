# Guida al portale e-commerce B2B – Mitsubishi Electric

Sito statico di help con video tutorial e istruzioni passo-passo per i clienti del portale e-commerce B2B (SAP Commerce Cloud – Composable Storefront).

## Contenuto

| Percorso | Descrizione |
|---|---|
| `index.html` | L'intero sito: testi, navigazione, ricerca e player (HTML/CSS/JS in un solo file, nessuna dipendenza esterna) |
| `video/` | 32 video tutorial in MP4 (H.264, senza audio, ottimizzati per lo streaming) |
| `img/` | Immagini di anteprima dei video |

Ogni passaggio del testo è collegato al momento esatto del video (pulsanti ▶).

## Pubblicazione con GitHub Pages

1. **Settings › Pages**
2. *Source*: **Deploy from a branch** → branch `main`, cartella `/ (root)` → **Save**
3. Dopo qualche minuto il sito è disponibile su `https://hnrg-lab.github.io/mitsubishi-portal-help/`

Il file `.nojekyll` evita l'elaborazione Jekyll e pubblica i file così come sono.

## Configurazione

All'inizio dello script in `index.html`:

```js
const PORTAL_URL = "https://it-s1.mitsubishielectric.eu/AC_DX/it/EUR/";
```

È l'indirizzo dell'**ambiente di test**: prima della messa in produzione va sostituito con l'URL di produzione.

Il logo è opzionale: se si aggiunge `img/logo.svg` viene mostrato nell'header.

## Dati nei video

I video sono stati registrati sull'ambiente di test. Indirizzi, telefoni, e-mail, nomi utente e codici cliente sono stati sfocati. I file originali non sfocati **non** fanno parte di questo repository e non devono esservi aggiunti.

## Modifica dei contenuti

I testi sono nell'array `CHAPTERS` in `index.html`. Ogni passaggio ha la forma:

```js
[17, `Testo del passaggio`]      // 17 = secondo del video da mostrare
[9,  `Testo`, 1]                 // terzo valore = indice del video (se l'argomento ne ha più di uno)
[null, `Passaggio senza video`]
```

---
Realizzato da HNRG – Altea Federation.
