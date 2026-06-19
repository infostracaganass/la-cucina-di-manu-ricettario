# Aggiornamento mobile e icona webapp

Per installare questa versione su GitHub/Vercel:

1. Apri il repository GitHub della webapp.
2. Sostituisci `index.html` con quello contenuto in questo pacchetto.
3. Aggiungi anche questi nuovi file nella root del repository:
   - `site.webmanifest`
   - `icon-192.png`
   - `icon-512.png`
   - `apple-touch-icon.png`
   - `favicon.png`
   - `vercel.json`
4. Fai `Commit changes`.
5. Attendi il nuovo deploy automatico su Vercel.
6. Da cellulare, apri il sito e ricarica la pagina. Per vedere la nuova icona, potrebbe essere necessario eliminare la vecchia icona salvata dalla schermata Home e aggiungerla di nuovo.

Nota: il pulsante `Cerca` forza il blur del campo di ricerca, così la tastiera mobile dovrebbe chiudersi dopo la ricerca.
