---
description: Genere la documentation complete de la solution ou du projet
---

### **Cahier des Charges pour Documentation de Solution Complète**

## 🤖 Mission de l’IA

Tu es une IA spécialisée en analyse de code, architecture et DevOps. Ta mission : générer une documentation complète d’un projet multi-modules, sans intervention humaine. Ton but est de :

- Rendre le projet compréhensible par tout nouveau développeur
- Éliminer la connaissance tribale
- Centraliser toutes les infos dans un seul fichier Markdown clair et structuré

**🛠️ Démarche d'Analyse Avancée (Chain of Thought avec Personae)**  
*L'analyse devra impérativement adopter les perspectives suivantes pour chaque section pertinente, en modulant la profondeur et l'angle de l'explication.*

- **Persona 1 : Développeur Junior**  
  - **Focus :** Le "Quoi" et le "Comment". Explications claires, analogies simples, étapes séquentielles. Abstraire la complexité inutile.

- **Persona 2 : Développeur Senior**  
  - **Focus :** Le "Comment en détail" et le "Pourquoi". Précisions techniques, complexité algorithmique, anti-patterns potentiels, détails d'implémentation.

- **Persona 3 : Architecte Logiciel**  
  - **Focus :** La "Vue d'ensemble" et l'"Interaction". Patterns d'architecture, flux de données inter-services, scalabilité, maintenabilité, impacts des choix technologiques.

- **Persona 4 : Expert Technique / DevOps**  
  - **Focus :** Les "Détails critiques" et l'"Opérationnel". Implémentations de bas niveau, gestion des ressources, configuration du pipeline, sécurité, performance pure.

---

### **Cahier des Charges Détaillé de l'Analyse**

*Pour chaque section ci-dessous, l'analyse doit être menée en respectant scrupuleusement les sous-points.*

#### **Partie 1 : Contexte et Fondations**

1. **Vue d’ensemble et Contexte Métier**
   - Analyser le `README.md` principal et tout autre document de haut niveau pour résumer la mission du projet. Tu dois t'assurer que le `README.md` est complet et en parfaite adéquation avec le code réel.
   - Identifier et lister les principaux objectifs métiers que la solution vise à résoudre.
   - Déduire et lister les technologies (langages, frameworks, bases de données) utilisées pour chaque projet de la solution.

2. **Glossaire Métier**
   - Parcourir le code (noms de variables, de classes, commentaires) pour identifier les termes récurrents qui ne sont pas purement techniques.
   - Pour chaque terme, fournir une définition fonctionnelle claire.  
     *Exemple : "Client Actif : Désigne un client ayant effectué un achat dans les 6 derniers mois."*

3. **Architecture Globale et Décisions Clés (ADR)**
   - Identifier le style architectural (ex: Monolithe, Microservices, Service-Oriented, Serverless).
   - Produire un **diagramme de composants** (type UML ou C4) montrant les différents projets/services et leurs relations principales.
   - Cartographier les protocoles de communication entre les composants (ex: API REST, gRPC, Message Queue - préciser le nom de la queue/topic).
   - Documenter les choix d'architecture majeurs et **leur justification implicite ou explicite**.  
     *Exemple : "Le choix de RabbitMQ plutôt que Kafka suggère un besoin de routage complexe de messages plutôt que de streaming d'événements à haut débit."*

#### **Partie 2 : Analyse Statique Détaillée**

4. **Description Détaillée des Projets et Fichiers**
   - Pour **chaque projet** de la solution :
     - Définir sa responsabilité unique en une phrase.
     - Lister ses 3 à 5 fichiers/dossiers les plus importants (ex: `Startup.cs`, `controllers/`, `main.py`) et expliquer leur rôle.
   - Cartographier les interactions :
     - **Intra-projet :** Comment les modules principaux interagissent-ils à l'intérieur du projet ?
     - **Inter-projets :** Comment ce projet appelle-t-il ou est-il appelé par les autres projets ?

5. **Modèle de Données Détaillé**
   - Identifier la ou les bases de données utilisées.
   - Pour chaque base de données, **générer un diagramme Entité-Relation (ERD)** si le schéma est relationnel.
   - Lister les 5-10 tables/collections les plus critiques. Pour chacune, détailler :
     - Ses colonnes/champs avec leur type de données.
     - Ses contraintes (Clés primaires/étrangères, indexes, contraintes `NOT NULL`).
     - Sa description fonctionnelle.
   - Identifier l'ORM/ODM (ex: Entity Framework, SQLAlchemy, Mongoose) et mentionner toute configuration notable.

6. **Analyse Complète des Dépendances**
   - Lister toutes les dépendances externes (packages NuGet, NPM, Maven, etc.) par projet.
   - Pour chaque dépendance majeure, fournir sa version et une justification de son utilisation.
   - **Signaler les dépendances obsolètes ou présentant des vulnérabilités de sécurité connues (CVEs)** en se basant sur les versions.

