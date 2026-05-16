# CASE STUDY 2 : SOCIÉTÉ GÉNÉRALE GUINÉE

## Exercice : Audit Cybersécurité

En tant que consultant Data Analyst, je réalise l'audit cybersécurité d'une entreprise type PME guinéenne (contexte similaire à la Société Générale Guinée avant 2022).

## Tableau d'Audit Cybersécurité

| Critère | Oui/Non | Note /10 | Action nécessaire |
|---------|---------|----------|-------------------|
| **Mots de passe forts obligatoires** | Non | **3 /10** | Imposer politique : min. 12 caractères, majuscules, chiffres, symboles. Déployer un gestionnaire de mots de passe. |
| **Authentification 2 facteurs (2FA)** | Non | **1 /10** | Déployer la 2FA (Login + Mot de passe + Code SMS) sur tous les accès critiques. Coût estimé : 50M GNF d'après le cas SG. Impact : 99% risque piratage comptes. |
| **Formation cybersécurité employés** | Non | **1 /10** | Organiser formation obligatoire 2 jours/employé : reconnaître le phishing, créer mots de passe forts, vérifier expéditeurs emails. 89% des cyberattaques réussies commencent par un clic employé sur email frauduleux. |
| **Système détection intrusion (IDS)** | Non | **1 /10** | Déployer un IDS comme IBM QRadar. L'IA surveille 24/7 les connexions inhabituelles, transferts anormaux, horaires suspects. Coût : 800M GNF mais rentabilisé en 1 seule attaque déjouée. |
| **Sauvegardes quotidiennes cloud** | Non | **2 /10** | Migrer les sauvegardes vers le cloud (Microsoft Azure). Sauvegarde 3 fois/jour au lieu d'une fois/semaine. Ne plus garder les sauvegardes dans le même bâtiment (risque incendie). Récupération en 2h au lieu de 2 jours. |
| **Antivirus à jour sur tous PC** | Partiel | **4 /10** | Déployer un antivirus centralisé avec mise à jour automatique sur 100% des postes. Vérification mensuelle de conformité. |
| **Politique d'accès (qui voit quoi)** | Non | **2 /10** | Définir des rôles et niveaux d'accès : le comptable ne doit pas avoir les mêmes droits que le DG. Principe du moindre privilège. |
| **Tests sécurité réguliers** | Non | **1 /10** | Mettre en place un pentesting mensuel : payer des hackeurs éthiques pour attaquer l'entreprise. SG Guinée est passée de 47 vulnérabilités (2022) à 2 mineures (2024) grâce à cette approche. Coût : 50M GNF/an. |
| **Plan de crise cyberattaque** | Non | **1 /10** | Élaborer un protocole d'urgence : détection en 2 min, réaction en 5 min, communication clients en temps réel, coupure des accès compromis, analyse des logs. |
| **Assurance cyberrisque** | Non | **2 /10** | Souscrire une assurance cyberrisque pour couvrir les pertes financières en cas d'attaque réussie. La SG Guinée a failli perdre 500M GNF puis 380M GNF – une assurance aurait limité l'impact. |

## Score Total et Interprétation

### Score Total : 18 / 100

**Interprétation : DANGER (0/39)** 

L'entreprise est extrêmement vulnérable aux cyberattaques. C'est exactement la situation de la Société Générale Guinée avant mai 2022 (note globale 2/10 lors de l'audit). Une action urgente et immédiate est requise.

## Plan d'Action Prioritaire

| N° | Action | Budget | Délai |
|----|--------|--------|-------|
| **1** | Formation cybersécurité obligatoire pour tous les employés (2 jours/employé) + déploiement 2FA + politique mots de passe forts avec gestionnaire Bitwarden | 350 millions GNF | 2 mois |
| **2** | Déploiement système de détection d'intrusion (IDS type IBM QRadar) avec surveillance IA 24/7 des connexions, transferts et horaires suspects | 800 millions GNF | 3 mois |
| **3** | Migration sauvegardes vers cloud sécurisé (Microsoft Azure) + mise en place pentesting mensuel + plan de crise cyberattaque | 650 millions GNF | 4 mois |

**Budget total estimé : 1,8 milliard GNF**

### ROI attendu : +200% en 2 ans

(comme démontré par le cas SG Guinée : 2,45 milliards investis pour 5+ milliards d'attaques déjouées). La cybersécurité n'est **PAS** une dépense, c'est un investissement.

## Compréhension des 5 piliers cybersécurité

### Pilier 1 - Authentification forte (2FA)
Même si un hackeur vole un mot de passe, il ne peut pas se connecter sans le téléphone de l'employé. **Impact : 99% risque piratage.**

### Pilier 2 - Formation humaine
L'humain est le maillon faible. 89% des attaques réussies commencent par un clic sur un email frauduleux. **Former = priorité n°1.**

### Pilier 3 - Détection d'intrusion (IDS)
L'IA surveille 24/7 et détecte les anomalies (connexion depuis un pays étranger, transfert inhabituel, horaire suspect). **Temps de détection : 2 minutes.**

### Pilier 4 - Sauvegardes cloud sécurisées
Données répliquées hors site avec chiffrement militaire. Incendie, vol ou catastrophe ? **Récupération en 2 heures au lieu de 2 jours.**

### Pilier 5 - Tests continus
Payer des hackeurs éthiques pour attaquer avant les vrais hackeurs. Amélioration continue : **de 47 vulnérabilités à 2 mineures en 2 ans.**
