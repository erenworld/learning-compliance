# DORA

- Afin de limiter le risque de conflits d’intérêts, les entités financières devraient veiller à la séparation des tâches lors de  l’attribution de rôles et de responsabilités 
- Afin de garantir une bonne gestion du risque lié aux systèmes de TIC hérités, les entités financières devraient  enregistrer et surveiller les dates d’expiration des services TIC d’appui fournis par des tiers.
- DAMIEN CLOCHARD m'a parlé de ça : Les contrôles cryptographiques peuvent garantir la disponibilité, l’authenticité, l’intégrité et la confidentialité des  données. Les entités financières visées au titre II du présent règlement devraient donc définir et mettre en œuvre ces  contrôles sur la base d’une approche fondée sur les risques. À cette fin, les entités financières devraient chiffrer les  données concernées, au repos, en transit ou, si nécessaire, en cours d’utilisation, sur la base des résultats d’un  processus en deux volets, à savoir la classification des données et une évaluation complète du risque lié aux TIC.
- Un aspect essentiel est la séparation stricte entre  les environnements de production des TIC, d’une part, et les environnements dans lesquels les systèmes de TIC sont  développés et testés, ou les autres environnements hors production, d’autre part.
- La gestion des correctifs devrait être un élément essentiel des politiques et procédures de sécurité des TIC qui, grâce  aux tests et au déploiement dans un environnement contrôlé, doivent permettre de remédier aux vulnérabilités  identifiées et d’éviter des perturbations lors de l’installation de correctifs. 
- si une entreprise SaaS découvre une faille de sécurité, elle doit avoir un processus clair pour prévenir les bonnes personnes (clients, partenaires, public) au bon moment, plutôt que de cacher le problème ou de communiquer n'importe comment (gravité, impact, solution)
- Chaque personne (et chaque système/API) qui accède aux données doit avoir son propre identifiant unique (HashiCorp Vault, IAM)


## Card 1
Q: For who ?

A: DORA is aimed specifically at EU-based financial entities and ICT service providers.

## Card 2
Q: Who is financial entities ?

A: 
- Payment and credit institutions
- Electronic money institutions
- Investment firms
- Insurance companies
- Trade repositories

## Card 3 
Q: Who is ICT providers ?

A: Cloud providers
Network security companies
IT consulting firms
Managed IT service providers
Help desk service providers

## Card 4
Q: 5 key compliance requirements of DORA

A: 
- ICT risk management
- ICT-related incident management
- Digital operational resilience testing
- ICT third-party risk management
- Information sharing

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

### To implement

- https://security.finic.ai/?tab=compliance  
- https://trust.openrouter.ai/ 
- https://trust.openzeppelin.com/
- Access Reviews & Least-Privilege Enforcement tool, Replace manual data gathering with automated discovery. Auto user discovery Single review interface One-click actions github
- Employee Portal Security shouldn't slow down deals. Device compliance Security training Workforce management
