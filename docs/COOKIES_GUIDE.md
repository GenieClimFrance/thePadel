# 🍪 Guide de Gestion des Cookies - THE PADEL

## 🎯 Statut Actuel : BANDEAU DÉSACTIVÉ

**Le bandeau de cookies est actuellement désactivé** car votre site n'utilise **aucun cookie nécessitant un consentement**.

### Pourquoi pas de bandeau ?

- ✅ **Vercel Analytics** ne nécessite pas de consentement (pas de cookies, anonymisé)
- ✅ **Google Maps (iframe)** : Simple carte de localisation sans API JavaScript
- ✅ Pas de trackers tiers (Google Analytics, Facebook Pixel, etc.)
- ✅ Meilleure expérience utilisateur sans popup inutile

**Vous êtes conforme RGPD sans bandeau !** 🎉

---

## 📦 Installation (Déjà Prête)

Tarteaucitron.js est installé et prêt à être activé si vous ajoutez des services nécessitant un consentement.

## 🎨 Personnalisation

Le bandeau de cookies a été stylisé aux couleurs de THE PADEL :

- **Couleur primaire** : Vert néon (#12EF97) pour les boutons "Accepter"
- **Couleur secondaire** : Bleu (#008AEF) pour les boutons "Refuser"
- **Fond** : Gris foncé (#2B2E36) pour le bandeau
- **Police** : Impact pour les boutons, Raleway pour le texte

## 📱 Fonctionnalités

### Ce qui est inclus :

✅ Bandeau de consentement conforme RGPD  
✅ Bouton "Tout accepter"  
✅ Bouton "Tout refuser"  
✅ Bouton "Personnaliser"  
✅ Icône flottante pour rouvrir le panneau  
✅ Lien vers votre politique de confidentialité  
✅ Design responsive (mobile + desktop)  
✅ Animation fluide

### Position du bandeau :

- **Desktop & Mobile** : En bas de l'écran
- **Icône** : En bas à gauche (réouvre le panneau)

## 🔧 Comment Ajouter des Services

### 1. Google Analytics (GA4)

Si vous voulez ajouter Google Analytics plus tard, décommentez dans `CookieConsent.astro` :

```javascript
tarteaucitron.user.gtagUa = "G-VOTRE-ID-ANALYTICS";
(tarteaucitron.job = tarteaucitron.job || []).push("gtag");
```

### 2. YouTube (vidéos embarquées)

Pour les vidéos YouTube, décommentez :

```javascript
(tarteaucitron.job = tarteaucitron.job || []).push("youtube");
```

Puis dans votre HTML, remplacez :

```html
<iframe src="https://www.youtube.com/embed/VIDEO_ID"></iframe>
```

Par :

```html
<div class="youtube_player" videoID="VIDEO_ID" width="560" height="315"></div>
```

### 3. Google Maps

Pour les cartes Google Maps embarquées :

```javascript
(tarteaucitron.job = tarteaucitron.job || []).push("googlemaps");
```

Puis dans votre HTML :

```html
<div
  class="googlemaps_embed"
  maps="https://www.google.com/maps/embed?pb=..."
  width="600"
  height="450"
></div>
```

### 4. Facebook Pixel

Si vous utilisez Facebook Ads :

```javascript
tarteaucitron.user.facebookpixelId = "VOTRE_PIXEL_ID";
(tarteaucitron.job = tarteaucitron.job || []).push("facebookpixel");
```

## 🎯 À Propos de Vercel Analytics

**Bonne nouvelle !** Vercel Analytics est respectueux de la vie privée et conforme RGPD par défaut car :

- ❌ Pas de cookies utilisés
- ✅ Données anonymisées
- ✅ Pas de tracking cross-site
- ✅ Conforme aux recommandations de la CNIL

**Vous n'avez donc pas besoin de demander le consentement pour Vercel Analytics !**

C'est pour cette raison que le bandeau est actuellement désactivé sur votre site.

## 🔄 Comment Réactiver le Bandeau

Si vous ajoutez plus tard des services nécessitant un consentement (Google Analytics, YouTube, etc.), voici comment réactiver le bandeau :

### Étape 1 : Décommenter dans `src/layouts/Layout.astro`

```astro
// Ligne à décommenter :
import CookieConsent from "../components/CookieConsent.astro";

// Et dans le body :
<CookieConsent />
```

### Étape 2 : Configurer les services dans `src/components/CookieConsent.astro`

Décommentez les services que vous utilisez (voir section "Comment Ajouter des Services" ci-dessous)

### Étape 3 : Tester

1. Ouvrez votre site en navigation privée
2. Le bandeau devrait apparaître automatiquement
3. Testez les 3 boutons :
   - **Tout accepter** : accepte tous les cookies
   - **Tout refuser** : refuse tous les cookies non essentiels
   - **Personnaliser** : permet de choisir service par service

### Pour réafficher le bandeau (une fois activé) :

- Cliquez sur l'**icône verte** en bas à gauche
- Ou ajoutez `#tarteaucitron` à la fin de l'URL

### Pour réinitialiser les cookies :

```javascript
// Dans la console du navigateur
tarteaucitron.userInterface.reset();
```

## 📊 Statistiques et Monitoring

Pour voir quels utilisateurs acceptent/refusent les cookies, vous pouvez :

1. **Consulter les cookies dans le navigateur** :

   - Cherchez le cookie `tarteaucitron`
   - Format : `!service=true/false`

2. **Ajouter un tracking personnalisé** :

```javascript
// Ajoutez dans CookieConsent.astro
tarteaucitron.user.analyticsMore = function () {
  console.log("Cookie consent:", tarteaucitron.state);
  // Envoyez à votre système d'analytics si besoin
};
```

## 🎨 Personnalisation Avancée

### Changer la position du bandeau :

Dans `CookieConsent.astro`, ligne `orientation`:

```javascript
"orientation": "bottom", // ou "top"
```

### Changer la position de l'icône :

```javascript
"iconPosition": "BottomLeft", // BottomRight, TopRight, TopLeft
```

### Modifier les couleurs :

Les styles sont dans la section `<style is:global>` de `CookieConsent.astro`

## 📝 Conformité RGPD

### Situation actuelle (sans bandeau) :

✅ **Pas de cookies nécessitant un consentement** = Pas besoin de bandeau  
✅ **Vercel Analytics conforme** par défaut (anonymisé, pas de cookies)  
✅ **Politique de confidentialité** en place avec lien dans le footer  
✅ **Mentions légales** accessibles  
✅ **Droits RGPD** documentés (accès, rectification, effacement, etc.)

### Ce que vous devez quand même faire (RGPD général) :

📋 **Compléter les informations manquantes** dans les mentions légales (SIRET, RCS, etc.)  
📋 **Former votre équipe** sur la gestion des données personnelles  
📋 **Tenir un registre** des traitements de données (si vous collectez des données clients)  
📋 **Sécuriser** les données personnelles (mots de passe, paiements, etc.)

### Si vous activez le bandeau plus tard :

✅ Lien vers la politique de confidentialité (déjà configuré)  
✅ Bouton "Tout refuser" aussi visible que "Accepter" (déjà stylisé)  
✅ Pas de cookies avant consentement (géré par Tarteaucitron)  
✅ Conservation du choix pendant 13 mois (configuré)  
✅ Possibilité de modifier son choix à tout moment (icône flottante)

## 🆘 Dépannage

### Le bandeau n'apparaît pas :

1. Vérifiez la console du navigateur (F12)
2. Videz le cache du navigateur
3. Vérifiez que le cookie `tarteaucitron` n'existe pas déjà

### Le bandeau est mal positionné :

1. Vérifiez qu'il n'y a pas de conflit avec d'autres z-index
2. Ajustez le CSS dans `CookieConsent.astro`

### Les services ne fonctionnent pas :

1. Vérifiez que vous avez bien décommenté le service
2. Vérifiez la syntaxe du code HTML (voir exemples ci-dessus)
3. Acceptez les cookies pour ce service

## 📚 Ressources

- **Documentation Tarteaucitron** : https://tarteaucitron.io/
- **Liste complète des services** : https://opt-out.ferank.eu/en/install/
- **CNIL (cookies)** : https://www.cnil.fr/fr/cookies-et-autres-traceurs
- **RGPD** : https://www.cnil.fr/fr/reglement-europeen-protection-donnees

## 🚀 Prochaines Étapes

### Situation actuelle ✅

Vous n'avez **rien à faire** ! Votre site est conforme RGPD sans bandeau de cookies.

### Si vous ajoutez des services plus tard :

1. **Réactiver le bandeau** (voir section "Comment Réactiver le Bandeau")
2. **Configurer les services** nécessaires (voir section "Comment Ajouter des Services")
3. **Tester** sur tous les navigateurs et appareils
4. **Mettre à jour** la politique de confidentialité avec la liste des cookies
5. **Former l'équipe** aux bonnes pratiques RGPD

### Services qui nécessiteraient le bandeau :

- ⚠️ Google Analytics (GA4)
- ⚠️ Facebook Pixel
- ⚠️ Vidéos YouTube embarquées
- ⚠️ Google Maps embarquées
- ⚠️ Publicités (Google Ads, etc.)
- ⚠️ Chat en direct (certains services)

### Services qui NE nécessitent PAS le bandeau :

- ✅ Vercel Analytics (ce que vous utilisez actuellement)
- ✅ Plausible Analytics
- ✅ Fathom Analytics
- ✅ Cookies essentiels (authentification, panier, sécurité)

---

**Besoin d'aide ?** Contactez votre développeur ou consultez la documentation officielle de Tarteaucitron.js
