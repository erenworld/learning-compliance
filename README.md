# DORA

## Pourquoi séparer les tâches et les responsabilités ?
Pour limiter les conflits d'intérêts.

## Pourquoi suivre les dates de fin de support des systèmes TIC ?
Pour gérer les risques liés aux technologies héritées (legacy).

## Pourquoi utiliser des contrôles cryptographiques ?
Pour garantir la confidentialité, l'intégrité, la disponibilité et l'authenticité des données.

## Quand faut-il chiffrer les données ?
Au repos, en transit et, si nécessaire, en cours d'utilisation.

## Sur quoi repose le choix des mesures de chiffrement ?
Sur la classification des données et l'évaluation des risques.

## Pourquoi séparer les environnements de développement et de production ?
Pour éviter qu'un test impacte les systèmes en production.

## Pourquoi la gestion des correctifs est-elle essentielle ?
Pour corriger les vulnérabilités en limitant les risques de perturbation.

## Que faire lorsqu'une faille de sécurité est découverte ?
Suivre un processus de notification clair pour informer les bonnes parties au bon moment.

## Pourquoi chaque utilisateur ou système doit-il avoir une identité unique ?
Pour assurer la traçabilité et appliquer les droits d'accès correctement.

## Quels outils permettent de gérer les identités et les secrets ?
HashiCorp Vault et une solution IAM.

## Pour qui ?

DORA is aimed specifically at EU-based financial entities and ICT service providers.

## Who is financial entities ?

- Payment and credit institutions
- Electronic money institutions
- Investment firms
- Insurance companies
- Trade repositories

## Who is ICT providers ?

A: Cloud providers
Network security companies
IT consulting firms
Managed IT service providers
Help desk service providers

## 5 key compliance requirements of DORA
 
- ICT risk management
- ICT-related incident management
- Digital operational resilience testing
- ICT third-party risk management
- Information sharing

## Comment faire la gestion des vulnérabilités TIC ?
 
- scanners de vulnérabilités (tenable nessus, tenable, qualys, openvas, greenbone)
- patch management (microsoft wsus/intune, invanti patch management)
- surveillance des CVE (NVD, CVE details/VulnCheck, Mandiant advantage)
- Gestion de configuration et automatisation (ansible, puppet, chef, saltstack, ci/cd, github actions, argo cd)
- Évaluation de la gravité et du risque (CVSS Calculator, Exploit Prediction Scoring System, NIST National Vulnerability Database, GitHub Security Advisories, Confluence)

## Quel outil permet de gérer une identité unique par utilisateur ?
Keycloak.

## Quel outil permet l'authentification forte (MFA) ?
Duo Security.

## Quels outils permettent la gestion des comptes à privilèges (PAM) ?
CyberArk PAM, BeyondTrust PAM, Delinea Secret Server.

## Quels outils permettent la journalisation et la traçabilité ?
Microsoft Sentinel, Elastic Security.

## Quel outil permet de gérer les comptes génériques de façon sécurisée ?
HashiCorp Vault.

## Quels outils automatisent la création et la suppression des comptes ?
Microsoft Entra ID + SCIM, Okta Lifecycle Management, SailPoint Identity Security Cloud.

## Pourquoi DORA impose-t-il une gestion des changements ?
Pour limiter les risques liés aux modifications des systèmes TIC.

## Que doit contenir un processus de gestion des changements ?
Approbation, tests, documentation, déploiement contrôlé et plan de retour arrière (rollback).

## Pourquoi séparer les rôles dans le Change Management ?
Pour éviter les conflits d'intérêts.

## Quels sont les objectifs d'une politique de sécurité de l'information ?
Protéger la confidentialité, l'intégrité, la disponibilité et l'authenticité des données et services.

## Quels sont les quatre principes de la sécurité de l'information ?
Confidentialité, intégrité, disponibilité et authenticité.

## Problème : Les autorités doivent pouvoir examiner facilement le cadre de gestion des risques TIC des entités financières.

Réaliser un réexamen régulier et transmettre un rapport dans un format électronique interrogeable.

## Problème : Les mesures de sécurité TIC ne peuvent pas être identiques pour toutes les entités financières.

Solution : Adapter les politiques et contrôles de sécurité au profil de risque, à la taille et à la complexité de l'entité, en couvrant notamment le chiffrement, la sécurité des opérations et des réseaux, la gestion des changements TIC et la continuité d'activité.

## Que doivent garantir les politiques de sécurité TIC (al. 1) ?

a) Sécurité des réseaux
b) Garanties contre intrusions et abus de données
c) Disponibilité, authenticité, intégrité, confidentialité (dont cryptographie)
d) Transmission précise et rapide sans retard injustifié

## Sur quoi doivent être alignées les politiques de sécurité TIC ? (2.a)

Sur les objectifs de sécurité de l'information définis dans la stratégie de résilience opérationnelle numérique (art. 6§8 DORA)

## Que doit indiquer la politique concernant l'organe de direction ? (2.b)

La date de son approbation formelle par l'organe de direction

## Que doivent suivre les indicateurs de mise en œuvre ? (2.c.i)

La mise en œuvre effective des politiques, procédures, protocoles et outils de sécurité TIC


---


## Study case

### HelixDB

Under the hood, Helix-DB was still operating like a fast-moving, early-stage startup:

- Monitoring existed, but no real alerting
- Backups were manual
- Access control was informal
- No formal incident response process

They introduced:

- A dedicated enterprise architecture on AWS
- Isolated, per-customer environments (VPCs, clusters, storage)
- Automated backups and tested restoration procedures
- Centralized logging and monitoring with alerting
- Formalized access control and internal processes

### Lucis

They faced three hard constraints:

- Extreme data sensitivity Unlike most B2C products, Lucis manages regulated health data. ISO 27001 wasn’t a sales checkbox. It was a signal to users, partners, and regulators that security was foundational.
- A lean, fast-moving team With engineering focused on shipping product and improving member outcomes, the team couldn’t afford months of manual documentation.
- Compliance that reflected reality Lucis didn’t want a generic framework that looked good on paper. They wanted certification to reflect how they actually built and operated their systems.

### Ideas from Reddit

#### What's one compliance requirement you thought would be a waste of time, but ended up making your security noticeably better?

- Centralized logging.
- Version control. I used to think people made too big a deal out of it until we had three different copies of the same document.
- Quarterly access reviews.
- Firewall rules review.
- Training content versioning.

### To implement

- https://security.finic.ai/?tab=compliance  
- https://trust.openrouter.ai/ 
- https://trust.openzeppelin.com/
- Access Reviews & Least-Privilege Enforcement tool, Replace manual data gathering with automated discovery. Auto user discovery Single review interface One-click actions github
- Employee Portal Security shouldn't slow down deals. Device compliance Security training Workforce management
