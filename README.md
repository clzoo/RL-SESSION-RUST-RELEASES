# RL SESSION Rust

**RL SESSION Rust** est un outil gratuit et indépendant pour **Rocket League**, développé par **CLZOO** pour Windows x64 (**testé sur Windows 11** ; les autres versions ne sont pas encore validées). Il affiche les statistiques de session, les joueurs en match et, lorsque Tracker Network les fournit, les MMR réels.

> **Projet de fan non officiel.** RL SESSION n'est ni conçu, ni approuvé, ni soutenu par Epic Games ou Psyonix. La mention exigée par Epic et les informations de propriété intellectuelle sont dans [NOTICE_EPIC.md](NOTICE_EPIC.md). Aucun partenariat officiel n'est revendiqué.

## Télécharger

Consultez l'onglet **Releases** de ce dépôt pour récupérer les fichiers de **v0.1.0** :

- `RL-SESSION-RUST-Setup-0.1.0-x64.exe` — installateur Windows (pour l'utilisateur actuel ou tous les utilisateurs).
- `RL-SESSION-RUST-Portable-0.1.0-x64.zip` — version portable autonome.
- `SHA256SUMS.txt` — empreintes de contrôle des deux fichiers.

**Les programmes ne sont pas signés numériquement.** Windows SmartScreen peut afficher un avertissement ; vérifiez la provenance et les empreintes SHA-256 avant toute installation. Ne neutralisez pas votre antivirus pour installer RL SESSION.

## Installation et stockage

Fermez RL SESSION depuis la zone de notification avant une mise à niveau. Sauvegardez les profils et sessions avant une première désinstallation ou un changement de mode de stockage.

L'installateur conserve normalement les données de chaque utilisateur dans `%LOCALAPPDATA%\RL-SESSION-RUST`. Le ZIP portable s'utilise après extraction **complète** et stocke par défaut les données à côté de l'exécutable, dans `data/`, sauf configuration de stockage explicite. Le dossier `mmr-transport` (Chromium) et `assets/ranks` doivent rester à côté du programme.

Pour vérifier le téléchargement dans PowerShell :

```powershell
(Get-FileHash -Algorithm SHA256 '.\RL-SESSION-RUST-Setup-0.1.0-x64.exe').Hash
```

Comparez le résultat à la ligne correspondante de `SHA256SUMS.txt` disponible dans la même Release.

## Fonctions de v0.1.0

- Compteur de sessions Rocket League, résultats confirmés, modes séparés et historique conservé entre les redémarrages.
- Module joueurs : équipes, vrais MMR transmis par Tracker lorsque disponibles, 23 illustrations de rangs et informations de match.
- Dashboard **Ma session**, **Réglages**, **Réglages avancés** et **À propos** ; diagnostic intégré à l'interface.
- Profils Tracker, raccourcis manette, mises en page enregistrées, icône de notification Windows et sauvegardes locales.

Le MMR dépend d'un service externe non officiel ; des restrictions de réseau, CAPTCHA, indisponibilités ou changements de l'API Tracker peuvent empêcher temporairement la récupération. RL SESSION ne contourne pas les CAPTCHA et n'invente pas de valeurs.

## Confidentialité, sécurité et droits

- [Sécurité, limites et signalement](SECURITE.md)
- [Licence d'utilisation propriétaire](LICENCE-UTILISATION.md)
- [Avis aux fans et droits des marques](NOTICE_EPIC.md)
- [Notes de la version 0.1.0](NOTES_VERSION_0.1.0.md)

**Ce dépôt public héberge uniquement la documentation de distribution et les téléchargements binaires des Releases.** Le code de l'application est conservé dans un dépôt privé distinct. Les archives « Source code » créées automatiquement par GitHub ne contiennent que les fichiers publics de ce dépôt, et non le code de l'application.

Copyright © 2026 CLZOO. Logiciel propriétaire distribué gratuitement.
