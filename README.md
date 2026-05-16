# 🚀 Jaya - Le projet qui va (peut-être) changer le monde

> *"Le code, c'est comme le café : ça marche mieux quand c'est bien préparé et que ça ne plante pas."* - Un développeur qui a trop bu de café

---

## 🎯 C'est quoi ce machin ?

C'est un projet Symfony 8.0, parce qu'on aime vivre dangereusement avec la dernière version stable. C'est comme conduire une Ferrari : puissant, mais attention aux virages serrés.

### ⚡ Réalisé en 4 jours en LIVE CODING

Oui, tu as bien lu. **4 jours**. En live. Avec des gens qui regardent. C'est comme cuisiner devant une audience : si tu fais tomber l'omelette, tout le monde le voit. Mais là, c'est du code, donc c'est encore plus stressant.

- Jour 1 : Setup et café
- Jour 2 : Code et plus de café
- Jour 3 : Debug et café
- Jour 4 : Finir (et café)

> *"Live coding : l'art de faire semblant de savoir ce qu'on fait en temps réel."*

### ✨ Fonctionnalités

- **🍽️ Système de réservation** : Réserve ta table en ligne (et prie pour qu'elle soit libre)
- **📱 Commande via QR Code** : Scanne le QR code de ta table, choisis ton menu, et passe commande sans appeler le serveur
- **🎉 Événements privés** : Organise tes événements spéciaux (anniversaire, mariage, divorce...)
- **👨‍💼 Administration** : Panel admin pour gérer tout ça (réservations, commandes, événements) comme un vrai boss
- **🌍 Multilingue** : Disponible en français et anglais (parce que le monde est grand)
- **ℹ️ Infos pratiques** : Tout ce que tu dois savoir sur le restaurant (horaires, adresse, comment nous trouver)

---

## 🌐 Partie Front (Côté Client)

### Pages Publiques
- **🏠 Page d'accueil** : Affichage des événements à venir et passés, détection automatique de la langue (FR/EN)
- **📅 Réservation** : Formulaire complet avec validation de date (pas de réservation dans le passé, logique)
- **🍴 Commande QR Code** :
  - Scan du QR code de table
  - Affichage du menu par catégorie (entrées, plats, desserts, boissons, cocktails)
  - Sélection des articles avec quantités
  - Confirmation de commande avec récapitulatif
  - Suivi du statut de la commande en temps réel
- **🎊 Événements privés** :
  - Affichage des événements à venir et passés
  - Formulaire de demande d'événement privé
  - Galerie d'images dynamique
- **ℹ️ Informations pratiques** :
  - Horaires d'ouverture détaillés par jour
  - Services disponibles (restaurant, bar, événements, Wi-Fi, parking, accès handicapé)
  - Coordonnées de contact avec carte
  - Moyens de transport (voiture, taxi, bus)
- **🤝 Collaborations** :
  - Territoires et environnements partenaires
  - Influenceurs et leurs témoignages
  - Partenaires locaux (pêcheurs, marché, rhums, etc.)

### Fonctionnalités Techniques
- **🌐 Multilingue** : Système de traduction dynamique via base de données (FR/EN)
- **📱 Responsive** : Design adapté mobile/tablette/desktop
- **🔒 Sécurité** : Protection CSRF sur tous les formulaires

---

## 🔧 Partie Admin (Back-office)

### Dashboard Principal
- **📊 Statistiques en temps réel** :
  - Chiffre d'affaires quotidien, hebdomadaire
  - Tendance des ventes (comparaison semaine précédente)
  - Nombre de commandes
  - Taux d'annulation
  - Panier moyen
- **📈 Analytics avancés** :
  - Top 10 des menus les plus vendus
  - Revenus par catégorie
  - Revenus horaires
- **🪑 Gestion des tables** :
  - Vue d'ensemble des tables (occupées/libres)
  - Toggle d'occupation en un clic

### Gestion des Réservations
- **📋 Liste complète** : Toutes les réservations triées par date/heure
- **👁️ Détail** : Vue détaillée de chaque réservation
- **✅ Gestion des statuts** : pending, confirmed, cancelled, completed, no_show
- **🗑️ Suppression** : Avec protection CSRF

### Gestion des Commandes
- **📦 Workflow complet** :
  - pending → validated → confirmed → ready → served
- **🔥 Vue cuisine** : Interface dédiée pour les commandes confirmées
- **✅ Actions rapides** :
  - Valider la commande
  - Confirmer et envoyer en cuisine
  - Marquer comme prête
  - Marquer comme servie
  - Annuler
- **🪑 Gestion des tables** : Toggle occupancy avec QR code generation

### Gestion des Événements
- **📅 CRUD complet** :
  - Créer un nouvel événement
  - Modifier les détails
  - Activer/Désactiver la visibilité
  - Supprimer
- **🖼️ Gestion des images** : Sélection d'image depuis dossier
- **📊 Vue séparée** : Événements à venir vs passés

### Gestion des Demandes d'Événements Privés
- **📋 Liste des demandes** : Toutes les demandes triées par date
- **👁️ Détail** : Vue complète de chaque demande
- **🔄 Gestion des statuts** : pending, contacted, confirmed, cancelled, completed

### Gestion des Traductions
- **🌍 CRUD complet** :
  - Créer une nouvelle traduction
  - Modifier existante
  - Supprimer
- **🔑 Clés de traduction** : Organisées alphabétiquement
- **💾 Persistance** : Stockées en base de données pour modification sans redeploy

### Sécurité Admin
- **🔐 Authentification** : Login sécurisé avec ROLE_ADMIN
- **🛡️ Protection CSRF** : Sur toutes les actions destructives
- **🚫 Accès restreint** : Toutes les routes admin protégées

---

## � Captures d'écran

### Partie Front (Côté Client)

#### Page d'accueil
![Page d'accueil](/CaptureEcran/screenshot_01.png)
*La page d'accueil avec les événements à venir et passés*

![Page d'accueil scroll](/CaptureEcran/screenshot_02.png)
*Section événements avec galerie*

#### Réservation
![Formulaire de réservation](/CaptureEcran/screenshot_03.png)
*Formulaire complet de réservation de table*

#### Commande via QR Code
![Scan QR code](/CaptureEcran/screenshot_04.png)
*Page de scan du QR code de table*

![Menu par catégorie](/CaptureEcran/screenshot_05.png)
*Affichage du menu organisé par catégorie (entrées, plats, desserts, boissons, cocktails)*

![Sélection des articles](/CaptureEcran/screenshot_06.png)
*Sélection des articles avec quantités*

![Confirmation de commande](/CaptureEcran/screenshot_07.png)
*Page de confirmation avec récapitulatif de la commande*

#### Événements Privés
![Événements privés](/CaptureEcran/screenshot_08.png)
*Page des événements privés avec formulaire de demande*

![Galerie d'événements](/CaptureEcran/screenshot_09.png)
*Affichage des événements à venir et passés*

#### Informations Pratiques
![Informations pratiques](/CaptureEcran/screenshot_10.png)
*Horaires, services et informations de contact*

#### Collaborations
![Collaborations](/CaptureEcran/screenshot_11.png)
*Page des partenariats et collaborations*

### Partie Admin (Back-office)

#### Login Admin
![Login admin](/CaptureEcran/screenshot_12.png)
*Page de connexion administrateur*

#### Dashboard Principal
![Dashboard admin](/CaptureEcran/screenshot_13.png)
*Tableau de bord avec statistiques en temps réel*

![Statistiques détaillées](/CaptureEcran/screenshot_14.png)
*Analytics avancés : revenus, tendances, top ventes*

#### Gestion des Réservations
![Liste des réservations](/CaptureEcran/screenshot_15.png)
*Vue complète des réservations clients*

![Détail réservation](/CaptureEcran/screenshot_16.png)
*Détail d'une réservation avec gestion des statuts*

#### Gestion des Commandes
![Liste des commandes](/CaptureEcran/screenshot_17.png)
*Vue des commandes par statut (pending, validated, confirmed, ready, served)*

![Détail commande](/CaptureEcran/screenshot_18.png)
*Détail d'une commande avec articles*

![Actions commande](/CaptureEcran/screenshot_19.png)
*Actions rapides : valider, confirmer, annuler, marquer prêt/servi*

#### Vue Cuisine
![Vue cuisine](/CaptureEcran/screenshot_20.png)
*Interface dédiée pour les commandes confirmées en cuisine*

#### Gestion des Tables
![Gestion des tables](/CaptureEcran/screenshot_21.png)
*Vue d'ensemble des tables avec statut d'occupation*

![Toggle table](/CaptureEcran/screenshot_22.png)
*Toggle d'occupation de table en un clic*

#### Gestion des Événements
![Liste des événements](/CaptureEcran/screenshot_23.png)
*Vue des événements à venir et passés*

![Créer événement](/CaptureEcran/screenshot_24.png)
*Formulaire de création d'événement*

![Modifier événement](/CaptureEcran/screenshot_25.png)
*Formulaire de modification d'événement*

#### Gestion des Demandes d'Événements Privés
![Demandes événements](/CaptureEcran/screenshot_26.png)
*Liste des demandes d'événements privés*

![Détail demande](/CaptureEcran/screenshot_27.png)
*Détail d'une demande avec gestion des statuts*

#### Gestion des Traductions
![Liste des traductions](/CaptureEcran/screenshot_28.png)
*Vue complète des traductions FR/EN*

![Créer traduction](/CaptureEcran/screenshot_29.png)
*Formulaire de création de traduction*

![Modifier traduction](/CaptureEcran/screenshot_30.png)
*Formulaire de modification de traduction*

#### Autres Vues Admin
![Vue supplémentaire 1](/CaptureEcran/screenshot_31.png)
*Interface administrative supplémentaire*

![Vue supplémentaire 2](/CaptureEcran/screenshot_32.png)
*Interface administrative supplémentaire*

![Vue supplémentaire 3](/CaptureEcran/screenshot_33.png)
*Interface administrative supplémentaire*

![Vue supplémentaire 4](/CaptureEcran/screenshot_34.png)
*Interface administrative supplémentaire*

![Vue supplémentaire 5](/CaptureEcran/screenshot_35.png)
*Interface administrative supplémentaire*

![Vue supplémentaire 6](/CaptureEcran/screenshot_36.png)
*Interface administrative supplémentaire*

![Vue supplémentaire 7](/CaptureEcran/screenshot_37.png)
*Interface administrative supplémentaire*

---

## �🛠️ Installation

```bash
# Cloner le repo (évidemment)
git clone https://github.com/ton-pseudo/jaya.git

# Entrer dans le dossier (sauf si tu veux coder depuis le parent)
cd jaya

# Installer les dépendances (prie pour que ça marche)
composer install

# Copier le fichier .env (et ne pas oublier de le modifier, hein)
cp .env .env.local

# Lancer le serveur (croise les doigts)
symfony server:start
```

### 🚨 Si ça plante

1. Vérifie ta connexion internet
2. Vide le cache : `php bin/console cache:clear`
3. Redémarre ton ordinateur (la solution ultime)
4. Fais une offrande au dieu du PHP

---

## 🧪 Tests

```bash
php bin/phpunit
```

> *"Si les tests passent, c'est qu'ils sont mal écrits."* - Loi de Murphy du développement

---

## 🤝 Contribuer

Les contributions sont les bienvenues ! Surtout si tu corriges mes bugs.

1. Fork le projet
2. Crée une branche (`git checkout -b feature/ma-feature-geniale`)
3. Commit (`git commit -m 'Ajout de quelque chose d\'incroyable'`)
4. Push (`git push origin feature/ma-feature-geniale`)
5. Ouvre une Pull Request et prie pour qu'elle soit acceptée

---

## 📄 Licence

Proprietary - parce que le code, c'est comme les recettes de grand-mère : ça ne se partage pas n'importe comment.

---

## 👨‍💻 Auteur

**Ton Nom** - *Le développeur qui a encore oublié un point-virgule quelque part*

---

## 🙏 Remerciements

- L'équipe Symfony pour ce framework incroyable
- Stack Overflow, mon meilleur ami
- Le café, car sans lui, ce code n'existerait pas
- ChatGPT pour les commentaires humoristiques

---

## ⚠️ Avertissement

Ce logiciel est fourni "tel quel", sans aucune garantie. Si ton serveur explose, si ton chat reçoit des emails de spam, ou si tu te retrouves avec une facture AWS de 10 000€, c'est pas ma faute.

---

<div align="center">
  <sub>Créé avec ❤️, beaucoup de ☕, et un peu de 🤬</sub>
</div>
