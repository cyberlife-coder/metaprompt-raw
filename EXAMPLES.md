# Exemples d'Utilisation des Workflows

Ce document fournit des exemples concrets d'utilisation pour chaque workflow disponible dans ce projet. Ces exemples montrent comment les développeurs peuvent utiliser efficacement ces métaprompts dans leur travail quotidien.

## 🛡️ /audit-pentest - Audit de Sécurité et Pentesting

### Situation d'usage
Vous venez de déployer une nouvelle application web et souhaitez effectuer un audit de sécurité complet avant d'ouvrir l'accès aux utilisateurs.

### Exemple d'appel
```
/audit-pentest

Veuillez effectuer un audit de sécurité complet de notre application de gestion de commandes. L'application est développée en Node.js avec Express, utilise MongoDB pour la persistance des données, et est déployée sur Azure App Service. Voici les points d'entrée principaux à analyser :

1. API d'authentification (/api/auth)
2. API de gestion des commandes (/api/orders)
3. Interface utilisateur admin (/admin)

Veuillez identifier les vulnérabilités de type OWASP Top 10, notamment les injections, les failles XSS, les problèmes de gestion des sessions, et les mauvaises configurations de sécurité.
```

### Résultat attendu
Un rapport de sécurité détaillé dans `SECURITY_AUDIT_REPORT_CONCISE.md` incluant :
- Cartographie de la surface d'attaque
- Vulnérabilités identifiées avec niveaux de criticité
- Preuves de concept (PoC) pour les vulnérabilités critiques
- Recommandations de remédiation prioritaires

## 🐛 /debug-taskforce - Débogage Expert Multi-Experts

### Situation d'usage
Votre application rencontre une erreur intermittente en production qui ne se reproduit pas en développement, causant des timeouts aléatoires.

### Exemple d'appel
```
/debug-taskforce

Nous rencontrons des timeouts intermittents en production sur notre service de traitement des paiements. L'erreur suivante apparaît dans les logs :

```
Error: TimeoutError: Operation timed out after 30000 ms
    at PaymentService.processPayment (/app/services/payment.js:45:12)
    at processTicksAndRejections (internal/process/task_queues.js:93:5)
```

Fichiers concernés :
- `/app/services/payment.js` (service principal)
- `/app/utils/database.js` (connexions DB)
- `/app/config/production.js` (configuration prod)

Le problème semble survenir principalement pendant les pics de trafic (~500 requêtes/minute). Aidez-nous à identifier la cause racine.
```

### Résultat attendu
Une analyse approfondie avec :
- Identification de la cause racine par les experts
- Analyse des interactions entre composants
- Recommandations de solutions concrètes
- Priorisation des actions correctives

## 📚 /doc-solution-brain - Documentation Technique Complète

### Situation d'usage
Vous rejoignez un projet complexe avec plusieurs microservices et avez besoin de comprendre rapidement l'architecture globale.

### Exemple d'appel
```
/doc-solution-brain

Documentez la solution complète de notre plateforme e-commerce. La solution comprend les composants suivants :

1. Frontend Next.js (dossier /frontend)
2. API Gateway (dossier /gateway)
3. Service catalogue produits (dossier /product-service)
4. Service gestion des commandes (dossier /order-service)
5. Service gestion des utilisateurs (dossier /user-service)
6. Base de données PostgreSQL (schéma dans /database)

Veuillez produire une documentation complète incluant l'architecture, les flux de données, les APIs, et les dépendances.
```

### Résultat attendu
Un document `SOLUTION_BRAIN.md` contenant :
- Vue d'ensemble de l'architecture
- Diagramme des composants et flux de données
- Description détaillée de chaque service
- Glossaire des termes métier
- Informations sur le déploiement et la configuration

## 🏗️ /feature-architect - Architecture de Nouvelles Fonctionnalités

### Situation d'usage
Vous souhaitez ajouter un système de notifications push à votre application existante.

### Exemple d'appel
```
/feature-architect

Ajoutez un système de notifications push à notre application de messagerie instantanée. Les exigences sont :

- Notifications en temps réel pour les nouveaux messages
- Support des plateformes iOS, Android et Web
- Personnalisation des préférences de notification par utilisateur
- Tolérance aux pannes et scalabilité

Stack actuelle : React Native (mobile), React (web), Node.js/Express (backend), MongoDB, Redis

Veuillez concevoir l'architecture et fournir un plan d'implémentation.
```

### Résultat attendu
Un plan architectural complet avec :
- Design de l'architecture de notification
- Choix technologiques justifiés
- Plan d'implémentation détaillé
- Tests et scénarios de déploiement

## 🎨 /feature-ui-ux - Design UI/UX et Développement

### Situation d'usage
Vous devez refondre l'interface utilisateur de votre tableau de bord administrateur pour améliorer l'expérience utilisateur.

