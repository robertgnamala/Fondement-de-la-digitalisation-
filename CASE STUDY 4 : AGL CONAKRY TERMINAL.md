# CASE STUDY 4 : AGL CONAKRY TERMINAL

## Exercice : Cloud Readiness Assessment

En tant que consultant Data Analyst, j'évalue la maturité cloud d'une entreprise type en Guinée (contexte similaire à AGL Conakry Terminal avant 2020).

---

## Tableau d'évaluation Cloud Readiness

| Critère | Oui/Non (Oui=10 ; Non=0) | Priorité | Action |
|---------|--------------------------|----------|--------|
| **Données critiques sur serveur local** | Oui | **URGENTE** | Migrer vers cloud (Azure). AGL avait 50 serveurs physiques locaux - en cas d'incendie (comme en avril 2019), TOUTES les données sont perdues. Récupération avec cloud : 10 minutes vs 6 mois. |
| **Besoin accès données hors bureau** | Oui | **URGENTE** | Le COVID a montré que l'impossibilité de télétravail coûte cher : AGL a perdu 5 millions USD en 2 semaines de fermeture. Le cloud permet l'accès 24/7 depuis n'importe où. |
| **Collaboration partenaires externes** | Oui | **HAUTE** | Fin des conflits de version par email. Un seul fichier en ligne, modifiable en simultané (comme AGL Conakry et MSC Genève qui collaborent désormais en temps réel). |
| **Coûts IT > 30% budget** | Oui | **HAUTE** | Le cloud réduit les coûts : AGL est passé de 80M GNF/mois (serveurs + électricité + climatisation + techniciens) à 50M GNF/mois cloud, soit **-37%**. |
| **Peur perdre données (incendie, vol)** | Oui | **URGENTE** | Justifié ! AGL a perdu TOUTES les données 2018 dans un incendie (avril 2019). Avec cloud, données sauvegardées en Europe. Test de simulation panne : reprise en 10 minutes. |
| **Équipe IT surchargée maintenance** | Oui | **HAUTE** | Maintenance automatique par Microsoft. Plus besoin de technicien sur place 24/7. Temps d'arrêt passé de 2h/semaine à 5 min/mois chez AGL. |
| **Croissance rapide prévue** | Oui | **MOYENNE** | Le cloud est évolutif : Azure ajoute automatiquement de la capacité en période de pic (Black Friday 2022 : trafic ×3, coût seulement +30% pour décembre). |
| **Besoin flexibilité** | Oui | **MOYENNE** | Avant : serveurs surchargés = plantages. Avec cloud : capacité ajustée automatiquement. On ne paye que ce qu'on utilise. |
| **Sécurité actuelle insuffisante** | Oui | **HAUTE** | Microsoft Azure est 1000× plus sécurisé qu'un serveur local (leçon 5 du cas SG Guinée). Chiffrement militaire, sauvegardes automatiques. |
| **Conformité réglementaire stricte** | Oui | **HAUTE** | Le cloud facilite la conformité : logs complets, traçabilité totale, rapports automatiques pour les auditeurs et régulateurs. |

---

## Score et Interprétation

### Score : 10 / 10

**Interprétation : CLOUD URGENT**

L'entreprise présente tous les signaux d'une migration cloud nécessaire et prioritaire. C'est exactement la situation d'AGL Conakry Terminal en 2020, où le COVID a révélé brutalement l'impossibilité de fonctionner sans cloud.

---

## Plan de Migration Cloud en 3 Phases

| Phase | Durée | Application | Coût |
|-------|-------|-------------|------|
| **1** | 1 mois | Migration emails et outils bureautiques vers Office 365. C'est l'approche recommandée par le document : commencer petit, comme AGL qui a migré 1 application test d'abord (gestion planning) avant le reste. | 5 millions GNF |
| **2** | 3 mois | Migration de l'infrastructure serveur vers Microsoft Azure : bases de données, sauvegardes automatiques 3 fois/jour, mise en place du disaster recovery (récupération en 10 min). Formation équipe IT (2 semaines suffisent selon le chef IT AGL). | 200 millions GNF |
| **3** | 2 mois | Déploiement d'applications métier cloud : application mobile pour le terrain (comme AGL Mobile avec scan QR code), tableau de bord Power BI en temps réel accessible partout, collaboration en temps réel avec partenaires. | 300 millions GNF |

### Budget total estimé : 505 millions GNF

(comparable au budget d'AGL de 1 milliard GNF, ajusté à la taille d'une PME)

### ROI attendu : 6 mois

(identique au cas AGL)

**Économies récurrentes :** 
- Réduction de **37%** des coûts IT mensuels
- Gain de productivité massif (AGL : temps par opération passé de 45 min à 12 min, soit **73%**)

---

## Impact Green IT

Réduction de **80%** de l'empreinte écologique (datacenter Microsoft fonctionne à l'énergie solaire vs 50 serveurs locaux consommant 100 000 kWh/an).
