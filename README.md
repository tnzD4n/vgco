# 📖 PDF Knowledge Base

Applicazione web statica e ricercabile generata da un PDF, deployabile su GitHub Pages. Zero backend, zero build step.

---

## 🚀 Setup (per il proprietario del repo)

```bash
# 1. Installa le dipendenze locali (solo per il parsing)
npm install

# 2. Copia il tuo PDF nella root del progetto
cp /path/to/your/file.pdf ./database.pdf

# 3. Genera il database
node parse.js

# 4. Committa tutto
git add index.html data.json README.md .gitignore parse.js package.json
git commit -m "Initial knowledge base"
git push
```

---

## 🌐 Attivare GitHub Pages

1. Vai al tuo repo su GitHub
2. **Settings → Pages**
3. Source: `Deploy from a branch`
4. Branch: `main`, cartella: `/ (root)`
5. Salva — il sito sarà live su `https://<username>.github.io/<reponame>/`

---

## 🔄 Aggiornare il database

```bash
# Sostituisci il PDF e ri-parsa
cp /path/to/new.pdf ./database.pdf
node parse.js
git add data.json
git commit -m "Update knowledge base"
git push
```

---

## 👥 Per i visitatori

Apri semplicemente l'URL di GitHub Pages — nessuna installazione richiesta.

---

## 📁 Struttura del progetto

```
project/
├── index.html      # Frontend completo (HTML+CSS+JS inline)
├── data.json       # Generato da parse.js — committato nel repo
├── parse.js        # Script locale: PDF → data.json
├── package.json    # Solo per parse.js (dipendenze locali)
├── .gitignore
└── README.md
```
