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

## 2026-10-06 · PDF final, page en espagnol, mise en ligne

**Fait**
- PDF : celui envoyé par Mamselle le 6 oct. (17 pages, CaféCITO 8 oct.) + **page 18** ajoutée : offre membresía 17 $ CAD/mois (prix vérifié sur le checkout Circle), bouton cliquable vers `https://voz-esencia-academy-cbf28a.circle.so/checkout/membership`. Source de la page 18 : `pdf-cierre.html` (Chrome headless → PDF, puis ajoutée avec PyMuPDF, lien recréé). Résultat : `cadeau.pdf` (18 pages).
- Page passée en **espagnol** (le PDF et le public sont hispanophones au Canada) et à l'**image du PDF** : crème, Cormorant Garamond italique, DM Sans, teal #0d4a5c, aqua #6fbfb5. Pixel VEA seul. Testé : envoi Formspree `mppqagwr`, téléchargement du PDF, pas de débordement mobile.
- Dépôt public `ray-charles/VEAcadeau` créé, GitHub Pages actif avec le domaine `cadeau.veacademy.studio`.
- Brouillon Gmail pour Mamselle (mamselleruiz@gmail.com, adresse vérifiée dans l'historique) dans le fil « PDF LEAD MAGNET POUR EL CAFECITO », avec le lien du PDF et 3 points à vérifier. Non envoyé.

**Bloqué (Charles)**
- Squarespace demande de reconfirmer la connexion Google avant de toucher au DNS. Après ça : enregistrement `CNAME cadeau → ray-charles.github.io`, puis redirection `/cadeau -> https://cadeau.veacademy.studio 301` (Paramètres du site → Outils pour développeurs → Redirections d'URL).
- Formspree : ajouter mamselleruiz@gmail.com dans Account → Linked emails (refusé à Claude par la vérification de sécurité), Mamselle clique le lien de vérification, puis Claude ajoute l'action courriel sur le formulaire.
- Formspree → Kit : coller la clé API Kit v3 dans le plugin ConvertKit du formulaire.
- Page 17 du PDF : « [fecha y hora] » et « [enlace] » du webinaire restent à remplir (contenu de Mamselle).

## 2026-10-06 (suite) · Formspree seul, pas de Kit

- Décision de Charles : **pas de Kit** pour ce lead magnet, Formspree seulement. Plugin ConvertKit abandonné ; le tag Kit `cadeau-pdf` (24285181) reste vide, sans effet.
- Formspree `mppqagwr` : chaque inscription envoie un courriel à keating.sands@gmail.com **et** mamselleruiz@gmail.com (adresse vérifiée).
- Mamselle a reçu le PDF.
- **Reste** : dans Squarespace, l'enregistrement DNS `CNAME cadeau → ray-charles.github.io` et la redirection `/cadeau -> https://cadeau.veacademy.studio 301` (vérifié le 2026-10-06 : pas encore faits). Ensuite Claude active HTTPS et teste.

## 2026-10-06 (soir) · EN LIGNE

- DNS Squarespace : `CNAME cadeau → ray-charles.github.io` ajouté (après reconnexion Google de Charles).
- HTTPS : certificat bloqué, débloqué en retirant puis remettant le domaine Pages ; `https_enforced` actif.
- Test réel sur la page en ligne : inscription « Prueba Claude » (keating.sands+cadeautest@gmail.com) acceptée par Formspree, PDF ouvert, courriel « Regalo PDF: nueva descarga » reçu.
- Courriel envoyé à Mamselle avec le lien, dans le fil « PDF LEAD MAGNET POUR EL CAFECITO ».
- **Lien à partager : https://cadeau.veacademy.studio**
- Pas fait : redirection `veacademy.studio/cadeau`. Le site Squarespace est verrouillé (cadenas sur « Edit site ») et ses réglages n'offrent pas les redirections d'URL. À reprendre si le forfait Squarespace est réactivé.

## 2026-10-07 · Page réduite à un simple formulaire

- Demande de Charles : le public sort d'un webinaire avec Mamselle, déjà convaincu. La page n'est plus qu'un formulaire sur un seul écran, sans défilement : logo, titre « Domina tu voz y gana confianza », nombre, apellido, correo, teléfono, bouton « Descargar mi cuaderno ».
- Après l'envoi Formspree, le navigateur va directement au PDF (plus d'écran de confirmation). Pixel `Lead` conservé.
- Vérifié : aucun défilement à 375×812 ni à 1366×650, formulaire centré, le PDF est bien appelé après l'envoi. Photo de Mamselle retirée (plus utilisée).

## 2026-10-07 · Page « ¿Y ahora? » retirée du PDF

- Demande de Charles : supprimer l'ancienne page 17 (« ¿Y ahora? », webinaire [fecha y hora], [enlace]). Le PDF passe à 17 pages : le geste 09 mène directement à l'offre membresía (17 $ CAD), lien du bouton intact.
