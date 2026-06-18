# Istruzioni operative — GitHub, Vercel, DNS WordPress

## 1. Preparazione file

Carica su GitHub questi file:

- `index.html`
- `vercel.json`
- `README.md`

Non rinominare `index.html`: Vercel lo userà come pagina principale della webapp.

---

## 2. Creare il repository GitHub

1. Vai su GitHub.
2. Clicca su **New repository**.
3. Nome consigliato:

```text
la-cucina-di-manu-ricettario
```

4. Visibilità consigliata: **Private** se non vuoi rendere pubblico il codice; **Public** se non è un problema.
5. Spunta **Add a README file** solo se vuoi; in alternativa carica il README incluso in questo pacchetto.
6. Clicca **Create repository**.

---

## 3. Caricare i file su GitHub via browser

1. Dentro il repository appena creato, clicca **Add file**.
2. Clicca **Upload files**.
3. Trascina dentro la pagina i file:

```text
index.html
vercel.json
README.md
ISTRUZIONI_DEPLOY.md
```

4. In basso, in **Commit changes**, scrivi ad esempio:

```text
Prima pubblicazione webapp ricettario
```

5. Seleziona **Commit directly to the main branch**.
6. Clicca **Commit changes**.

---

## 4. Importare il progetto in Vercel

1. Vai su Vercel.
2. Clicca **Add New...** oppure **New Project**.
3. Scegli **Import Git Repository**.
4. Seleziona il repository GitHub:

```text
la-cucina-di-manu-ricettario
```

5. Nelle impostazioni di importazione usa:

```text
Framework Preset: Other / No Framework
Root Directory: ./
Build Command: vuoto
Output Directory: vuoto o ./
Install Command: vuoto
```

6. Clicca **Deploy**.
7. Vercel creerà un indirizzo provvisorio tipo:

```text
https://la-cucina-di-manu-ricettario.vercel.app
```

Controlla che la webapp funzioni correttamente.

---

## 5. Aggiungere il sottodominio in Vercel

1. In Vercel apri il progetto.
2. Vai su **Settings**.
3. Vai su **Domains**.
4. Clicca **Add Domain**.
5. Inserisci:

```text
app.lacucinadimanu.com
```

6. Conferma.
7. Vercel ti mostrerà il record DNS da impostare. Copia esattamente il valore indicato.

---

## 6. Creare il DNS su WordPress.com

1. Vai nella dashboard WordPress.com del sito.
2. Vai su **Upgrades / Aggiornamenti → Domains / Domini**.
3. Clicca sul dominio:

```text
lacucinadimanu.com
```

4. Apri **DNS records / Record DNS**.
5. Clicca **Manage / Gestisci**.
6. Clicca **Add a record / Aggiungi record**.
7. Inserisci il record:

```text
Type / Tipo: CNAME
Name / Host: app
Value / Points to: valore CNAME mostrato da Vercel
TTL: automatico oppure 3600
```

8. Salva.

---

## 7. Verifica finale

1. Torna in Vercel → progetto → **Settings → Domains**.
2. Attendi che lo stato diventi valido, per esempio **Valid Configuration** o equivalente.
3. Apri:

```text
https://app.lacucinadimanu.com
```

La propagazione DNS può richiedere pochi minuti, ma in alcuni casi anche diverse ore.

---

## 8. Aggiornamenti futuri della webapp

Ogni volta che modifichi la webapp:

1. carica il nuovo `index.html` nel repository GitHub;
2. fai **Commit changes** su `main`;
3. Vercel aggiornerà automaticamente il sito pubblicato.

---

## 9. Nota importante

Non modificare i DNS principali di `lacucinadimanu.com` e `www.lacucinadimanu.com`, altrimenti rischi di toccare il sito WordPress ufficiale. Per questa webapp serve solo il sottodominio `app`.
