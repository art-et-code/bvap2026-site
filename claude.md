# Projet BVAP 2026

Site web de campagne pour la liste **"Bien Vivre à Perros, aujourd'hui et demain"** aux élections municipales de mars 2026 à Perros-Guirec (Côtes-d'Armor, Bretagne).

## Infos clés

- **Tête de liste** : Erven Léon (maire sortant)
- **Élections** : 15 et 22 mars 2026
- **Site** : bienvivreaperros.fr
- **Réseaux sociaux** : @bvap2026 (Facebook, Instagram, YouTube)
- **WhatsApp** : https://whatsapp.com/channel/0029VbCPgKh0gcfDOBz2OX2G

## Structure du site

### Pages HTML
- `index.html` - Page d'accueil (photo équipe, engagements, actualités, agenda)
- `programme.html` - Programme complet (3 engagements + logement/urbanisme)
- `logement.html` - Article "Un logement pour tous"
- `urbanisme.html` - Article "Comprendre les règles d'urbanisme"
- `equipe.html` - L'équipe (30 colistiers)
- `actualites.html` - Actualités et agenda
- `galerie.html` - Galerie photos et vidéos
- `presse.html` - Espace presse (revue de presse, documents, réseaux sociaux)
- `contact.html` - Contact et dons
- `mentions-legales.html` - Mentions légales

### Dossiers
- `images/` - Images du site (logos, éléments graphiques, photo-groupe-accueil.jpg)
- `images/presse/` - Articles de presse (scans)
- `a-publier/` - Contenus à publier
  - `photos/` - Photos de campagne (galerie)
  - `communiques/` - Communiqués de presse (PDF)
  - `documents de campagne/` - Tracts, affiches (PDF)
  - `programme/` - Contenus du programme (photos, articles .md)
  - `articles_presse.csv` - Liste des articles de presse

## Charte graphique

### Couleurs CSS
- `--bleu-marine` / `--bleu-ocean` : #3D4A5C
- `--magenta` : #E6007E
- `--cyan` : #00BCD4
- `--granite` : #6b7280

### Polices
- Titres : Playfair Display
- Corps : Source Sans 3
- Hero : Oswald
- Script : Caveat

## Conventions

### Éditorial
- Site en français
- Ton professionnel et institutionnel
- Respect du RGPD (pas de données personnelles sans consentement)

### Noms de fichiers presse
Format : `YYYY-MM-DD-Source-Titre.extension`
Exemple : `2026-01-28-Le-Telegramme-La-place-Chez-Titine-fait-peau-neuve.jpeg`

### Workflow Git
- Branche de travail : `dev`
- Branche de production : `main`
- Branches feature : `feature/xxx` (ex: `feature/programme`)
- Déploiement : GitHub Pages (automatique sur push main)

### Process de publication
1. Ajouter les fichiers dans `a-publier/`
2. Mettre à jour le HTML correspondant
3. Commit sur `dev` puis merge sur `main`

### Publication différée
Pour publier une page plus tard (ex: programme) :
1. Travailler sur une branche `feature/xxx`
2. Publier les pages prêtes via `dev` → `main`
3. Merger la branche feature quand tout est prêt

## Axes du programme

1. **Une ville bienveillante** — "Prendre soin de chacun, à chaque âge de la vie"
   - Solidarité, Inclusion, Transmission

2. **Une ville responsable** — "Protéger notre patrimoine naturel, préparer l'avenir"
   - Écologie, Patrimoine, Citoyenneté

3. **Une ville vivante** — "Une ville qui bouge, une ville qui rassemble"
   - Sport, Culture, Proximité

## Contact

- Email : contact@bienvivreaperros.fr
- Local de campagne : 9 rue de la Poste, 22700 Perros-Guirec
