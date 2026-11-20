# RL SESSION Rust v0.1.3 — Windows x64

**Statut : notes de distribution préparées.** La publication de la release et la présence des fichiers téléchargeables doivent être vérifiées séparément.

## Nouveautés

- Deux présentations MMR : tableau complet ou deux tableaux séparés côte à côte, avec largeur adaptative lors du redimensionnement.
- Correction du centrage des colonnes et assouplissement de la largeur minimale du tableau de classements pour préserver la visibilité des statistiques W, L et WIN %.
- Noms complets des rangs en français dans les tableaux (Platine, Diamant, Champion, Grand Champion, etc.).
- Surbrillance de la ligne du mode actif, y compris lors d'un changement par le raccourci manette.
- Thèmes de tableau pétrole et violet, commandés par deux icônes compactes sans fond coloré.
- Valeur et libellé CASUAL grisés, MMR Casual en gras et présentation compacte.
- Date de dernière réception du MMR placée à côté du titre MMR ; tableau et descriptions allégés.
- Le nombre des dix derniers matchs confirmés par mode reste calculé localement ; aucun résultat ni classement fictif n'est ajouté.

## Distribution

Fichiers attendus pour **Windows x64** :

- `RL-SESSION-RUST-Setup-0.1.3-x64.exe` : installateur Windows.
- `RL-SESSION-RUST-Portable-0.1.3-x64.zip` : dossier autonome avec le composant Chromium `mmr-transport`.
- `SHA256SUMS.txt` : empreintes SHA-256 des deux fichiers ci-dessus.

Le ZIP doit être extrait **intégralement** avant lancement et le dossier `mmr-transport` doit rester à côté du programme.

## Mise à niveau

1. Fermer RL SESSION depuis la zone de notification.
2. Sauvegarder les données de `%LOCALAPPDATA%\RL-SESSION-RUST`.
3. Exécuter l'installateur v0.1.3.
4. Vérifier le maintien des profils Tracker, statistiques de session, réglages et dispositions.

La mise à niveau et le fonctionnement de l'installateur v0.1.3 ont été validés par l'utilisateur sur Windows. Le ZIP et les empreintes doivent être contrôlés avant publication.

## Transparence

RL SESSION est un logiciel de fan indépendant, non officiel, sans affiliation à Epic Games, Psyonix ou Tracker Network. Certaines fonctionnalités MMR dépendent des réponses de Tracker et peuvent être momentanément indisponibles (CAPTCHA, restrictions, panne). Le logiciel ne contourne pas les CAPTCHA.

**Les exécutables ne sont pas signés numériquement.** Vérifier l'origine GitHub et les empreintes SHA-256 avant utilisation ; ne pas désactiver les protections de Windows.

Ce dépôt public contient seulement la distribution et sa documentation. Les fichiers `Source code` générés automatiquement par GitHub ne contiennent pas le dépôt Rust privé.
