# MetaPrompt Raw - Collection de Workflows Techniques

> **Collection précise de métaprompts techniques** - Analyse exacte et documentation rigoureuse basée sur le contenu réel des fichiers

## 📋 Vue d'ensemble

Ce projet contient une collection de **métaprompts techniques** analysés et documentés avec précision. Chaque fichier représente un workflow spécialisé avec des objectifs, méthodologies et formats de sortie définis. Les métaprompts sont conçus pour l'utilisation avec Windsurf IDE et d'autres environnements d'IA.

## 🏗️ Structure exacte du projet

```
metaprompt-raw/
├── workflows/                 # Fichiers de métaprompts
│   ├── audit-pentest.md       # Audit de sécurité et pentesting
│   ├── debug-taskforce.md     # Task force de débogage multi-experts
│   ├── doc-solution-brain.md  # Documentation technique complète
│   ├── feature-architect.md   # Architecture de nouvelles fonctionnalités
│   ├── feature-ui-ux.md       # Design UI/UX et développement
│   ├── ideation-product.md    # Idéation produit
│   ├── migrate-webservice.md  # Migration de webservices v8
│   └── scan-trivy.md          # Scan de sécurité Trivy
├── docs/                      # Dossier documentation supplémentaire
├── templates/                 # Dossier templates et exemples
└── README.md                  # Documentation principale
```

## 📋 Description précise de chaque métaprompt

### 🛡️ **audit-pentest.md**
**Cahier des charges pour audit de sécurité et pentesting**
- **Objectif** : Analyse offensive autonome de sécurité
- **Méthodologie** : 4 personae (Architecte sécurité, Auditeur, Pentester, Remediator)
- **Format de sortie** : `SECURITY_AUDIT_REPORT_CONCISE.md`
- **Sections** : Surface d'attaque, vulnérabilités, PoC, remédiation
- **Focus** : Rapport synthétique avec preuves de concept concrètes

### 🐛 **debug-taskforce.md**
**Task force de débogage multi-experts**
- **Objectif** : Résolution systématique de problèmes complexes
- **Équipe** : Melanie (testeuse experte), Paul (testeur expert), Fabrice (architecte), François (SecDevOps)
- **Processus** : 6 étapes - analyse individuelle, challenge collectif, priorisation, root cause
- **Format** : Discussion multi-experts avec validation utilisateur
- **Focus** : Identification précise de la cause racine

### 📚 **doc-solution-brain.md**
**Documentation technique complète**
- **Objectif** : Analyse autonome d'une solution logicielle multi-projets
- **Méthodologie** : Chain of Thought avec 4 personae (Junior, Senior, Architecte, DevOps)
- **Format de sortie** : Document Markdown unique `SOLUTION_BRAIN.md`
- **Sections** : Vue d'ensemble, architecture, modèle de données, fonctions clés, CI/CD, sécurité
- **Focus** : Documentation exhaustive éliminant la connaissance tribale

### 🏗️ **feature-architect.md**
**Architecture de nouvelles fonctionnalités**
- **Objectif** : Orchestration de nouvelles fonctionnalités multi-experts
- **Méthodologie** : 5 experts (Product Manager, Architecte, Dev, QA, DevOps)
- **Processus** : Analyse, conception, implémentation, tests, déploiement
- **Format** : Planification structurée avec validation à chaque étape
- **Focus** : Architecture robuste et évolutive

### 🎨 **feature-ui-ux.md**
**Design UI/UX et développement**
- **Objectif** : Task-force multidisciplinaire UI/UX/Dev/QA
- **Équipe** : Designer UX, Designer UI, Développeur Frontend, QA, DevOps
- **Processus** : Recherche utilisateur, design, prototypage, développement, tests
- **Format** : Collaboration étroite entre design et développement
- **Focus** : Expérience utilisateur optimale et implémentation technique

### 💡 **ideation-product.md**
**Idéation produit**
- **Objectif** : Processus d'idéation et validation produit
- **Méthodologie** : Analyse marché, définition MVP, roadmap
- **Format** : Framework structuré pour innovation produit
- **Focus** : Produit/market fit et stratégie produit

### 🔧 **migrate-webservice.md**
**Migration de webservices v8**
- **Objectif** : Moteur d'analyse et migration de webservices version 8
- **Méthodologie** : Analyse de compatibilité, stratégie de migration
- **Format** : Guide technique complet pour migrations complexes
- **Focus** : Migration sans downtime et validation exhaustive

