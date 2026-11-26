# Brique

Application web installable (PWA) pour gérer ses dépenses au quotidien et construire son rêve, brique par brique.

- 100 % gratuite, sans serveur ni compte
- Fonctionne **hors ligne** une fois installée
- Les données restent **sur le téléphone** de chaque personne

**Ouvrir l'app :** https://kkepiphane.github.io/brique-app/

## Pour qui ?

| Profil | D'où vient l'argent | Budget du jour calculé jusqu'à… |
| --- | --- | --- |
| Salaire chaque mois | Un salaire à date fixe | la prochaine paie |
| Revenus irréguliers | Freelance, contrats, business | la prochaine rentrée (ou 30 jours par prudence) |
| Les deux | Salaire + revenus en plus | la prochaine paie |
| **Étudiant(e), sans salaire** | Parents, famille, bourse, petits jobs | voir ci-dessous |

### Étudiants

L'étudiant choisit à quel rythme il reçoit son argent :

- **Chaque jour** : le budget du jour correspond à l'argent reçu ce jour-là. La saisie d'un revenu reprend le montant de la dernière fois.
- **Chaque semaine** : il choisit le jour (lundi, mardi…). Son argent doit tenir jusqu'à ce jour-là la semaine suivante.
- **Chaque mois** : il indique le jour du mois.
- **Ça varie** : l'app compte jusqu'à la prochaine rentrée prévue, ou sur 30 jours par prudence.

Les revenus proposés sont adaptés (*Parents, famille · Bourse · Petit job · Cadeau*), ainsi que les catégories : *Études* apparaît, *Business* est masqué. Les charges fixes (scolarité, forfait…) restent mensuelles, quel que soit le rythme choisi.

### Loyer

À l'inscription, l'app demande : **« Tu paies un loyer ? »**
- *Oui* : le loyer est ajouté aux charges fixes.
- *Non, je suis logé(e)* (famille, foyer, chez un proche) : aucune charge de loyer n'est ajoutée.

### Autres fonctions

- Catégories de dépenses personnalisées (bouton « + Nouvelle », ou **Profil › Mes catégories**)
- Proposition d'installation sur le téléphone (bandeau « Installe Brique »)
- Rêve à financer, rituel du soir, sauvegarde par export / import

## Installer sur le téléphone

- **Android (Chrome)** : ouvre le lien, puis touche **Installer** dans le bandeau, ou menu ⋮ › **Installer l'application**
- **iPhone (Safari)** : ouvre le lien › Partager › **Sur l'écran d'accueil**

## Fichiers

| Fichier | Rôle |
| --- | --- |
| `index.html` | Toute l'application |
| `manifest.webmanifest` | Nom, couleurs et icônes pour l'installation |
| `sw.js` | Fonctionnement hors ligne |
| `icon-*.png` | Icônes |

## Mettre à jour

Modifie les fichiers, puis `git commit` et `git push` : GitHub Pages republie en une minute.
Si tu modifies `sw.js` ou les icônes, augmente le numéro du cache dans `sw.js` (par exemple `brique-v4` → `brique-v5`) pour que les téléphones prennent la nouvelle version.

Guide détaillé : [LISEZMOI.md](LISEZMOI.md)
