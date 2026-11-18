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
- 23 illustrations de rangs et panneau joueurs validés en partie.
- Actualisation du MMR personnel en début de match ; requêtes des autres joueurs volontairement limitées.
- Avertissement conditionnel en cas de CAPTCHA/indisponibilité Tracker, sans contournement.
- Dashboard avec Ma session, Réglages, Réglages avancés et À propos ; terminal de diagnostic intégré.
- Profils Tracker, dispositions sauvegardées, raccourcis manette et icône dans la zone de notification.
- Installateur permettant une installation personnelle ou pour tous les utilisateurs ; distribution portable indépendante.

## Validation de la version

L'installateur et le ZIP ont été construits sur Windows, testés en situation réelle, avec vérification de l'icône EXE et des 23 PNG. Les tests Rust et la compilation Windows ont réussi sur GitHub Actions. La mise à niveau RC1, la désinstallation/réinstallation, la restauration des fichiers utilisateur, les vrais MMR et le ZIP extrait hors du dépôt ont été validés.

**Empreintes SHA-256 :** voir `SHA256SUMS.txt` joint à la Release. Vérifiez vos fichiers téléchargés avant de les utiliser.

## Précautions importantes

Les exécutables ne disposent pas de signature Authenticode ; le statut `NotSigned` a été constaté sur l'EXE et le setup. SmartScreen ou l'antivirus peuvent donc demander une vérification. **N'ajoutez pas d'exclusion de sécurité automatiquement.**

Une revue de `npm audit` du processus de fabrication a relevé 11 signalements (6 élevés et 5 modérés) principalement propagés dans les dépendances de construction Electron ; le filtre `--omit=dev` en relevait zéro. Le paquet JS embarqué a été vérifié pour éviter d'inclure par erreur des modules npm de construction. Cela ne constitue pas une certification de sécurité d'Electron ou de Chromium. Les mises à jour de sécurité et les changements des services externes seront surveillés pour les versions suivantes.

**Projet non officiel** : lire [NOTICE_EPIC.md](NOTICE_EPIC.md) et la [politique d'Epic Games](https://legal.epicgames.com/epicgames/fan-art-policy?lang=fr) avant la diffusion.
