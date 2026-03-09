# Guide de Configuration des Médias (Logo, Favicon, Captures d'écran)

Ce guide vous explique comment personnaliser l'identité visuelle de votre documentation VesselIQ étape par étape.

## 1. Logo de l'application

Les logos sont gérés dans le dossier `logo/` et configurés dans le fichier `docs.json`.

### Étapes pour mettre à jour :
1. **Préparez vos fichiers** : Idéalement au format SVG pour une netteté parfaite, mais le PNG/JPG fonctionne aussi.
2. **Remplacez les fichiers existants** dans votre dossier local :
   - `logo/light.svg` (affiché en mode clair)
   - `logo/dark.svg` (affiché en mode sombre)
3. **Si vous utilisez d'autres noms ou formats (ex: PNG)** :
   - Ouvrez `docs.json`.
   - Modifiez la section `logo` comme ceci :
     ```json
     "logo": {
       "light": "/logo/mon-logo-clair.png",
       "dark": "/logo/mon-logo-sombre.png"
     }
     ```

---

## 2. Favicon (L'icône de l'onglet du navigateur)

Le favicon est l'icône qui apparaît à côté du titre de la page dans votre navigateur.

### Étapes pour mettre à jour :
1. **Remplacez le fichier** `favicon.svg` à la racine de votre projet par votre propre icône.
2. **Si vous utilisez un format différent (ex: .ico ou .png)** :
   - Enregistrez votre fichier (ex: `favicon.png`) à la racine.
   - Ouvrez `docs.json` et modifiez la ligne suivante :
     ```json
     "favicon": "/favicon.png"
     ```

---

## 3. Captures d'écran (Screenshots) de l'application

Il est fortement recommandé d'ajouter des captures d'écran pour chaque onglet (Dashboard, Consultations, etc.) afin d'illustrer les fonctionnalités.

### Étape 1 : Capturer et enregistrer
1. Prenez une capture d'écran de l'onglet souhaité dans votre application.
2. Enregistrez l'image dans le dossier `images/` de votre projet de documentation.
3. Utilisez des noms de fichiers clairs, par exemple : `images/tableau-de-bord.png`.

### Étape 2 : Ajouter à la documentation
Pour afficher l'image dans une page (fichier `.mdx`), utilisez cette syntaxe :

```md
![Description de l'image](/images/tableau-de-bord.png)
```

### Optionnel : Utiliser un cadre (Frame)
Pour un rendu plus professionnel avec une bordure élégante, utilisez le composant `<Frame>` de Mintlify :

```md
<Frame>
  ![Tableau de Bord VesselIQ](/images/tableau-de-bord.png)
</Frame>
```

---

## 4. Conseils pour un rendu Premium

*   **Format des captures** : Essayez de prendre vos captures d'écran avec la même taille de fenêtre pour garder une cohérence visuelle.
*   **Optimisation** : Si vos images sont lourdes (plus de 500 Ko), passez-les sur un site comme [TinyPNG](https://tinypng.com/) pour accélérer le chargement de la documentation.
*   **Mode Sombre** : Si possible, prenez des captures d'écran en mode clair ET en mode sombre pour que les utilisateurs s'y retrouvent dans les deux thèmes.
