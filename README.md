# DORA

- Afin de limiter le risque de conflits d’intérêts, les entités financières devraient veiller à la séparation des tâches lors de  l’attribution de rôles et de responsabilités 
- Afin de garantir une bonne gestion du risque lié aux systèmes de TIC hérités, les entités financières devraient  enregistrer et surveiller les dates d’expiration des services TIC d’appui fournis par des tiers.
- DAMIEN CLOCHARD m'a parlé de ça : Les contrôles cryptographiques peuvent garantir la disponibilité, l’authenticité, l’intégrité et la confidentialité des  données. Les entités financières visées au titre II du présent règlement devraient donc définir et mettre en œuvre ces  contrôles sur la base d’une approche fondée sur les risques. À cette fin, les entités financières devraient chiffrer les  données concernées, au repos, en transit ou, si nécessaire, en cours d’utilisation, sur la base des résultats d’un  processus en deux volets, à savoir la classification des données et une évaluation complète du risque lié aux TIC.
- Un aspect essentiel est la séparation stricte entre  les environnements de production des TIC, d’une part, et les environnements dans lesquels les systèmes de TIC sont  développés et testés, ou les autres environnements hors production, d’autre part.
- La gestion des correctifs devrait être un élément essentiel des politiques et procédures de sécurité des TIC qui, grâce  aux tests et au déploiement dans un environnement contrôlé, doivent permettre de remédier aux vulnérabilités  identifiées et d’éviter des perturbations lors de l’installation de correctifs. 
- si une entreprise SaaS découvre une faille de sécurité, elle doit avoir un processus clair pour prévenir les bonnes personnes (clients, partenaires, public) au bon moment, plutôt que de cacher le problème ou de communiquer n'importe comment (gravité, impact, solution)
- Chaque personne (et chaque système/API) qui accède aux données doit avoir son propre identifiant unique (HashiCorp Vault, IAM)


## For who ?

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
