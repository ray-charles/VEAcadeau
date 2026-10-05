# ETAT, page cadeau (veacademy.studio/cadeau)

Journal vivant : chaque changement, pourquoi, et la suite.

## 2026-10-04 · Page lead magnet `/cadeau`

**Fait**
- Page `index.html` (dossier `C:\DEV CODE\Cadeau`, sorti du repo VEA) (français, marque bleue du VSL : teal, boutons jaunes, crème, Montserrat + Kalam). Formulaire prénom, nom, téléphone, courriel. Au clic : envoi à Formspree, pixel `Lead`, puis téléchargement du PDF (`cadeau.pdf`) + bouton de secours.
- Testé en local : envoi simulé, écran de succès, téléchargement déclenché, pas de débordement à 375 px.
- Kit : tag `cadeau-pdf` créé (id 24285181).

**Pourquoi la page n'est pas encore en ligne**
- `veacademy.studio` est un site Squarespace : GitHub Pages ne peut pas servir `/cadeau` dessus. Plan : héberger la page sur GitHub Pages et ajouter une redirection Squarespace (Paramètres → Redirections d'URL) `/cadeau -> <adresse de la page> 301`.

- Formspree : formulaire « Lead magnet PDF » créé (`mppqagwr`), branché dans la page. Courriel de notification à keating.sands@gmail.com.

**Suite**
1. Plugin ConvertKit du formulaire : la boîte « Connect ConvertKit » demande la clé API Kit (v3, Kit → Settings → Developer). Charles la colle lui-même, puis Claude choisit le tag `cadeau-pdf`.
2. Recevoir le PDF → `cadeau/cadeau.pdf`, réécrire titre + 3 puces (marqués `TODO PDF`).
3. Choisir l'hébergement, publier, ajouter la redirection Squarespace, tester de bout en bout.

## 2026-10-05 · Hébergement

- Choix : dépôt GitHub `ray-charles/VEAcadeau` → GitHub Pages → `cadeau.veacademy.studio`, plus redirection Squarespace `/cadeau`. Commit local prêt, fichier `CNAME` inclus.
- Bloqué : la création du dépôt public a été refusée par la vérification de sécurité de Claude Code. Charles doit l'autoriser (ou créer le dépôt), puis : Pages, enregistrement DNS `cadeau` CNAME `ray-charles.github.io` dans Squarespace, redirection `/cadeau -> https://cadeau.veacademy.studio 301`.