### Exemple d'appel
```
/feature-ui-ux

Refondez l'interface du tableau de bord administrateur de notre plateforme de gestion de contenu. Problèmes actuels :

- Navigation complexe avec trop de menus
- Temps de chargement élevé des données
- Manque de visualisations de données
- Problèmes d'accessibilité (non conforme WCAG)

Contenu actuel :
- Statistiques de trafic
- Gestion des articles
- Modération des commentaires
- Gestion des utilisateurs

Veuillez proposer une nouvelle interface moderne, accessible et performante.
```

### Résultat attendu
Des livrables incluant :
- Wireframes et maquettes UX
- Composants UI implémentables
- Guidelines d'accessibilité
- Plan de migration de l'interface existante

## 💡 /ideation-product - Idéation Produit

### Situation d'usage
Votre équipe cherche à identifier de nouvelles fonctionnalités pour améliorer l'engagement des utilisateurs.

### Exemple d'appel
```
/ideation-product

Identifiez de nouvelles fonctionnalités pour notre application de fitness mobile. Actuellement, l'application propose :

- Suivi d'entraînements
- Suivi alimentaire
- Communauté d'utilisateurs
- Intégration avec des appareils wearables

Objectif : Augmenter l'engagement quotidien et le taux de rétention à 30 jours. Notre cible principale est les adultes de 25-45 ans soucieux de leur santé.

Veuillez proposer 5 idées de fonctionnalités innovantes avec leur priorité et leur impact attendu.
```

### Résultat attendu
Une proposition structurée avec :
- 5 idées de fonctionnalités détaillées
- Analyse de marché et personas
- Priorisation basée sur impact/effort
- Roadmap de développement suggérée

## 🔧 /migrate-webservice - Migration de Webservices

### Situation d'usage
Vous devez migrer un ancien service WCF vers une API REST moderne.

### Exemple d'appel
```
/migrate-webservice

Migrez notre service WCF de gestion des inventaires vers une API REST en .NET Core. Contraintes :

- Doit utiliser les procédures stockées existantes (SQL Server)
- Doit maintenir la compatibilité avec les clients existants pendant 6 mois
- Doit inclure une documentation OpenAPI/Swagger
- Doit être déployable via Azure DevOps

Fichiers à analyser :
- ServiceContract.cs
- InventoryService.svc.cs
- DataModels.cs

Veuillez fournir un plan de migration et une implémentation pilote.
```

### Résultat attendu
Des livrables incluant :
- Plan de migration détaillé
- Implémentation d'un endpoint pilote
- Documentation API
- Stratégie de déploiement

## 🔍 /scan-trivy - Scan de Sécurité Trivy

### Situation d'usage
Avant un déploiement en production, vous souhaitez vérifier les vulnérabilités de dépendances.

### Exemple d'appel
```
/scan-trivy

Effectuez un scan de sécurité complet de notre projet Node.js. Veuillez analyser :

- package.json et package-lock.json
- Dossier node_modules/
- Dockerfile de production

Identifiez toutes les vulnérabilités avec un score CVSS >= 7.0 et proposez un plan de remédiation.
```

### Résultat attendu
Un rapport de sécurité avec :
- Liste des vulnérabilités identifiées
- Niveau de criticité et CVSS scores
- Recommandations de mise à jour
- Plan d'action de remédiation

## 🗃️ /sql-refactor - Refactorisation SQL Server

### Situation d'usage
Vous avez une procédure stockée complexe qui prend plusieurs minutes à s'exécuter et cause des problèmes de performance en production.

### Exemple d'appel
```
/sql-refactor

Optimisez cette procédure stockée qui prend plus de 5 minutes à s'exécuter lorsqu'elle traite plus de 100 000 enregistrements :

```sql
CREATE PROCEDURE [dbo].[GetCustomerOrdersReport]
    @StartDate DATE,
    @EndDate DATE,
    @CustomerID INT = NULL
AS
BEGIN
    SELECT 
        c.CustomerName,
        c.Email,
        o.OrderID,
        o.OrderDate,
        p.ProductName,
        od.Quantity,
        od.UnitPrice,
        (od.Quantity * od.UnitPrice) AS TotalPrice
    FROM Customers c
    INNER JOIN Orders o ON c.CustomerID = o.CustomerID
    INNER JOIN OrderDetails od ON o.OrderID = od.OrderID
    INNER JOIN Products p ON od.ProductID = p.ProductID
    WHERE o.OrderDate BETWEEN @StartDate AND @EndDate
        AND (@CustomerID IS NULL OR c.CustomerID = @CustomerID)
    ORDER BY o.OrderDate DESC, c.CustomerName
END
```

Contexte : Base de données SQL Server 2019, environ 2 millions de commandes, 500 000 clients. La procédure est appelée plusieurs fois par heure par l'application web.

Veuillez analyser et proposer une version optimisée avec un plan de mise en production.
```

### Résultat attendu
Des livrables incluant :
- Code SQL refactorisé avec améliorations de performance
- Analyse détaillée des gains attendus
- Index suggérés
- Zones de risque identifiées
- Instructions de mise en production

---

*Ce document a été généré pour aider les développeurs à utiliser efficacement les workflows de cette collection.*
