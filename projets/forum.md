# Forum national de l'entrepreneuriat — site officiel

**Site :** [jcibamakoelite.ml](https://jcibamakoelite.ml/) · **Organisateur :** JCI Bamako Élite · **Rôle :** conception, développement full stack

Site officiel du Forum national de l'entrepreneuriat, à Bamako : présentation de l'événement, programme, actualités, inscription en ligne et billet électronique contrôlé à l'entrée.

**Expérience utilisateur :** le participant s'inscrit depuis son téléphone et reçoit un billet QR code. À l'entrée, un simple scan suffit.

![Page d'accueil du Forum](../captures/forum/accueil.jpg)

## Fonctionnalités

- **Site public** : programme, intervenants, actualités, formulaire de contact.
- **Inscription en ligne**, validée ou refusée depuis le back-office.
- **Billet électronique** avec QR code, contrôlé à l'entrée par scan.
- **Annuaire des exposants et partenaires**, avec cartes de visite (vCard) téléchargeables.
- **Back-office** : contenus du site, inscriptions, messages, paramètres, statistiques.

## Architecture

```mermaid
flowchart LR
    P["Site public<br/>React"] --> API["API REST<br/>Node.js · Express"]
    BO["Back-office<br/>scan des billets"] --> API
    API --> F[("Données JSON<br/>et fichiers")]
```

## Technologies

| Couche | Technologies |
|---|---|
| Front-end | React, Vite, Tailwind CSS, Framer Motion, QR codes |
| API | Node.js, Express, JWT, Helmet, Multer, limitation du nombre de requêtes |

## Captures du site

| Programme et présentation | Inscription par QR code | Mobile |
|---|---|---|
| ![Programme](../captures/forum/a-propos.jpg) | ![Inscription](../captures/forum/inscription-qr.jpg) | ![Version mobile](../captures/forum/mobile.jpg) |

---

[← Retour au portfolio](../README.md) · Code source privé, démonstration sur demande.
