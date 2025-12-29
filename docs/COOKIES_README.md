# 🍪 Cookies et RGPD - THE PADEL

## ✅ Statut Actuel : PAS DE BANDEAU NÉCESSAIRE

Votre site THE PADEL **n'utilise aucun cookie nécessitant un consentement**.

### Pourquoi ?

- **Vercel Analytics** ne nécessite pas de consentement (pas de cookies, données anonymisées)
- Aucun tracker tiers (Google Analytics, Facebook Pixel, etc.)
- Pas de vidéos YouTube ou Google Maps embarquées

### Vous êtes conforme RGPD ! 🎉

Sans cookies nécessitant un consentement, vous n'avez **pas besoin** de bandeau de cookies. C'est même mieux pour vos utilisateurs (pas de popup ennuyeuse) !

---

## 🔧 Configuration

### Actuellement

Le composant `CookieConsent.astro` est **installé mais désactivé** dans `src/layouts/Layout.astro` :

```astro
// import CookieConsent from "../components/CookieConsent.astro"; // ✅ Désactivé
```

### Si vous ajoutez des services plus tard

**Services nécessitant le bandeau :**

- Google Analytics
- Facebook Pixel
- Vidéos YouTube embarquées
- Google Maps embarquées
- Publicités

**Pour réactiver le bandeau :**

1. Décommentez l'import dans `src/layouts/Layout.astro`
2. Configurez les services dans `src/components/CookieConsent.astro`
3. Consultez `COOKIES_GUIDE.md` pour le détail

---

## 📚 Documentation

- **Guide complet** : `docs/COOKIES_GUIDE.md`
- **Politique de confidentialité** : `/politique-de-confidentialite`
- **Mentions légales** : `/mentions-legales`

---

## ❓ Questions Fréquentes

### Est-ce que je suis conforme RGPD sans bandeau ?

**Oui !** Si vous n'utilisez pas de cookies nécessitant un consentement, vous n'avez pas besoin de bandeau. Vous devez quand même avoir une politique de confidentialité et respecter les autres obligations RGPD.

### Qu'est-ce que Vercel Analytics ?

Vercel Analytics est un outil d'analyse web respectueux de la vie privée :

- ❌ Pas de cookies
- ✅ Données anonymisées
- ✅ Conforme RGPD par défaut
- ✅ Pas besoin de consentement

### Quand dois-je activer le bandeau ?

Activez le bandeau uniquement si vous ajoutez des services qui utilisent des cookies non essentiels ou des trackers (Google Analytics, Facebook Pixel, etc.).

### Les cookies de session sont-ils concernés ?

Non, les cookies **strictement nécessaires** (authentification, panier, sécurité) ne nécessitent pas de consentement.

---

**Besoin d'aide ?** Consultez `COOKIES_GUIDE.md` ou contactez votre développeur.