### 🔍 **scan-trivy.md**
**Scan de sécurité Trivy**
- **Objectif** : Scan de sécurité automatisé avec Trivy
- **Méthodologie** : Analyse des vulnérabilités et problèmes de sécurité
- **Format** : Rapport de sécurité structuré
- **Focus** : Sécurité continue et dépendances à jour

## 🎯 Utilisation précise

### Méthode 1 : Via slash commands
```
/audit-pentest          # Audit de sécurité
/debug-taskforce        # Débogage expert
/doc-solution-brain     # Documentation complète
/feature-architect      # Architecture features
/feature-ui-ux          # Design UI/UX
/migrate-webservice     # Migration webservices
/scan-trivy            # Scan sécurité
```

### Méthode 2 : Copier-coller direct
1. Ouvrir le fichier workflow souhaité
2. Copier le contenu complet
3. Coller dans Windsurf ou autre IDE IA
4. Exécuter avec le contexte approprié

### Méthode 3 : Personnalisation
1. Dupliquer un fichier workflow
2. Adapter les sections selon les besoins
3. Sauvegarder dans `templates/` pour réutilisation
4. Documenter les modifications

### Méthode 4 : Exemples d'utilisation
Des exemples concrets d'utilisation pour chaque workflow sont disponibles dans le fichier [EXAMPLES.md](EXAMPLES.md). Ce fichier montre des situations réelles et des appels typiques pour chaque métaprompt.

## 📋 Format et structure des workflows

### Structure commune
- **En-tête YAML** : Description précise du workflow
- **Objectif** : Définition claire du but
- **Méthodologie** : Processus étape par étape
- **Personae** : Rôles et perspectives (quand applicable)
- **Format de sortie** : Structure attendue du résultat
- **Sections détaillées** : Instructions spécifiques pour chaque aspect

### Types de workflows
- **Analyse technique** : doc-solution-brain.md
- **Sécurité** : audit-pentest.md, scan-trivy.md
- **Débogage** : debug-taskforce.md
- **Architecture** : feature-architect.md, migrate-webservice.md
- **Design** : feature-ui-ux.md
- **Produit** : ideation-product.md

## 🔧 Bonnes pratiques

### Avant utilisation
- Lire la description YAML complète
- Identifier le persona approprié
- Préparer le contexte nécessaire
- Valider la structure des outputs

### Pendant l'utilisation
- Suivre exactement la méthodologie
- Respecter les formats de sortie spécifiés
- Documenter les adaptations nécessaires
- Valider les résultats intermédiaires

### Après utilisation
- Réviser les outputs selon les standards
- Documenter les cas d'usage réussis
- Partager les améliorations possibles
- Maintenir les versions à jour

## 📄 Licence

### Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International

[![License: CC BY-NC-SA 4.0](https://licensebuttons.net/l/by-nc-sa/4.0/80x15.png)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

Ce projet est sous licence **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)**.

**[🔗 Lien officiel de la licence](https://creativecommons.org/licenses/by-nc-sa/4.0/)**

### Permissions
- ✅ **Utilisation, reproduction et distribution libres** pour usage non-commercial
- ✅ **Modification et création d'œuvres dérivées**
- ✅ **Distribution interne et open-source**

### Conditions
- 🔗 **Attribution obligatoire** : mentionner l'auteur (Cyberlife-coder)
- 🔗 **ShareAlike** : partager les modifications sous la même licence CC BY-NC-SA 4.0
- ❌ **NonCommercial** : interdit l'usage commercial sans accord explicite

### Usage Commercial
Pour toute utilisation commerciale :
- 📧 **Contact** : cyberlife-coder pour obtenir une licence commerciale séparée
- 💼 **Contrat dual-licensing** disponible (modèle open-core)

### Comment citer ce projet
```
MetaPrompt Raw Collection
Copyright (c) 2025 Cyberlife-coder
Licensed under CC BY-NC-SA 4.0
https://creativecommons.org/licenses/by-nc-sa/4.0/
```


**Auteur** : Cyberlife-coder  
**Date de mise à jour** : 01/08/2025  
**Version** : 3.1.0 (basée sur analyse exacte des fichiers existants)  