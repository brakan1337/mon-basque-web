# Mon basque — site public

**👉 [brakan1337.github.io/mon-basque-web](https://brakan1337.github.io/mon-basque-web/)**

Entraînement au basque, niveau A1 : on construit des phrases en appuyant sur
les mots, dans les deux sens de traduction, et dix conversations se jouent
réplique après réplique. Aucune vie, aucune limite.

**La progression n'est pas enregistrée** : elle vit le temps de l'onglet et
repart à zéro à chaque visite. C'est voulu — rien n'est stocké dans le
navigateur.

## Ce dépôt ne contient pas de code

Seulement le site déjà construit. Le code source vit dans un dépôt privé
séparé, `brakan1337/mon-basque`, qui sert aussi à fabriquer l'application
Android. Ne rien modifier ici à la main : tout serait écrasé à la publication
suivante.

Trois fichiers méritent une explication :

| Fichier | Pourquoi |
|---|---|
| `.nojekyll` | sans lui, GitHub Pages ignore `_expo/`, et les dossiers commençant par `_` en général — la page resterait blanche |
| `404.html` | copie de `index.html` : c'est le repli qui fait démarrer l'application sur n'importe quelle URL profonde |
| `_expo/` | le paquet JavaScript, construit avec la base `/mon-basque-web` pour que le routeur se retrouve sous ce sous-chemin |

## Republier

Depuis le dépôt source :

```bash
npx expo export --platform web
```

puis copier le contenu de `dist/` ici, remettre `.nojekyll` et recopier
`index.html` en `404.html`.
