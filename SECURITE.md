# Sécurité et bonnes pratiques

## Origine et intégrité des fichiers

Téléchargez RL SESSION Rust uniquement depuis les fichiers joints aux Releases officielles de **ce dépôt public**. Comparez le SHA-256 du setup ou du ZIP au fichier `SHA256SUMS.txt` joint à la même version. Une empreinte confirme l'intégrité par rapport au manifeste publié, pas à elle seule l'absence de code malveillant.

## Signature numérique

La version **v0.1.0 est non signée** (`NotSigned` avec Authenticode). Windows SmartScreen peut demander une confirmation. Ce n'est ni une preuve de malveillance, ni une garantie de sûreté. Examinez toujours les alertes ; **ne désactivez pas Defender ou votre antivirus** pour l'exécuter.

## Données et réseau

Les profils, dispositions et sessions sont conservés localement dans le dossier configuré. Le transport MMR intégré contacte Tracker Network pour accéder aux données de classement : son service peut répondre avec des erreurs 403/429, demander un CAPTCHA, ou devenir indisponible. Le programme n'effectue pas de contournement automatisé des restrictions de Tracker. Il ne faut pas promettre un MMR permanent.

La version portable doit rester dans un dossier où les données peuvent être écrites et conserver son sous-dossier `mmr-transport`. Cette variante affiche les rangs en texte coloré et ne distribue aucun PNG de rang. Lors d'une mise à niveau ou désinstallation, sauvegardez les données et arrêtez complètement l'application dans la zone de notification.

## Dépendances

Avant la publication, un audit `npm audit` complet a rapporté **11 entrées de vulnérabilité** (6 élevées, 5 modérées) dans l'arbre de la chaîne de construction Electron, et 0 avec `--omit=dev`. L'analyse a identifié principalement des bibliothèques de correspondance de motifs utilisées à la compilation. Le contenu JavaScript de l'archive Electron distribuée a été vérifié séparément. **Le filtrage des devDependencies ne garantit pas l'absence de vulnérabilités dans le runtime Electron/Chromium.** Il n'est pas prétendu que cette version possède une certification de sécurité.

## Signaler un problème

Utilisez les issues de ce dépôt public pour décrire les bugs et les erreurs de téléchargement **sans y publier** de jetons, de fichiers de sauvegarde, de logs contenant vos identifiants ou de liens privés. Pour signaler une vulnérabilité sensible, contactez l'éditeur par un canal privé avant de publier les détails ; aucun contact privé spécifique n'est indiqué dans ce dépôt.
