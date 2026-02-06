# Mise à jour de l'agenda

Met à jour les événements passés dans l'agenda sur la page Actualités.

## Instructions

1. Identifier la date du jour
2. Lire le fichier `actualites.html` et identifier tous les événements dans les sections :
   - Réunions publiques
   - Tournée des quartiers (Près de chez vous)
   - Sur les marchés
   - Dates importantes
3. Pour chaque événement dont la date est passée, appliquer le style "passé" :
   - Ajouter `style="opacity: 0.7;"` sur le `div.event-item`
   - Changer la couleur de fond du `div.event-date-box` en `style="background: var(--granite);"`
   - Ajouter `<span style="font-weight: normal; color: var(--granite);">— Passée</span>` après le titre dans le `h4`
4. Ne pas modifier les événements déjà marqués comme passés
5. Informer l'utilisateur des événements mis à jour
6. Proposer de commit et push sur main

## Format HTML événement passé

```html
<div class="event-item" style="opacity: 0.7;">
    <div class="event-date-box" style="background: var(--granite);">
        <span class="day">JJ</span>
        <span class="month">MOIS</span>
    </div>
    <div class="event-content">
        <h4>Titre de l'événement <span style="font-weight: normal; color: var(--granite);">— Passée</span></h4>
        <p>Description...</p>
        <div class="event-location">Lieu</div>
    </div>
</div>
```

## Notes

- Les mois dans le HTML sont en majuscules : JAN, FÉV, MARS, etc.
- Comparer les dates en tenant compte de l'année 2026
- Les événements avec `style="background: var(--magenta);"` (élections) ne doivent pas être grisés même une fois passés
