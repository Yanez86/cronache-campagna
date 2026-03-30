# ⚔ Cronache della Campagna — TTRPG Blog

Blog per campagne TTRPG costruito con **Astro**, ospitato su **Netlify**, gestito con **Decap CMS + Netlify Identity**.

---

## 🚀 Setup in 4 passi

### 1. Crea un repo su GitHub

1. Vai su [github.com/new](https://github.com/new)
2. Nome repo (es. `cronache-campagna`)
3. Imposta **Public**
4. **Non** inizializzare con README
5. Clicca **Create repository**

Poi dal terminale nella cartella del progetto:

```bash
git init
npm install
git add .
git commit -m "🎲 Initial commit"
git branch -M main
git remote add origin https://github.com/TUO-USERNAME/TUO-REPO.git
git push -u origin main
```

---

### 2. Collega a Netlify

1. Vai su [app.netlify.com](https://app.netlify.com)
2. **Add new site** → **Import an existing project** → **GitHub**
3. Seleziona il tuo repo
4. Impostazioni build:
   - **Build command**: `npm run build`
   - **Publish directory**: `dist`
5. Clicca **Deploy site**

Il sito sarà live su `https://NOME-SITO.netlify.app` 🎉

---

### 3. Abilita Netlify Identity

1. Vai su **Site configuration** → **Identity** → **Enable Identity**
2. In **Registration** seleziona **Invite only** (solo tu puoi accedere)
3. Scorri fino a **Git Gateway** → clicca **Enable Git Gateway**

---

### 4. Invita te stesso come utente

1. Vai su **Identity** → **Invite users**
2. Inserisci la tua email
3. Controlla la mail e clicca il link di conferma
4. Imposta la password

Ora puoi accedere al CMS su:
```
https://NOME-SITO.netlify.app/admin/
```

---

## 📝 Usare il CMS

1. Vai su `/admin/` del tuo sito
2. Clicca **Login with Netlify Identity**
3. Usa l'editor WYSIWYG per gestire tutti i contenuti

Ogni salvataggio fa un commit automatico su GitHub e il sito si aggiorna in ~1 minuto.

---

## 🗂 Struttura

```
ttrpg-blog/
├── src/
│   ├── content/
│   │   ├── sessions/       ← sessioni di gioco
│   │   ├── characters/     ← schede personaggio
│   │   ├── house-rules/    ← regole homebrew
│   │   ├── world/          ← lore del mondo
│   │   └── credits/        ← credits
│   ├── layouts/
│   ├── pages/
│   └── styles/
├── public/
│   └── admin/
│       └── config.yml      ← configurazione CMS
├── netlify.toml
└── astro.config.mjs
```
