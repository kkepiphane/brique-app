# Brique — ton app de dépenses, brique par brique

Une application web installable (PWA), 100 % gratuite :
- pas de serveur, pas d'abonnement ;
- fonctionne **hors ligne** une fois installée ;
- tes données restent **sur ton téléphone** (personne d'autre ne les voit) ;
- chaque personne à qui tu partages le lien a **sa propre app vide**, avec ses propres données.

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

- **Android (Chrome)** : ouvre le lien › menu ⋮ › **Installer l'application** (ou « Ajouter à l'écran d'accueil »).
- **iPhone (Safari)** : ouvre le lien › bouton Partager › **Sur l'écran d'accueil**.

## Le rappel du soir (gratuit)

Sans serveur, une app web ne peut pas programmer une notification toute seule. Deux solutions :
- dans **Profil › Sauvegarde**, touche « Ajouter un rappel quotidien à 21 h (agenda) » : un événement quotidien s'ajoute à ton agenda ;
- ou crée une alarme quotidienne à 21 h sur ton téléphone, nommée « Brique ».

## Tes données

- Elles sont stockées dans le navigateur de ton téléphone. Si tu **vides les données de Chrome** ou désinstalles le navigateur, elles sont perdues.
- Fais une copie régulièrement : **Profil › Sauvegarde › Exporter**. Garde le fichier (ou le texte) dans tes notes ou envoie-le-toi sur WhatsApp.
- Pour changer de téléphone : **Exporter** sur l'ancien, **Importer** sur le nouveau.

## Mettre à jour l'app

Remplace `index.html` dans ton dépôt. Si tu modifies aussi `sw.js`, change le nom du cache (`brique-v1` → `brique-v2`) pour que les téléphones prennent la nouvelle version.
