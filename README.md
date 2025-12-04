# Resto Universitaire — README

## Équipe

- Salem Diber
- Adem Miladi
- Skander Ben Salah
- Nizar Chaieb

## Exécution rapide (Tailwind via CDN — pas de build local requis)

1) Cloner le projet

```powershell
git clone <URL_DU_REPO>
cd <NOM_DU_PROJET>
```

2) Ouvrir dans le navigateur

- Le projet utilise Tailwind via CDN directement dans les pages (`<script src="https://cdn.tailwindcss.com"></script>`).
- Ouvrez `index.html` ou `menus.html` dans votre navigateur, ou servez le dossier :

```powershell
npx serve -s . -l 5500
# puis ouvrez http://localhost:5500
```

3) (Optionnel) Utiliser un build local de Tailwind

Si vous préférez compiler Tailwind localement (optionnel), gardez `input.css`/`output.css` et utilisez les commandes suivantes :

```powershell
npm install -D tailwindcss
npx tailwindcss init
npx tailwindcss -i ./input.css -o ./output.css --watch
```

Remarque : le projet fonctionne parfaitement avec le CDN — vous pouvez supprimer `input.css`/`output.css` si vous n'utilisez pas de build local.

---

## Problèmes rencontrés & solutions apportées

1) Icônes Lucide n'apparaissaient pas — corrigé en important l'UMD et en appelant `createIcons()`.
2) Images & cheminements — toutes les images ont été déplacées dans `assets/` et les chemins mis à jour.
3) Conflits d'ombres et bordures sur les cards — ajustements Tailwind appliqués.

