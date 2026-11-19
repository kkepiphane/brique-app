# Brique

Application web installable (PWA) pour gérer ses dépenses au quotidien et construire son rêve, brique par brique.

- 100 % gratuite, sans serveur ni compte
- Fonctionne **hors ligne** une fois installée
- Les données restent **sur le téléphone** de chaque personne

**Ouvrir l'app :** https://kkepiphane.github.io/brique-app/

## Installer sur le téléphone

- **Android (Chrome)** : ouvre le lien › menu ⋮ › **Installer l'application**
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
Si tu modifies `sw.js` ou les icônes, change le nom du cache (`brique-v1` → `brique-v2`) pour que les téléphones prennent la nouvelle version.

Guide détaillé : [LISEZMOI.md](LISEZMOI.md)
