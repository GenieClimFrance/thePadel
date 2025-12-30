# 🍪 Cookies et RGPD - THE PADEL

## ✅ Statut Actuel : PAS DE BANDEAU NÉCESSAIRE

Votre site THE PADEL **n'utilise aucun cookie nécessitant un consentement**.

### Services utilisés :

- ✅ **Vercel Analytics** : Analytics respectueux de la vie privée (pas de cookies, pas de consentement nécessaire)
- ✅ **Google Maps (iframe)** : Carte de localisation simple sur la page contact (pas de consentement nécessaire)
- ✅ **Tarteaucitron.js** : Installé mais désactivé (prêt si besoin)

### Vous êtes conforme RGPD ! 🎉

Sans cookies nécessitant un consentement, vous n'avez **pas besoin** de bandeau. C'est même mieux pour vos utilisateurs (pas de popup ennuyeuse) !

---

## 🔧 Configuration

### Actuellement

Le composant `CookieConsent.astro` est **désactivé** dans `src/layouts/Layout.astro` :

```astro
// import CookieConsent from "../components/CookieConsent.astro"; // ✅ Désactivé
```

**Aucun service nécessitant un consentement.**

### Si vous ajoutez des services plus tard

**Services nécessitant le bandeau :**

- Google Analytics
- Facebook Pixel
- Vidéos YouTube embarquées
- Google Maps avec API JavaScript
- Publicités

**Pour activer le bandeau plus tard :**

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

### Pourquoi l'iframe Google Maps ne nécessite pas de consentement ?

L'iframe d'embed Google Maps est considérée comme un contenu légitime de localisation. Elle n'utilise pas l'API JavaScript de Google Maps et ne dépose pas de cookies de tracking. C'est donc acceptable sans consentement pour une simple carte de localisation.

### Les cookies de session sont-ils concernés ?

Non, les cookies **strictement nécessaires** (authentification, panier, sécurité) ne nécessitent pas de consentement.

---

**Besoin d'aide ?** Consultez `COOKIES_GUIDE.md` ou contactez votre développeur.
