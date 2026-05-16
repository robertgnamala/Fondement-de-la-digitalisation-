# CASE STUDY 5 : EDG (ÉLECTRICITÉ DE GUINÉE)

## Exercice : IA Anti-Fraude pour le secteur de l'énergie

En tant que consultant Data Analyst, je conçois un système IA antifraude en m'appuyant sur le modèle déployé par EDG avec Schneider Electric.

---

## Étape 1 : Identification de 5 types de fraudes (20 min)

| N° | Type de Fraude | Fréquence | Perte/an | Détectable par IA ? |
|----|----------------|-----------|----------|---------------------|
| **1** | **Branchement sauvage :** câble branché AVANT le compteur pour obtenir de l'électricité gratuite (cas M. Diallo, Ratoma) | Très fréquent | 60 Mrd GNF | **OUI** - Algo Consommation Zéro Suspect : compteur affiche 0 kWh mais maison occupée (lumières visibles le soir) |
| **2** | **Compteur trafiqué :** utilisation d'un aimant puissant collé sur le compteur pour le ralentir, divisant la facture par 3 (cas Mme Bah) | Fréquent | 40 Mrd GNF | **OUI** - Algo Baisse Subite : consommation stable à 200 kWh/mois pendant 2 ans, puis chute soudaine à 50 kWh/mois |
| **3** | **Faux abonnement :** un commerce (restaurant) utilise le nom d'une mosquée pour bénéficier du tarif réduit, économisant 80% | Modéré | 30 Mrd GNF | **OUI** - Algo Tarif Frauduleux : mosquée consommant 800 kWh/mois alors que les vraies mosquées consomment 50-100 kWh max |
| **4** | **Activité non déclarée :** un local déclaré comme restaurant mais abritant aussi un cyber café et un atelier de soudure cachés (cas Restaurant Le Bon Goût) | Fréquent | 30 Mrd GNF | **OUI** - Algo Pic Nocturne + Profil Anormal : consommation élevée en dehors des heures d'ouverture déclarées + consommation ×5 par rapport aux commerces similaires |
| **5** | **Compteur reprogrammé :** compteur modifié avec un Arduino pour afficher une consommation artificielle avec un profil 'trop parfait' sans variations naturelles | Rare mais croissant | 20 Mrd GNF | **OUI** - Algo Patterns Trop Parfaits : pic exact toujours à la même minute (trop précis = robot), aucune variation naturelle (suspect) |

---

## Étape 2 : Conception d'un Algorithme de Détection (20 min)

### Fraude ciblée : Compteur trafiqué (aimant ou modification physique)

Cet algorithme s'inspire directement de l'Algo 3 "Baisse Subite" déployé par EDG, enrichi avec des signaux complémentaires détectés par les smart meters.

#### Signaux suspects :

**Signal suspect 1 :** Baisse subite de consommation de plus de 50% par rapport à la moyenne des 6 derniers mois, sans changement déclaré (déménagement, absence). 
*Exemple du document :* M. Sow passé de 200 kWh/mois à 50 kWh/mois du jour au lendemain.

**Signal suspect 2 :** Consommation significativement inférieure à celle des voisins avec un profil similaire (même taille de maison, même nombre d'occupants). 
*L'IA d'EDG compare systématiquement avec les 10 foyers les plus similaires.*

**Signal suspect 3 :** Profil de consommation trop régulier et sans les variations naturelles attendues (pas de pic le soir, pas de baisse la nuit). 
*Un compteur trafiqué avec Arduino montre des patterns trop parfaits comme détecté en mars 2024.*

**Signal suspect 4 :** Incohérence entre la consommation déclarée et les indices d'activité réelle : lumières visibles le soir alors que le compteur affiche zéro, ou consommation basse alors que le compteur intelligent détecte des appareils énergivores.

**Signal suspect 5 :** Chute de consommation coïncidant avec un achat d'aimant ou de matériel électronique détecté (données croisées avec les achats en ligne ou les informations de marché local).

#### Seuil d'alerte :

Si **3 signaux ou plus** sont détectés simultanément, la probabilité de fraude est estimée à plus de 85% (seuil utilisé par EDG : le système déclenche une alerte à partir de 87% de probabilité).

#### Actions automatiques :

1. Alerte immédiate envoyée à l'équipe terrain avec le détail de l'anomalie
2. Analyse automatique de l'historique sur 12 mois
3. Comparaison avec les 10 compteurs voisins
4. Recommandation : **VISITE TERRAIN URGENTE** (comme dans le cas du Restaurant Le Bon Goût détecté le 15 août 2024 à 03h47)

> **⚠️ Important :** pas de sanction automatique, car le document souligne que 13% sont de faux positifs (famille nombreuse qui déménage = consommation ×2).

---

## Étape 3 : Budget et ROI (20 min)

### Investissement

| Poste d'investissement | Coût |
|------------------------|------|
| **Collecte de données :** remplacement de 50 000 compteurs par des smart meters connectés (communication GSM/4G, envoi de données toutes les 15 min) | 500 millions GNF (10 000 GNF/compteur × 50 000, exactement le coût indiqué par EDG) |
| **Plateforme IA de détection :** développement des 10 algorithmes de détection, infrastructure serveur, intégration avec les smart meters (partenariat type Schneider Electric) | 200 millions GNF |
| **Formation équipe :** formation des agents terrain à l'utilisation du système d'alertes, interprétation des données, procédures de vérification sur site | 100 millions GNF |
| **TOTAL INVESTISSEMENT** | **800 millions GNF** |

### Gains attendus

| Indicateur | Avant IA | Après IA | Progression |
|------------|----------|----------|-------------|
| Fraudes détectées/mois | 50 | 2 000 | **+3900%** |
| Taux de détection | 5% | 87% | **+82 pts** |
| Pertes mensuelles | 15 Mrd GNF | 3 Mrd GNF | **-80%** |
| Recouvrement mensuel | 500 M GNF | 8 Mrd GNF | **+1500%** |

### ROI : Moins de 2 mois

Avec un investissement de 800 millions GNF et des économies de 12 milliards GNF/mois, le projet est rentabilisé en **seulement 20 jours** (exactement comme le calcule le document EDG).

---

## Impact social positif

Comme le souligne le document, la réduction des fraudes de 80% permet à EDG de baisser les tarifs de **15%** pour tous les clients honnêtes.

C'est un **cercle vertueux** : 
- Les clients honnêtes paient moins
- EDG gagne plus
- L'électricité devient accessible à tous les Guinéens

---

## Approche éthique (Leçon 4 EDG)

Comme EDG, l'approche doit être **transparente** :

- Informer les clients de l'installation des compteurs intelligents
- Offrir une option de refus (avec facturation estimée haute)
- Ne jamais sanctionner automatiquement sans vérification humaine

### Principe : Humain + IA = Parfait

> *L'IA détecte, l'humain vérifie, la décision est prise ensemble.*
