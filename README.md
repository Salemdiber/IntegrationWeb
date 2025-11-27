# Resto Universitaire — README

## Équipe
-Salem Diber
-Adem Miladi 
-Skander Ben Salah 
-Nizar Chaieb

(Replacez les noms et responsabilités ci-dessus selon la composition réelle de votre équipe.)

---

## Exécution du projet (rapide)
Le projet est une application front-end statique. Voici plusieurs façons de lancer localement :

1) Serveur Python (rapide, PowerShell) :


```powershell
npm install
npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
```


---

## Contenu ajouté / fichiers modifiés
- `src/index.html` : header, hero (titre), deux cards (Réserver / Composer), section Informations, cards d'horaires et menu du jour, footer.
- Ajout de classes CSS inline (`.hero-title`, `.card`) dans le head de `src/index.html`.

---

## Problèmes rencontrés & solutions apportées
1) Icônes Lucide n'apparaissaient pas
- Problème : le projet référençait un chemin CSS/JS incorrect sur le CDN (`/dist/lucide.min.css` et `/dist/lucide.min.js`), provoquant des erreurs 404.
- Solution : utiliser le bundle UMD fourni par le package (`/dist/umd/lucide.min.js`) et initialiser `lucide.createIcons()` après le DOMContentLoaded. Les éléments `<i data-lucide="...">` sont transformés en SVG.

2) Images & cheminements
- Problème : lors d'ouverture directe du fichier (`file://`) certains navigateurs bloquent les requêtes CDN ou les images relatives.
- Solution : recommander d'exécuter un serveur local (voir section Exécution) ou utiliser des chemins absolus/relatifs corrects (ex: `/reserver.jpg`).

3) Conflits d'ombres et bordures sur les cards
- Problème : ombres Tailwind par défaut et styles personnalisés pouvaient entrer en conflit.
- Solution : centraliser le rendu des cartes via la classe `.card` (border `#E5E7EB`, double `box-shadow`, `border-radius: 8px`) et retirer les `shadow-lg` redondants.

