# Publication du site bienvivreaperros.fr

## Prérequis
- Accès au repo GitHub : `github.com/art-et-code/bvap2026-site`
- Accès à Cloudflare pour le domaine `bienvivreaperros.fr`

---

## Étape 1 : Activer GitHub Pages

1. Aller sur le repo GitHub : https://github.com/art-et-code/bvap2026-site
2. Cliquer sur **Settings** (onglet en haut)
3. Dans le menu de gauche, cliquer sur **Pages**
4. Dans **Source**, sélectionner :
   - **Deploy from a branch**
   - Branch : **main**
   - Folder : **/ (root)**
5. Cliquer sur **Save**

> Le site sera d'abord accessible sur : `https://art-et-code.github.io/bvap2026-site`

---

## Étape 2 : Configurer le domaine personnalisé (GitHub)

1. Toujours dans **Settings** → **Pages**
2. Dans la section **Custom domain**, entrer : `bienvivreaperros.fr`
3. Cliquer sur **Save**
4. Cocher **Enforce HTTPS** (peut prendre quelques minutes à s'activer)

> GitHub va automatiquement créer un fichier `CNAME` dans le repo.

---

## Étape 3 : Configurer Cloudflare DNS

1. Se connecter à Cloudflare : https://dash.cloudflare.com
2. Sélectionner le domaine `bienvivreaperros.fr`
3. Aller dans **DNS** → **Records**
4. Supprimer les anciens enregistrements A/CNAME pour @ et www (si existants)
5. Ajouter les enregistrements suivants :

| Type  | Nom (Name) | Contenu (Target)       | Proxy |
|-------|------------|------------------------|-------|
| CNAME | @          | art-et-code.github.io  | Oui   |
| CNAME | www        | art-et-code.github.io  | Oui   |

---

## Étape 4 : Configurer Cloudflare SSL

1. Aller dans **SSL/TLS** → **Overview**
2. Sélectionner le mode : **Full** (pas "Full (strict)")

---

## Étape 5 : Redirection www vers racine (optionnel)

Pour rediriger `www.bienvivreaperros.fr` vers `bienvivreaperros.fr` :

1. Aller dans **Rules** → **Page Rules**
2. Cliquer sur **Create Page Rule**
3. Configurer :
   - URL : `www.bienvivreaperros.fr/*`
   - Setting : **Forwarding URL** (301 - Permanent Redirect)
   - Destination : `https://bienvivreaperros.fr/$1`
4. Cliquer sur **Save and Deploy**

---

## Vérification

Après 10-30 minutes de propagation :

- [ ] `https://bienvivreaperros.fr` affiche le site
- [ ] `https://www.bienvivreaperros.fr` redirige vers la racine
- [ ] Le cadenas HTTPS est présent
- [ ] Toutes les pages fonctionnent

---

## Dépannage

### Le site n'apparaît pas
- Vérifier que GitHub Pages est bien activé (Settings → Pages)
- Attendre 10 minutes pour la propagation DNS

### Erreur de certificat SSL
- Vérifier que Cloudflare SSL est en mode "Full" (pas "Full strict")
- Vérifier que "Enforce HTTPS" est coché sur GitHub

### Erreur 404
- Vérifier que la branche **main** est sélectionnée
- Vérifier que `index.html` est à la racine du repo

---

## Contact support
- GitHub Pages : https://docs.github.com/en/pages
- Cloudflare : https://developers.cloudflare.com/dns/
