# Serena Giuliano — site officiel

Site vitrine de la romancière **Serena Giuliano**, autrice de huit romans parus
au Cherche-Midi, chez Robert Laffont et chez Calmann-Lévy, et traduite auprès de
plus d'un million de lecteurs.

Conçu et développé de bout en bout : architecture, design, contenu, conformité.

🔗 **[serenagiuliano.fr](https://serenagiuliano.fr)** *(bientôt en ligne)*

![Page d'accueil](captures/accueil.jpg)

---

## Ce que fait le site

Une bibliographie complète et vérifiée, une page d'actualités qui se tient à
jour toute seule, un agenda de dédicaces, et les pages légales qu'impose un site
français.

| Page | Rôle |
|---|---|
| **Accueil** | Dernière parution et dernier roman, côte à côte, puis une biographie courte |
| **Livres** | Les 8 romans, les 3 albums jeunesse et le récit numérique |
| **Fiche livre** | Synopsis, prix, éditions successives, liens d'achat vérifiés |
| **Actualités** | Toutes les parutions, de la plus récente à la plus ancienne |
| **Agenda** | Salons et séances de dédicace |
| **Mentions légales · Confidentialité** | LCEN et RGPD |

![Page Livres](captures/livres.jpg)

---

## Stack

**Next.js 14** (App Router) · **TypeScript** strict · **Tailwind CSS** ·
**Framer Motion** · déploiement statique, sans base de données.

Les 23 pages sont pré-générées au build. Aucune route API, aucune action
serveur : le site est un ensemble de fichiers, servis tels quels.

---

## Trois partis pris

### Aucune donnée inventée

C'est le site officiel d'une autrice publiée : un ISBN approximatif finit dans
les données structurées lues par Google, une date de dédicace erronée fait se
déplacer un lecteur pour rien.

Chaque éditeur, date de parution et ISBN a donc été vérifié sur une fiche
éditeur ou un catalogue libraire, un par un. Les synopsis sont reformulés à
partir des résumés officiels. **Quand une information n'était pas vérifiable,
le champ est resté vide** — l'agenda l'est encore aujourd'hui, faute de dates
confirmées, et la page le dit en renvoyant vers Instagram.

Les 21 liens d'achat ont été ouverts dans un navigateur et renvoient le bon
titre. Un contrôle automatique vérifie que chaque ISBN des données correspond
à un ISBN des liens, et réciproquement.

### Zéro cookie, zéro traceur

Aucune requête vers un domaine tiers, aucun cookie, aucun stockage local —
vérifié au runtime sur le build de production.

Les polices Google sont téléchargées au build et servies depuis le site. Les
réseaux sociaux sont de simples liens, pas des widgets. Conséquence directe :
**aucun bandeau de consentement n'est nécessaire**, puisqu'il n'y a rien à
faire consentir.

### Accessible, et rapide partout

Contrastes conformes AA, focus clavier visible, `prefers-reduced-motion`
respecté, textes alternatifs en français.

Testé de **320 px** — un iPhone SE de première génération — à **1440 px** :
aucun débordement horizontal. Les images sont servies en WebP aux navigateurs
récents et **en JPEG aux appareils anciens**, automatiquement.

![Version mobile](captures/mobile.jpg)

---

## Pourquoi le code n'est pas ici

Le dépôt applicatif est privé. Il contient les 21 couvertures fournies par les
éditeurs et le portrait de l'autrice, dont la rediffusion suppose des
autorisations écrites.

---

## Crédits

Portrait de Serena Giuliano : **Pauline Darley**.
Couvertures : Le Cherche-Midi, Robert Laffont, Calmann-Lévy, Le Livre de Poche,
Pocket. Albums *Nina & Bruno* illustrés par **Mathou**.
