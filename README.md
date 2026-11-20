# RL SESSION (Rust)

**RL SESSION Rust** est un outil gratuit et indépendant pour **Rocket League**, développé par **CLZOO** pour Windows x64 (**testé sur Windows 11** ; les autres versions ne sont pas encore validées). Il affiche les statistiques de session, les joueurs en match et, lorsque Tracker Network les fournit, les MMR réels.

> **Projet de fan non officiel.** RL SESSION n'est ni conçu, ni approuvé, ni soutenu par Epic Games ou Psyonix. Aucun partenariat officiel n'est revendiqué.

**Mention Epic Games requise par la section 1.10 de sa politique de contenu de fan :**

> Des parties des supports utilisés sont des marques déposées et/ou des travaux soumis aux droits d’auteur d’Epic Games, Inc. Tous droits réservés par Epic. Ce produit n’est pas officiel et n’a pas l'approbation d'Epic.

Lire les [informations légales et conditions de la politique Epic](NOTICE_EPIC.md).

## Télécharger

**Version publique actuellement disponible : v0.1.2.** La v0.1.3 est validée sur Windows et sa distribution est en préparation ; elle ne doit pas être annoncée comme téléchargeable tant que ses fichiers n'apparaissent pas dans les [Releases GitHub](https://github.com/clzoo/RL-SESSION-RUST-RELEASES/releases).

Pour la version publiée de votre choix, récupérer dans sa Release :

- `RL-SESSION-RUST-Setup-<version>-x64.exe` — installateur Windows (utilisateur actuel ou tous les utilisateurs).
- `RL-SESSION-RUST-Portable-<version>-x64.zip` — version portable autonome.
- `SHA256SUMS.txt` — empreintes de contrôle des deux fichiers.

Les [notes de la v0.1.3](NOTES_VERSION_0.1.3.md) sont disponibles. **Les programmes ne sont pas signés numériquement.** Windows SmartScreen peut afficher un avertissement ; vérifiez la provenance et les empreintes SHA-256 avant toute installation. Ne neutralisez pas votre antivirus.

## Installation et stockage

Fermez RL SESSION depuis la zone de notification avant une mise à niveau. Sauvegardez les profils et sessions avant une première désinstallation ou un changement de mode de stockage.

L'installateur conserve normalement les données de chaque utilisateur dans `%LOCALAPPDATA%\RL-SESSION-RUST`. Le ZIP portable s'utilise après extraction **complète** et stocke par défaut les données à côté de l'exécutable, dans `data/`, sauf configuration de stockage explicite. Le dossier `mmr-transport` (Chromium) doit rester à côté du programme. Les rangs sont représentés par des **codes colorés**, sans sous-dossier d'illustrations `assets/ranks` dans les nouveaux téléchargements.

Pour vérifier le téléchargement (exemple pour la v0.1.3 lorsqu'elle sera publiée) dans PowerShell :

```powershell
(Get-FileHash -Algorithm SHA256 '.\RL-SESSION-RUST-Setup-0.1.3-x64.exe').Hash
```

Comparez le résultat à la ligne correspondante de `SHA256SUMS.txt` disponible dans la même Release.

## Fonctions principales

- Compteur de sessions Rocket League, résultats confirmés, modes séparés et historique conservé entre les redémarrages.
- Module joueurs : équipes, vrais MMR transmis par Tracker lorsque disponibles, **23 codes de rangs colorés** (NC, B1 à GC3, SSL) et informations de match, sans illustrations de rangs.
- Dashboard **Ma session**, **Réglages**, **Réglages avancés** et **À propos** ; diagnostic intégré à l'interface.
- Profils Tracker, raccourcis manette, mises en page enregistrées, icône de notification Windows et sauvegardes locales.

Le MMR dépend d'un service externe non officiel ; des restrictions de réseau, CAPTCHA, indisponibilités ou changements de l'API Tracker peuvent empêcher temporairement la récupération. RL SESSION ne contourne pas les CAPTCHA et n'invente pas de valeurs.

## Confidentialité, sécurité et droits

- [Sécurité, limites et signalement](SECURITE.md)
- [Licence d'utilisation propriétaire](LICENCE-UTILISATION.md)
- [Avis aux fans et droits des marques](NOTICE_EPIC.md)
- [Notes de la version 0.1.3](NOTES_VERSION_0.1.3.md)
- [Notes de la version 0.1.0](NOTES_VERSION_0.1.0.md)

**Ce dépôt public héberge uniquement la documentation de distribution et les téléchargements binaires des Releases.** Le code de l'application est conservé dans un dépôt privé distinct. Les archives « Source code » créées automatiquement par GitHub ne contiennent que les fichiers publics de ce dépôt, et non le code de l'application.

Copyright © 2026 CLZOO. Logiciel propriétaire distribué gratuitement.
