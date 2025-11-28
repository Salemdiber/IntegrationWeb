# Resto Universitaire — README

## Équipe


## Exécution du projet (rapide)




## Exécution du projet (rapide)

1) Cloner le projet

```bash
git clone <URL_DU_REPO>
cd <NOM_DU_PROJET>
```

2) Installer Tailwind CSS (optionnel si vous préférez utiliser le CDN en développement)

Assurez-vous d'avoir Node.js et npm installés, puis (si vous voulez un build local) :

```bash
npm install -D tailwindcss
npx tailwindcss init
```

3) Créer `input.css` (dans `src/`) si absent

Créez `src/input.css` avec le contenu suivant :

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

4) Compiler Tailwind en mode watch

Cette commande génère `src/output.css` et reste en écoute pour recompilation :

```bash
npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
```

5) Ouvrir le projet dans un navigateur (serveur local recommandé)

```
http://localhost:5500/src/menus.html
```

Ou, si vous préférez utiliser `npx serve` :

```bash
npx serve -s . -l 5500
```


---

## Problèmes rencontrés & solutions apportées
1) Icônes Lucide n'apparaissaient pas

2) Images & cheminements

3) Conflits d'ombres et bordures sur les cards

