# Ajout de photos à la galerie

Ajoute les nouvelles photos à la galerie sur la page Galerie.

## Instructions

1. Vérifier les nouvelles photos dans `a-publier/photos/` (fichiers non trackés par git)
2. Identifier la catégorie appropriée selon le nom du fichier :
   - `Réunion-de-travail` → Section "Réunions de travail"
   - `Tractage` → Section "Tractage"
   - `Lancement-campagne` → Section "Lancement de campagne"
   - `Photo-de-Groupe` → Section "Photo de groupe"
   - `Reunion-publique` → Section "Réunions publiques"
   - Autre → Demander à l'utilisateur
3. Ajouter les photos dans la section correspondante de `galerie.html`
4. Utiliser le format HTML existant :

```html
<a href="a-publier/photos/[NOM_FICHIER]" class="gallery-link" style="display: block; border-radius: 10px; overflow: hidden; cursor: pointer;">
    <img src="a-publier/photos/[NOM_FICHIER]" alt="[DESCRIPTION]" style="width: 100%; height: 200px; object-fit: cover;">
</a>
```

5. Pour les photos de groupe, utiliser un format plus grand (max-width: 600px, height: auto)
6. Respecter l'ordre chronologique (plus récent en haut de chaque section)
7. Informer l'utilisateur des photos ajoutées
8. Proposer de commit et push sur main
