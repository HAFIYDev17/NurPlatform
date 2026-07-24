# Vitrine Nûr Platform

Page unique, statique. Pas de dépendance, pas de build : `index.html` se suffit.

## Déployer sur Vercel

1. vercel.com → "Add New" → "Project"
2. "Deploy without Git", ou relie le dépôt `nur-platform`
3. Glisse ce dossier entier
4. Deploy

Tu obtiens une adresse du type `nur-platform.vercel.app`.

## Brancher la connexion

Trois liens mènent aujourd'hui vers `https://aecs-black.vercel.app/login` :

- le bouton « Se connecter » de la barre du haut
- le bouton « Ouvrir mon espace » du hero
- la ligne NûrGest dans la liste des applications

Remplace l'adresse aux trois endroits :

    href="https://aecs-black.vercel.app/login"
    →
    href="https://TON-ADRESSE/login"

**Ces trois liens sont provisoires.** Ils pointent vers une application
précise, alors que la vitrine est celle d'une plateforme. À terme ils mènent
tous au même endroit, la porte, qui authentifie puis renvoie chacun vers
l'outil qui le concerne : NûrGest pour un directeur d'école, NûrOps pour un
conducteur de travaux. Le visiteur ne choisit pas son application, elle le
reconnaît.

Tant que cette porte n'existe pas, garder les trois liens sur une application
qui fonctionne vaut mieux que les pointer vers une page qui n'est pas prête.

## Le domaine

Quand tu auras `nur.yt`, tu le branches dans Vercel (Settings → Domains). La
vitrine devient l'adresse publique, et la porte vit sur un sous-domaine :

    nur.yt          la vitrine (ce dossier)
    app.nur.yt      la porte, puis les applications

## Modifier la page

Les zones modifiables sont signalées dans `index.html` par des commentaires
`✎`. Les principales :

- **le hero** : surtitre, titre, chapô
- **le nœud** : pour renommer une application, changer le `<text>` du satellite
- **l'anneau** : NûrProgress. Ce n'est pas un quatrième satellite, c'est le
  cercle qui passe par les trois. Les satellites sont posés exactement dessus
  (128 du centre) : si tu déplaces l'un d'eux, garde cette distance ou
  l'anneau cessera de les toucher.
- **les applications** : un bloc `<a class="app">` par ligne. États possibles :
  `prod` (ambre), `pilote` (clair), `attente` (gris)

Les couleurs vivent dans les variables CSS en tête de fichier (`--nuit`,
`--lumiere`, `--ivoire`). Ne les change qu'à cet endroit.
