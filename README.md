# RevStar Summit '25 - MC Cue Cards

Application mobile de cue cards pour l'animation de la conférence RevStar Summit 2025.

## Fonctionnalités

✅ **Navigation intuitive** : Tape à gauche pour revenir, à droite pour avancer (ou swipe)
✅ **Schedule rapide** : Bouton "Schedule" pour voir toutes les interventions chronologiques
✅ **Mode édition** : Modifier les cartes directement dans l'app (sauvegarde locale)
✅ **Design mobile-first** : Optimisé pour téléphone, texte très lisible
✅ **45 cartes** : Toutes tes notes organisées par section

## Déploiement sur Netlify

### Option 1 : Drag & Drop (plus rapide)

1. Va sur [app.netlify.com](https://app.netlify.com)
2. Clique sur "Add new site" → "Deploy manually"
3. Drag & drop le dossier `revstar-cue-cards` complet
4. Ton site sera en ligne en ~30 secondes!

### Option 2 : Avec Git (recommandé pour mises à jour faciles)

```bash
cd revstar-cue-cards
git init
git add .
git commit -m "Initial commit: RevStar cue cards"

# Créer un repo GitHub
# Puis:
git remote add origin <ton-repo-url>
git push -u origin main
```

Ensuite sur Netlify:
1. "Add new site" → "Import an existing project"
2. Connecte ton GitHub
3. Sélectionne le repo
4. Deploy!

### Custom domain (optionnel)

Dans les settings Netlify, tu peux ajouter un sous-domaine genre `revstar.francois.com` ou utiliser le domaine Netlify gratuit.

## Utilisation

### Navigation
- **Tap gauche** de l'écran = carte précédente
- **Tap droite** de l'écran = carte suivante
- **Swipe** aussi supporté
- **Flèches clavier** pour tester sur desktop

### Schedule
- Bouton **"Schedule"** en haut à droite
- Affiche toutes tes 12 interventions chronologiques
- Tap pour fermer

### Mode édition
- Bouton **"Edit"** en haut à droite
- Édite le JSON des cartes
- **Save Changes** = sauvegarde dans le navigateur (localStorage)
- **Reset to Default** = retour aux cartes originales
- Les changements persistent même si tu fermes l'app!

## Structure d'une carte

```json
{
  "section": "Welcome",
  "title": "Introduction",
  "bullets": [
    "Premier point",
    "Deuxième point",
    "Troisième point"
  ]
}
```

## Notes techniques

- Fichier unique: `index.html` (tout-en-un)
- Pas de dépendances externes
- Fonctionne 100% offline après chargement
- Données sauvegardées dans localStorage du navigateur
- Mobile-first, responsive

## Support

Besoin de modifications? Demande à Claude! 🤖
