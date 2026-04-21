# Céline Harbane — Cheffe de Projet & Dev Shopify

Portfolio professionnel en HTML/CSS/JS (Three.js + GSAP via CDN).
Site statique self-contained prêt à déployer sur Vercel.

**Nom du projet Vercel** : `celine-harbane-cheffe-de-projet-et-dev`
**URL cible** : https://celine-harbane-cheffe-de-projet-et-dev.vercel.app

> Ce projet est un **nouveau déploiement séparé** — ton projet `celineharbane-3d-demo` existant reste intact.

---

## Déployer en 3 options

### Option A — Drag & drop (recommandé, 30 secondes)

1. Va sur https://vercel.com/new
2. En bas de la page, section **"Deploy without Git"** → clique sur **"Other"**
3. Glisse-dépose le dossier `celine-harbane-cheffe-de-projet-et-dev/` entier
4. Vercel te demande un nom de projet → entre `celine-harbane-cheffe-de-projet-et-dev`
5. Clique **Deploy** — ton URL sera https://celine-harbane-cheffe-de-projet-et-dev.vercel.app

### Option B — Vercel CLI

Depuis le dossier du projet :

```bash
cd celine-harbane-cheffe-de-projet-et-dev
vercel --prod
```

À la première exécution, Vercel demande :
- `Set up and deploy?` → **Yes**
- `Link to existing project?` → **No** (on crée un nouveau projet)
- `What's your project's name?` → `celine-harbane-cheffe-de-projet-et-dev`
- `In which directory is your code located?` → `./` (appuie sur Entrée)

### Option C — Via GitHub (si tu veux versionner)

```bash
# Crée un nouveau repo GitHub (public ou privé)
# Sur github.com → New repository → celine-harbane-cheffe-de-projet-et-dev

cd celine-harbane-cheffe-de-projet-et-dev
git init
git add .
git commit -m "feat: initial portfolio deployment"
git branch -M main
git remote add origin https://github.com/celineharbane/celine-harbane-cheffe-de-projet-et-dev.git
git push -u origin main

# Puis sur vercel.com/new → Import Git Repository → sélectionne le repo
```

Vercel redéploie automatiquement à chaque push sur `main`.

---

## Contenu du dossier

| Fichier | Rôle |
|---|---|
| `index.html` | Portfolio complet (1531 lignes, tout inline) |
| `vercel.json` | Config Vercel (cleanUrls + headers sécurité) |
| `robots.txt` | Autorisation crawl + lien sitemap |
| `sitemap.xml` | Sitemap minimal pour GSC |
| `README.md` | Ce fichier |

## Checks post-déploiement

- [ ] Animation Three.js charge (torus knot + particules)
- [ ] Loader s'affiche puis disparaît (1,6 s)
- [ ] Scroll déclenche les animations GSAP (hero → about → services → work → contact)
- [ ] Curseur custom fonctionne sur desktop
- [ ] Responsive OK sur mobile (iPhone SE 320px minimum)
- [ ] Navigation ancre fonctionne (scroll vers les sections)
- [ ] Lien contact → mailto fonctionne

## Pour plus tard : brancher ton domaine custom

Une fois déployé, Vercel → Project → Settings → Domains → Add :
- `celineharbane.com` (ou le domaine que tu choisis)
- Suivre les instructions DNS (OVH, Gandi, Cloudflare…)

## Contact

Céline Harbane · capr@hotmail.fr · Paris
