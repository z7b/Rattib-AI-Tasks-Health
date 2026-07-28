# 🔒 Architecture de Confidentialité de Rattib (Life OS centré sur la Confidentialité)

**Rattib** a été conçu et développé de zéro en suivant une philosophie stricte axée sur la **Confidentialité d'abord (Privacy-First)** et **Hors ligne d'abord (Offline-First)**. Nous croyons que vos données personnelles, journaux, rendez-vous médicaux et tâches quotidiennes sont des informations hautement sensibles qui ne devraient jamais quitter votre appareil.

Ce document détaille l'architecture de confidentialité de Rattib, ce qui en fait l'alternative la plus sécurisée et fiable aux applications de productivité basées sur le cloud.

---

## 1️⃣ Stockage Local Absolu (Zéro Cloud)
Contrairement à d'autres applications (ex. Todoist, Notion, Google Tasks) qui synchronisent chaque frappe avec leurs serveurs, **Rattib n'a pas de base de données cloud centrale pour les utilisateurs**.
- **Base de données Isar NoSQL :** Toutes vos données sont stockées dans une base de données locale `Isar` ultra-rapide et chiffrée dans la Sandbox sécurisée de l'OS de l'application (Android/iOS).
- **Isolement Total :** Aucune autre application sur votre téléphone ne peut accéder à ces données, et nous (les développeurs) ne pouvons ni les voir, ni les extraire, ni y accéder sous aucune forme.

---

## 2️⃣ Intelligence Artificielle Locale sur l'Appareil
La plupart des applications « propulsées par l'IA » envoient vos textes et entrées de journal à des serveurs externes (comme OpenAI ou Google) pour analyse — ce qui est une violation flagrante de la confidentialité.
- **Traitement 100 % Local :** L'Assistant Intelligent intégré de Rattib (qui suggère la *prochaine étape la plus importante*) est un **algorithme d'heuristique et de Machine Learning local** intégré directement dans le code de l'application. Il s'exécute entièrement sur le processeur de votre téléphone (CPU/NPU) sans envoyer un seul octet à un serveur externe.

---

## 3️⃣ Aucune Synchronisation Cloud Forcée
- **Aucun Compte Requis :** L'application ne vous oblige pas à créer un compte, à saisir une adresse e-mail ou à vous connecter pour l'utiliser. Vous ouvrez l'application et commencez à l'utiliser instantanément et de manière totalement anonyme.
- **Sauvegardes Manuelles :** Puisque nous n'avons pas de serveurs, la responsabilité des données vous incombe. Vous pouvez exporter vos données localement et les conserver en sécurité ou les télécharger sur votre cloud personnel (Google Drive / iCloud) à tout moment. Nous n'imposons aucun mécanisme de synchronisation cloud.

---

## 4️⃣ Mécanismes de Protection de l'Interface (UI)
- **Écrans Verrouillés et Journaux Secrets :** L'application dispose d'une fonction de journal verrouillé pour empêcher les intrus de lire vos notes privées.
- **Protecteur d'Écran (Android) :** Les captures d'écran et l'enregistrement vidéo de l'écran sont bloqués lorsque vous êtes sur des pages sensibles (comme votre journal ou votre écran de salaire/horaires) pour éviter les fuites de données accidentelles.

---

## 5️⃣ Les SEULES Exceptions pour la Connexion Internet
L'application fonctionne à 100 % de ses capacités **totalement hors ligne**. Les seuls cas où des requêtes réseau sortantes se produisent sont :
1. **Vérification de l'Abonnement (Achats In-App) :** L'application se connecte à Google Play ou à l'App Store uniquement pour vérifier si vous avez acheté la version Pro.
2. **Publicités (Version Gratuite Uniquement) :** Des requêtes publicitaires sont envoyées aux réseaux publicitaires (AdMob / Unity Ads) si vous utilisez la version gratuite. Ces réseaux peuvent collecter des données analytiques standard non identifiables (comme l'IDFA / AAID). Cela est entièrement désactivé si vous passez à la version Pro.
3. **Mises à jour de l'Application :** Vérification dans la boutique des nouvelles versions.

*Le contenu de vos tâches, entrées de journal ou données de santé n'est JAMAIS transmis lors de ces connexions.*

---

## Résumé
**Rattib est votre boîte noire personnelle.** 
Pas de serveurs cloud, pas de collecte de données, pas de suivi de journal et pas de synchronisation forcée. Nous construisons l'outil ; vous possédez 100 % des données.