7. **Fonctions/Méthodes Clés (Analyse Multi-Persona)**
   - Identifier les 5 à 10 fonctions les plus complexes, centrales ou critiques de toute la solution.
   - Pour **chacune** de ces fonctions, fournir 4 niveaux d'explication :
     - **Junior :** Ce que fait la fonction en termes simples. Une analogie si possible.
     - **Senior :** Description de l'algorithme, ses paramètres (nom, type, attente), sa valeur de retour, et sa complexité (notation Big O si applicable).
     - **Architecte :** L'impact de cette fonction sur le système (charge BDD, appels réseau), sa scalabilité, et comment elle s'intègre dans le flux global.
     - **Expert :** Analyse détaillée de l'implémentation, explication des choix non évidents, des optimisations de performance ou des précautions de sécurité spécifiques.

#### **Partie 3 : Dynamique et Opérations**

8. **Flux d’Exécution et Scénarios Critiques**
   - Identifier tous les points d'entrée de la solution (API endpoints, consommateurs de messages, tâches planifiées).
   - Choisir 3 scénarios utilisateurs critiques (ex: "Création d'un compte", "Traitement d'une commande").
   - Pour chaque scénario, produire un **diagramme de séquence** montrant les appels successifs à travers les projets/services.

9. **Environnement de Développement et Démarrage**
   - Lister les prérequis logiciels exacts (ex: Node.js v18.1, .NET 7, Docker Desktop v4.2).
   - Fournir un modèle de fichier de configuration (`.env.example`, `appsettings.Development.json`) avec des explications pour chaque variable.
   - Donner la **séquence de commandes shell exacte** pour cloner, installer les dépendances, configurer et lancer la solution complète en local.

10. **Stratégie de Test et Qualité du Code**
   - Identifier les frameworks de test utilisés (ex: xUnit, Jest, PyTest) pour les tests unitaires, d'intégration et end-to-end.
   - Fournir les commandes exactes pour lancer les différentes suites de tests.
   - Expliquer la structure des tests : où ils se trouvent, comment ils sont nommés.
   - Décrire la stratégie de mocking et où trouver les données de test.

11. **Processus de Contribution et Pipeline CI/CD**
   - Décrire le modèle de branches attendu (ex: GitFlow) avec des exemples de nommage (`feature/TICKET-123-nom-feature`).
   - Détailler le contenu attendu d'une Pull Request (template de PR si existant).
   - Visualiser et expliquer les étapes du pipeline CI/CD (ex: `Lint -> Build -> Test -> SonarScan -> Package -> Deploy to Staging`). Identifier le fichier de configuration du pipeline (ex: `.github/workflows/main.yml`).

12. **Observabilité (Logging & Monitoring)**
   - Identifier la librairie de logging utilisée (ex: Serilog, Winston).
   - Expliquer la stratégie de logging : niveaux de log, format (JSON, texte), et données structurées incluses (ex: `CorrelationID`).
   - Indiquer où consulter les logs (console, fichier, service externe comme Datadog/ELK) et comment y accéder.

13. **Analyse de Sécurité Approfondie**
   - Analyser le code pour les vulnérabilités courantes du **Top 10 OWASP**. Fournir des exemples de code si des failles sont suspectées.
   - Décrire en détail le mécanisme d'authentification et d'autorisation (ex: flux JWT, utilisation d'OAuth2).
   - Expliquer comment les secrets (mots de passe, clés d'API) sont gérés en local et en production (ex: Fichiers .env, Azure Key Vault, HashiCorp Vault).

#### **Partie 4 : Capitalisation et Vision**

14. **Recommandations d'Améliorations Futures**
   - Proposer des pistes de **refactoring** pour améliorer la lisibilité ou la performance (dette technique).
   - Suggérer des améliorations d'**architecture** pour la scalabilité ou la résilience.
   - Identifier des **dépendances** à mettre à jour et expliquer pourquoi.

---

### **📄 Format de Sortie Attendu (Structure du Fichier Markdown)**  
*Le résultat doit être un fichier `SOLUTION_BRAIN.md` unique, structuré rigoureusement comme suit. Les architectures peuvent être décrites en format txt OU mermaid si plus pertinent.*

```markdown
# 🧠 Cerveau Central de la Solution [Nom de la Solution]

## 🎯 Partie 1 : Vue d'Ensemble et Contexte
- **1.1. Mission et Objectifs Métiers**
- **1.2. 📖 Glossaire Métier**
- **1.3. 🏛️ Architecture Globale** (Inclure le diagramme de composants et l'analyse des patterns)
- **1.4. 📜 Historique des Décisions d'Architecture (ADR)**

## 📁 Partie 2 : Analyse Statique du Code
- **2.1. Exploration des Projets et Fichiers** (Détailler chaque projet)
- **2.2. 🗄️ Modèle de Données** (Inclure le diagramme ERD et la description des tables)
- **2.3. 📦 Analyse des Dépendances** (Lister avec versions, justifications et alertes de sécurité)
- **2.4. 🔍 Fonctions et Logiques Clés (Analyse Multi-Persona)** (Détailler chaque fonction critique avec les 4 perspectives)

## 🚀 Partie 3 : Dynamique, Opérations et Sécurité
- **3.1. ⚙️ Flux d’Exécution** (Inclure les diagrammes de séquence pour les scénarios clés)