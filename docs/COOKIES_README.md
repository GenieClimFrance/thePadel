# 🍪 Cookies et RGPD - THE PADEL

## ✅ Statut Actuel : BANDEAU ACTIVÉ

Votre site THE PADEL utilise **Google Maps** sur la page contact, qui nécessite un consentement RGPD.

### Services configurés :

- ✅ **Google Maps** : Carte interactive sur la page contact (nécessite consentement)
- ✅ **Vercel Analytics** : Analytics respectueux de la vie privée (pas de consentement nécessaire)
- ✅ **Tarteaucitron.js** : Bandeau de gestion des cookies (activé et stylisé)

### Vous êtes conforme RGPD ! 🎉

Le bandeau de cookies est actif et permet à vos visiteurs d'accepter ou refuser Google Maps. La carte sera floutée jusqu'à ce que l'utilisateur donne son consentement.

---

## 🔧 Configuration

### Actuellement

Le composant `CookieConsent.astro` est **activé** dans `src/layouts/Layout.astro` avec Google Maps configuré :

```astro
import CookieConsent from "../components/CookieConsent.astro"; // ✅ Activé
```

**Services actifs :**

- Google Maps (page contact)

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

### Est-ce que je suis conforme RGPD avec le bandeau ?

**Oui !** Le bandeau Tarteaucitron est conforme RGPD et gère automatiquement le consentement pour Google Maps. Les utilisateurs peuvent accepter ou refuser, et leur choix est mémorisé.

### Qu'est-ce que Vercel Analytics ?

Vercel Analytics est un outil d'analyse web respectueux de la vie privée :

- ❌ Pas de cookies
- ✅ Données anonymisées
- ✅ Conforme RGPD par défaut
- ✅ Pas besoin de consentement

### Comment fonctionne le bandeau pour Google Maps ?

Lorsqu'un utilisateur visite la page contact, la carte Google Maps est **floutée** avec un bouton "Accepter Google Maps". Une fois qu'il clique, la carte s'affiche normalement et son choix est mémorisé pour 13 mois.

### Les cookies de session sont-ils concernés ?

Non, les cookies **strictement nécessaires** (authentification, panier, sécurité) ne nécessitent pas de consentement.

---

**Besoin d'aide ?** Consultez `COOKIES_GUIDE.md` ou contactez votre développeur.
