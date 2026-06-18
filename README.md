# La cucina di Manu — Ricettario digitale

Webapp statica one-page per consultare e cercare le ricette del progetto **La cucina di Manu**.

## Contenuto del repository

- `index.html` — webapp completa, pronta per la pubblicazione.
- `vercel.json` — configurazione Vercel per servire la webapp come sito statico one-page.

## Pubblicazione consigliata

Dominio finale desiderato:

```text
https://app.lacucinadimanu.com
```

## Impostazioni Vercel consigliate

Quando importi il repository su Vercel:

- Framework Preset: **Other** oppure **No Framework**
- Root Directory: `./`
- Build Command: lasciare vuoto
- Output Directory: lasciare vuoto oppure `./`
- Install Command: lasciare vuoto

La webapp è statica e non richiede Node.js, database, API o variabili ambiente.

## DNS da configurare su WordPress.com

Dopo aver aggiunto `app.lacucinadimanu.com` nei domini del progetto Vercel, Vercel mostrerà il record DNS esatto da creare.

Di norma sarà un record di questo tipo:

| Tipo | Nome / Host | Valore / Points to | TTL |
|---|---|---|---|
| CNAME | app | valore indicato da Vercel | Automatico o 3600 |

Importante: copiare il valore CNAME esattamente come indicato da Vercel. Può essere un valore univoco del progetto, ad esempio simile a `xxxx.vercel-dns-xxx.com`.

## Aggiornamenti futuri

Per aggiornare la webapp:

1. sostituire `index.html` nel repository GitHub;
2. fare commit su `main`;
3. Vercel pubblicherà automaticamente la nuova versione.
