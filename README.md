# Site TRIADE — squelette prêt pour GitHub Pages

Ce dossier contient un site statique (HTML/CSS pur, aucune dépendance) prêt à être
mis en ligne gratuitement via GitHub Pages.

## Structure des fichiers
```
triade-site/
├── index.html         → page d'accueil
├── carnet.html         → carnet de route (articles)
├── associations.html  → associations soutenues / cagnotte
├── style.css           → feuille de style partagée par toutes les pages
└── README.md            → ce fichier
```

## Mise en ligne avec GitHub Pages (gratuit)

1. Crée un compte sur github.com si tu n'en as pas déjà un.
2. Crée un nouveau dépôt (repository), par exemple nommé `triade-site`.
   - Public (obligatoire pour GitHub Pages gratuit sur un compte personnel classique)
3. Mets tous les fichiers de ce dossier à la racine du dépôt :
   - Sur github.com, bouton "Add file" → "Upload files" → glisse-dépose les 5 fichiers
   - (ou en ligne de commande si tu es à l'aise avec git : `git init`, `git add .`,
     `git commit -m "premier site"`, `git remote add origin <url>`, `git push`)
4. Va dans **Settings** du dépôt → section **Pages** (dans le menu de gauche).
5. Sous "Build and deployment" → Source, choisis **"Deploy from a branch"**,
   branche `main`, dossier `/ (root)` → **Save**.
6. Après 1-2 minutes, GitHub affiche l'URL de ton site, du type :
   `https://<ton-pseudo-github>.github.io/triade-site/`

## Mettre à jour le site pendant le voyage

Deux options simples depuis un téléphone :
- **App GitHub officielle** : ouvre le fichier à modifier (ex. `carnet.html`),
  édite le texte directement, valide ("Commit changes"). Le site se met à jour
  automatiquement en 1-2 minutes.
- **github.dev** : appuie sur la touche `.` sur la page du dépôt (ou remplace
  `github.com` par `github.dev` dans l'URL) pour ouvrir un éditeur de code complet
  dans le navigateur, y compris sur mobile.

## Ajouter un nouvel article au carnet

Dans `carnet.html`, duplique un bloc comme celui-ci et modifie le texte :
```html
<a class="bcard" href="#">
  <div class="bimg"></div>
  <div class="bc-body">
    <div class="bc-tag">PAYS · JOUR</div>
    <h4>Titre de l'article</h4>
    <p>Résumé court de l'étape.</p>
  </div>
</a>
```

## Intégrer la carte en direct (Polarsteps) et le compteur de dons (HelloAsso)

Cherche les commentaires `<!-- ... -->` dans `index.html` et `associations.html` :
ils indiquent exactement où coller le code `<iframe>` fourni par Polarsteps
("Partager" → "Intégrer sur un site") et par HelloAsso ("Partager" → widget).

## Nom de domaine personnalisé (optionnel)

Si tu achètes un domaine (ex. chez Namecheap ou OVH, ~10€/an) :
1. Dans Settings → Pages de ton dépôt, renseigne le domaine dans "Custom domain".
2. Chez ton registrar, ajoute les enregistrements DNS indiqués par GitHub
   (documentation officielle : `docs.github.com` → "Managing a custom domain
   for your GitHub Pages site").
