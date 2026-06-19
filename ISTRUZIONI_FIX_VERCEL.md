# Fix Vercel – ricette non visibili

## Problema corretto
Nel file `index.html` precedente c'era un errore JavaScript nella funzione di evidenziazione della ricerca. Il file veniva caricato, ma lo script si interrompeva prima di stampare le schede delle ricette.

## Cosa fare
1. Apri il repository GitHub della webapp.
2. Sostituisci il file `index.html` con quello contenuto in questo pacchetto.
3. Fai `Commit changes` sul branch `main`.
4. Vercel dovrebbe eseguire automaticamente un nuovo deploy.
5. Quando il deploy è terminato, apri il dominio Vercel o il sottodominio configurato.

## Se Vercel non aggiorna subito
In Vercel vai nel progetto → `Deployments` → ultimo deployment → `Redeploy`.

## Verifica rapida
Cerca una ricetta come:
- `bolognese`
- `focaccia`
- `zucca`
- `tiramisu`

Se compaiono i risultati, il fix è installato correttamente.
