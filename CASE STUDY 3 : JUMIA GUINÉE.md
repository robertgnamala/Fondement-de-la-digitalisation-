# CASE STUDY 3 : JUMIA GUINÉE

## Exercice : Stratégie Big Data pour un Business

En tant que consultant Data Analyst, je conçois une stratégie Big Data pour une entreprise de commerce (type boutique/commerce général en Guinée), en m'inspirant directement de l'approche Jumia Guinée.

---

## Partie 1 : Identification de 10 données collectables (15 min)

| N° | Type de donnée | Comment la collecter | Utilité business |
|----|----------------|----------------------|------------------|
| **1** | Historique des achats | Système de vente / caisse enregistreuse | Prédire les prochains achats du client, comme Jumia le fait avec ses 50 millions de données sur 200 000 clients |
| **2** | Âge et sexe du client | Formulaire d'inscription / compte client | Créer des profils types (comme les 12 profils Jumia : Fashionista, Bricoleur, Gamer, Maman Active, etc.) |
| **3** | Localisation géographique | Adresse de livraison / géolocalisation app | Adapter les offres selon la zone (Conakry, Labé, Kankan ont des besoins différents comme montré par les clients A, B, C de Jumia) |
| **4** | Fréquence d'achat | Système de vente (dates d'achat) | Distinguer les clients fréquents (1 fois/semaine comme Aminata) des occasionnels (1 fois/trimestre comme Mme Diallo) |
| **5** | Panier moyen | Calcul automatique via système de vente | Segmenter : petit panier (200K GNF), gros panier (1,5M GNF) et adapter les promotions en conséquence |
| **6** | Produits consultés sans achat | Tracking site web / application mobile | Identifier les hésitations (comme Kadiatou qui a consulté une poussette 5 fois sans acheter) et déclencher une offre ciblée |
| **7** | Heure et jour de connexion/achat | Logs serveur / application mobile | Découvrir des patterns temporels (comme le pattern Jeudi Soir : 40% des achats vêtements entre 20h-23h) |
| **8** | Appareil utilisé (téléphone/PC) | Useragent navigateur / type d'appli | Optimiser l'expérience selon le support (mobile-first en Guinée car 85% ont un téléphone) |
| **9** | Recherches effectuées sur le site | Barre de recherche / logs requêtes | Anticiper les besoins (comme l'IA Jumia qui détecte une cliente cherchant 'fatigue grossesse' et prédit une grossesse) |
| **10** | Date de naissance du client | Formulaire d'inscription | Envoyer des offres anniversaire personnalisées (résultat Jumia : 40% des clients achètent pour leur propre anniversaire avec +30%) |

---

## Partie 2 : Analyse de 3 Patterns (15 min)

### Pattern 1 - L'Effet Salaire

En analysant les données temporelles d'achat, on observe que les achats de produits à forte valeur (électroménager, électronique) se concentrent entre le 25 et le 30 de chaque mois, correspondant à la période de versement des salaires. C'est exactement le pattern identifié par Jumia Guinée.

**Action business :** Programmer les promotions sur les produits chers uniquement en fin de mois (25-30 du mois). Envoyer des emails personnalisés à ce moment précis avec des facilités de paiement. 

**Résultat attendu :** augmentation significative du taux de conversion, car les clients ont les moyens d'acheter à ce moment.

---

### Pattern 2 - Le Panier Complémentaire

Les clients qui achètent un produit donné achètent systématiquement des produits complémentaires. Jumia a découvert que les acheteurs de couches bébé achètent aussi du lait, des vêtements enfant et des jouets avec une probabilité de 85%.

**Action business :** Mettre en place un système de recommandations automatiques "Produits complémentaires". Quand un client ajoute des couches au panier, lui proposer automatiquement lait + vêtements bébé + jouets avec une remise groupée.

**Résultat attendu chez Jumia :** panier moyen passé de 450K GNF à 780K GNF **(+73%)**.

---

### Pattern 3 - L'Hésitant Convertible

Un client qui consulte un même produit plusieurs fois sans acheter est sur le point de craquer. Jumia a détecté Kadiatou qui avait cherché poussette bébé 5 fois en une semaine et consulté 12 produits bébé sans acheter. L'IA a prédit 90% de probabilité d'achat dans 48h.

**Action business :** Déclencher automatiquement un email personnalisé avec une réduction limitée dans le temps (ex: "25% SEULEMENT AUJOURD'HUI") + une option de paiement en 3 fois sans frais.

**Résultat Jumia :** Kadiatou a acheté pour 780 000 GNF au lieu des 480 000 GNF prévus, grâce aux produits complémentaires ajoutés.

---

## Partie 3 : Plan d'Action en 3 Phases (15 min)

| Phase | Action | Outil | Coût | Délai |
|-------|--------|-------|------|-------|
| **1** | Collecter les données de base : historique achats, âge, localisation, fréquence. Mettre en place le tracking des comportements (pages vues, recherches, temps passé). | Google Analytics (gratuit) + Système de caisse avec CRM intégré | 5M GNF | 1 mois |
| **2** | Analyser les données avec machine learning : créer les profils clients types, identifier les patterns temporels et comportementaux, construire les modèles prédictifs. | Python + TensorFlow (comme Jumia) ou solutions simples : Excel / Power BI pour commencer | 50M GNF | 3 mois |
| **3** | Automatiser les actions marketing : emails personnalisés selon profils, notifications push ciblées, promotions dynamiques basées sur les prédictions IA. | Plateforme marketing automation (Mailchimp/Sendinblue) + intégration API | 30M GNF | 2 mois |

### Budget total : 85 millions GNF

(bien inférieur aux 500M GNF de Jumia car on commence simple, conformément à la Leçon 3 du document : Jumia a commencé avec juste historique achats + âge + localisation)

### ROI attendu : 

Sur la base des résultats Jumia **(+217% de CA mensuel en 6 mois)**, un ROI de **+100% minimum** est réaliste dans les 6 premiers mois.

---

## Respect de l'éthique

Conformément à la Leçon 4 de Jumia : **toujours demander la permission avant d'utiliser les données clients.**

La transparence sur l'utilisation des données génère la confiance, et la confiance génère des données de meilleure qualité. Informer clairement chaque client de ce qui est collecté et pourquoi, avec option de refus.
