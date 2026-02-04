# Ajout d'articles à la revue de presse

Ajoute les nouveaux articles de presse au site.

## Instructions

1. Lire le fichier `a-publier/articles_presse.csv` pour identifier les nouveaux articles
2. Comparer avec les articles déjà présents dans `presse.html`
3. Pour chaque nouvel article :
   - Vérifier que l'image existe dans `images/presse/`
   - Ajouter l'article dans la section "Revue de Presse" de `presse.html`
   - Respecter l'ordre chronologique décroissant (plus récent en haut)
4. Utiliser le format HTML existant :

```html
<a href="images/presse/[NOM_FICHIER]" target="_blank" class="presse-card">
    <div class="presse-source">[SOURCE]</div>
    <h4 class="presse-title">[TITRE]</h4>
    <div class="presse-date">[DATE]</div>
    <span class="presse-cta">Lire l'article →</span>
</a>
```

5. Informer l'utilisateur des articles ajoutés
6. Proposer de commit et push sur main
