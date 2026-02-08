# SWF → page web (Ruffle) → intégration ÉLÉA (iframe)

Contenu :
- `index.html` : page web qui charge Ruffle + le SWF
- `animation.swf` : votre animation

## 1) Mise en ligne sur GitHub Pages
1. Créer un dépôt GitHub (ex. `combustion-carbone`).
2. Uploader **à la racine du dépôt** : `index.html` + `animation.swf`.
3. Aller dans **Settings → Pages**.
4. **Source** : `Deploy from a branch`.
5. **Branch** : `main` + dossier `/ (root)`.
6. Enregistrer : GitHub vous donne une URL du type `https://VOTRE_USER.github.io/combustion-carbone/`.

## 2) Vérification avant ÉLÉA
- Ouvrir l’URL GitHub Pages.
- Vérifier que l’animation est **entièrement visible** (boutons compris).
- Si le bas est rogné : augmenter la hauteur dans `index.html` (section `#player`).

## 3) Iframe à coller dans ÉLÉA
Dans ÉLÉA, coller un iframe simple (hauteur légèrement > à celle validée sur GitHub Pages).

Exemple :
```html
<iframe
  src="https://VOTRE_USER.github.io/combustion-carbone/"
  width="100%"
  height="650"
  style="border:0; border-radius:10px; overflow:hidden;"
  scrolling="no"
  allowfullscreen>
</iframe>
```

Astuce : si une barre de défilement apparaît, augmenter la `height` (ex. 700, 750…).
