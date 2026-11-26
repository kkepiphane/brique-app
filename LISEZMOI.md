# Brique — ton app de dépenses, brique par brique

Une application web installable (PWA), 100 % gratuite :
- pas de serveur, pas d'abonnement ;
- fonctionne **hors ligne** une fois installée ;
- tes données restent **sur ton téléphone** (personne d'autre ne les voit) ;
- chaque personne à qui tu partages le lien a **sa propre app vide**, avec ses propres données.

## Ton profil : d'où vient ton argent ?

Au début, l'app te demande d'où vient ton argent. Ça change le calcul de ton **budget du jour** :

- **Salaire chaque mois** : ton argent doit tenir jusqu'à ta prochaine paie.
- **Revenus irréguliers** (freelance, business…) : jusqu'à ta prochaine rentrée, ou 30 jours par prudence si tu ne sais pas.
- **Les deux** : salaire + revenus en plus.
- **Étudiant(e), sans salaire** : ton argent vient des parents, de la famille, d'une bourse ou de petits jobs.

### Tu es étudiant(e) ?

Choisis à quel rythme tu reçois ton argent :

| Rythme | Exemple | Comment l'app calcule |
| --- | --- | --- |
| **Chaque jour** | Tes parents te donnent 1 000 F chaque matin | Ton budget du jour = l'argent reçu ce jour-là. Note-le chaque jour dans **Revenu** : le montant de la dernière fois est déjà proposé. |
| **Chaque semaine** | Tu reçois 7 000 F chaque lundi | Ton argent doit tenir jusqu'au lundi suivant. |
| **Chaque mois** | Bourse ou argent du mois le 5 | Ton argent doit tenir jusqu'au 5 du mois suivant. |
| **Ça varie** | Tu reçois de l'argent de temps en temps | Jusqu'à la date que tu indiques, ou 30 jours par prudence. |

Quand tu notes un revenu, tu choisis : *Parents, famille*, *Bourse*, *Petit job*, *Cadeau* ou *Autre*. Recevoir l'argent des parents ou la bourse démarre une nouvelle période.
Tu as aussi une catégorie de dépenses **Études** (photocopies, fournitures).

Tu peux changer de profil ou de rythme à tout moment : **Profil › Mon argent vient de › Modifier**.

### Le loyer

L'app te demande si tu paies un loyer :
- **Oui** : ajoute son montant, il sera mis de côté chaque mois avant de calculer ton budget du jour ;
- **Non, je suis logé(e)** (famille, foyer, chez un proche) : pas de loyer, tu ajoutes seulement tes autres charges si tu en as (scolarité, forfait internet, tontine…).

## Tes catégories

Tu peux créer tes propres catégories de dépenses : touche **+ Nouvelle** quand tu ajoutes une dépense, ou va dans **Profil › Mes catégories**. Si tu en retires une, les dépenses déjà notées gardent leur nom.

## Contenu du dossier

| Fichier | Rôle |
| --- | --- |
| `index.html` | Toute l'application |
| `manifest.webmanifest` | Nom, couleurs et icônes pour l'installation |
| `sw.js` | Fonctionnement hors ligne |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` | Icônes |

## Mettre l'app en ligne gratuitement (GitHub Pages)

1. Crée un dépôt public sur GitHub, par exemple `brique`.
2. Dépose les 6 fichiers à la racine du dépôt (bouton « Add file » › « Upload files »).
3. Dans le dépôt : **Settings › Pages › Build and deployment**, choisis la branche `main`, dossier `/ (root)`, puis **Save**.
4. Après une minute, ton app est en ligne à l'adresse `https://<ton-pseudo>.github.io/brique/`.

Autres hébergeurs gratuits possibles : Netlify, Cloudflare Pages ou Vercel. Il suffit d'y déposer le dossier.

> L'app doit être servie en **https** pour s'installer et marcher hors ligne. Ouvrir `index.html` directement depuis le téléphone fonctionne aussi, mais sans installation ni mode hors ligne.

## L'installer sur ton téléphone

- **Android (Chrome)** : ouvre le lien, un bandeau « Installe Brique » apparaît, touche **Installer**. Sinon : menu ⋮ › **Installer l'application** (ou « Ajouter à l'écran d'accueil »).
- **iPhone (Safari)** : ouvre le lien › bouton Partager › **Sur l'écran d'accueil**. (Sur iPhone, il faut utiliser Safari.)
- Le bouton **Installer l'app sur cet appareil** est aussi dans **Profil › Sauvegarde**.

## Le rappel du soir (gratuit)

Sans serveur, une app web ne peut pas programmer une notification toute seule. Deux solutions :
- dans **Profil › Sauvegarde**, touche « Ajouter un rappel quotidien à 21 h (agenda) » : un événement quotidien s'ajoute à ton agenda ;
- ou crée une alarme quotidienne à 21 h sur ton téléphone, nommée « Brique ».

## Tes données

- Elles sont stockées dans le navigateur de ton téléphone. Si tu **vides les données de Chrome** ou désinstalles le navigateur, elles sont perdues.
- Fais une copie régulièrement : **Profil › Sauvegarde › Exporter**. Garde le fichier (ou le texte) dans tes notes ou envoie-le-toi sur WhatsApp.
- Pour changer de téléphone : **Exporter** sur l'ancien, **Importer** sur le nouveau.

## Mettre à jour l'app

Remplace `index.html` dans ton dépôt. Si tu modifies aussi `sw.js` ou les icônes, augmente le numéro du cache dans `sw.js` (par exemple `brique-v4` → `brique-v5`) pour que les téléphones prennent la nouvelle version.
