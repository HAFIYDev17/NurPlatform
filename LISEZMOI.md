# Vitrine Nûr Platform

## Déployer sur Vercel en deux minutes

1. Va sur vercel.com, "Add New" puis "Project"
2. Choisis "Deploy without Git" (ou crée un dépôt `nur-platform`)
3. Glisse ce dossier entier
4. Deploy

Tu obtiens une adresse du type `nur-platform.vercel.app`.

## Brancher la connexion

Dans `index.html`, les liens de connexion pointent vers `https://aecs-black.vercel.app/login`. Remplace-les
par l'adresse de ton application :

    href="https://aecs-black.vercel.app/login"   →   href="https://aecs-black.vercel.apphttps://aecs-black.vercel.app/login"

Il y en a trois : le bouton du haut, le bouton principal du hero, et la ligne
NûrGest dans la liste des applications.

## Le domaine

Quand tu auras `nurgest.fr` ou `nur.yt`, tu le branches dans Vercel
(Settings > Domains). La page vitrine devient ton adresse publique, et
l'application vit sur `app.` ou `https://aecs-black.vercel.app/login`.
