# RL SESSION Rust v0.1.0 — première version Windows

**Version :** 0.1.0  
**Plateforme :** Windows x64 — validation effectuée sur Windows 11  
**Distribution :** logiciel gratuit et propriétaire, code source non public  
**Signature numérique :** non signée

## Première version

RL SESSION Rust propose une application Windows native Rust/GPUI dédiée au suivi des parties Rocket League :

- Trois fenêtres : compteur, panneau des joueurs et Dashboard.
- Sessions et résultats de match confirmés, par mode et tous modes, sauvegardés entre les redémarrages.
- Vrais MMR récupérés via Tracker Network lorsque le service les transmet, sans interpolation ni faux classement.
- 23 codes de rangs colorés (NC, B1–B3, S1–S3, G1–G3, P1–P3, D1–D3, C1–C3, GC1–GC3, SSL), sans illustrations ni logos de rangs.
- Actualisation du MMR personnel en début de match ; requêtes des autres joueurs volontairement limitées.
- Avertissement conditionnel en cas de CAPTCHA/indisponibilité Tracker, sans contournement.
- Dashboard avec Ma session, Réglages, Réglages avancés et À propos ; terminal de diagnostic intégré.
- Profils Tracker, dispositions sauvegardées, raccourcis manette et icône dans la zone de notification.
- Installateur permettant une installation personnelle ou pour tous les utilisateurs ; distribution portable indépendante.

## Validation de la version

La candidate précédente, qui contenait des illustrations de rangs, a passé les tests Windows et GitHub Actions, ainsi que la mise à niveau RC1, la désinstallation/réinstallation et les contrôles de données/MMR. **La nouvelle candidate à rangs textuels a été compilée localement avec succès le 18 novembre 2026** : installateur et ZIP portable générés. Les tests en partie, la vérification indépendante des hashes et la nouvelle recette Windows restent à effectuer **avant publication**. Les anciens SHA-256 et exécutables de la Release en brouillon ne sont pas ceux de cette variante.

**Empreintes SHA-256 :** voir `SHA256SUMS.txt` joint à la Release. Vérifiez vos fichiers téléchargés avant de les utiliser.

## Précautions importantes

Les exécutables ne disposent pas de signature Authenticode ; le statut `NotSigned` a été constaté sur l'EXE et le setup. SmartScreen ou l'antivirus peuvent donc demander une vérification. **N'ajoutez pas d'exclusion de sécurité automatiquement.**

Une revue de `npm audit` du processus de fabrication a relevé 11 signalements (6 élevés et 5 modérés) principalement propagés dans les dépendances de construction Electron ; le filtre `--omit=dev` en relevait zéro. Le paquet JS embarqué a été vérifié pour éviter d'inclure par erreur des modules npm de construction. Cela ne constitue pas une certification de sécurité d'Electron ou de Chromium. Les mises à jour de sécurité et les changements des services externes seront surveillés pour les versions suivantes.

**Projet non officiel — mention Epic Games (section 1.10 de la politique de contenu de fan) :**

> Des parties des supports utilisés sont des marques déposées et/ou des travaux soumis aux droits d’auteur d’Epic Games, Inc. Tous droits réservés par Epic. Ce produit n’est pas officiel et n’a pas l'approbation d'Epic.

RL SESSION n'est ni développé, ni approuvé, ni soutenu par Epic Games ou Psyonix. Lire [NOTICE_EPIC.md](NOTICE_EPIC.md) et la [politique d'Epic Games](https://legal.epicgames.com/epicgames/fan-art-policy?lang=fr).
