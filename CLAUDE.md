# CLAUDE.md — Site Céline Harbane

## Présentation du projet

Site portfolio/conversion de Céline Harbane — Chef de projet digital & Développeuse Shopify, basée à Paris. Objectif : convertir des visiteurs (PME françaises) en clients pour des missions de migration e-commerce vers Shopify.

URL de production : `https://celine-harbane-cheffe-de-projet-et.vercel.app/`  
Repo GitHub : `celineharbane/celine-harbane-cheffe-de-projet-et-dev`  
Déploiement : Vercel, auto-deploy sur push `main`

---

## Stack technique

- **HTML/CSS/JS pur** — aucun framework, aucun bundler
- **Three.js r128** — animation TorusKnot 3D en arrière-plan (canvas fixe)
- **GSAP 3.12.2 + ScrollTrigger** — animations au scroll et à l'entrée
- CDN : `cdnjs.cloudflare.com`
- Fonts : `Bebas Neue` (display/titres) + `DM Sans` (corps) via Google Fonts

---

## Charte graphique

```css
--bg:      #060608       /* fond principal */
--text:    #f0eeea       /* texte principal */
--muted:   #8a8a9a       /* texte secondaire */
--accent:  #3b82f6       /* bleu — accent principal */
--accent2: #8b5cf6       /* violet — Shopify Plus */
--accent-rgb: 59,130,246
--font-display: 'Bebas Neue', sans-serif
--font-body:    'DM Sans', sans-serif
```

**Icônes** : SVG stroke-based, `fill="none"`, `stroke-width="1.5"`, `stroke-linecap="round"`.  
- Sections standards → stroke `#4B7BF5`  
- Section Shopify Plus → stroke `#8b5cf6`  
Ne jamais utiliser d'emojis comme icônes.

---

## Structure des fichiers

```
index.html              ← site principal (tout en un seul fichier)
blog/
  index.html            ← liste des 10 articles
  migration-prestashop-shopify.html
  woocommerce-vs-shopify.html
  5-raisons-abandonner-prestashop.html
  migration-woocommerce-seo.html
  cout-migration-shopify.html
  wix-ecommerce-limites.html
  prestashop-couts-caches.html
  wix-vs-shopify.html
  migrer-catalogue-shopify.html
  erreurs-migration-ecommerce.html
images/
  GERMAINEDESPRESHOME (4).jpg
  GERMAINEDESPRESPRODUIT (1).jpg
  GERMAINEDESPRESPRODUIT (3).jpg
  GERMAINEDESPRETSCOFFRET.jpg
  LGNHOME.jpg
  LGNLISTPRODUIT (6).jpg
  LGNPRODUIT (7).jpg
sitemap.xml
robots.txt
vercel.json
```

---

## Sections de index.html (dans l'ordre)

| ID / classe | Contenu |
|---|---|
| `#loader` | Loader animé avec barre de progression |
| `#canvas-wrap` | Three.js TorusKnot (fixe, z-index 0) |
| `nav` | Logo CH + liens + CTA "Devis gratuit" (WhatsApp) |
| `.s-hero` | Hero : "MIGRATION / VERS SHOPIFY." + sous-titre + CTAs |
| `.s-about` | À propos + stats (50+ projets, 8 ans, etc.) |
| `#services .s-services` | 4 cartes service avec SVG icons |
| `#shopify-plus .s-plus` | Section Shopify Plus (6 cartes, accent violet) |
| `#processus .s-process` | 5 étapes du processus de travail |
| `#competences .s-skills` | 6 cartes compétences avec SVG icons |
| `#work .s-work` | Projets réalisés (Germaine des Prés + LGN) avec sliders |
| `.s-why` | "Pourquoi moi" — 4 arguments différenciants |
| `.s-faq` | FAQ accordion (7 questions) |
| `#contact .s-contact` | Contact final + email |
| `.sticky-cta` | Barre CTA fixe en bas (apparaît après 300px de scroll) |

---

## Projets dans la section Work

**Germaine des Prés** — Slider 4 images (3500ms autoplay)  
Fichiers : `GERMAINEDESPRESHOME (4).jpg`, `GERMAINEDESPRESPRODUIT (1).jpg`, `GERMAINEDESPRESPRODUIT (3).jpg`, `GERMAINEDESPRETSCOFFRET.jpg`

**Louis Gabriel Nouchi (LGN)** — Slider 3 images (4000ms autoplay)  
Fichiers : `LGNHOME.jpg`, `LGNLISTPRODUIT (6).jpg`, `LGNPRODUIT (7).jpg`

Affichage : rangées horizontales `.proj-row` avec mockup navigateur `.proj-browser`. Alternance `.reverse` sur la 2e ligne.

---

## Contact / CTA

- **WhatsApp** : `https://wa.me/33666461363`
- Message pré-rempli selon le contexte (migration PrestaShop, Shopify Plus, etc.)
- Email : présent dans la section contact

---

## Conventions de code

- Tout le CSS est inline dans `<style>` dans chaque fichier HTML
- Pas de fichiers CSS externes, pas de JS externe (sauf Three.js et GSAP en CDN)
- Les articles de blog partagent tous le même style dark (même variables CSS)
- URLs d'images avec espaces : encoder en `%20` dans le HTML
- Langue : **français** pour tout le contenu

---

## Workflow git

```bash
git add <fichier>
git commit -m "message"
git push   # → déploie automatiquement sur Vercel
```

Branche principale : `main`
