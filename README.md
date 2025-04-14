# Cours : Introduction à l’Architecture Logicielle

## 🔑 1. Notions de base en architecture logicielle

### 1.1. Composants

Un **composant logiciel** est une unité fonctionnelle autonome. Il regroupe des fonctions et des données associées, et peut interagir avec d’autres composants via des interfaces.

#### ✅ Exemples :
- **Base de données** : composant responsable du stockage des données.
- **Interface utilisateur (UI)** : permet à l’utilisateur d’interagir avec le logiciel.
- **API REST** : composant qui expose des fonctionnalités via HTTP.

#### 🎯 Objectifs :
- Permettre la **réutilisation**.
- Favoriser la **testabilité**.
- Faciliter le **remplacement** et la **maintenance**.

---

### 1.2. Couches (Layers)

L’architecture en **couches** est un modèle de conception logique du logiciel, séparant les responsabilités.

#### 📚 Couches classiques :
1. **Présentation (UI)** : interface visible par l’utilisateur.
2. **Logique métier (Business Logic)** : règles du domaine.
3. **Accès aux données (Data Access Layer)** : communication avec la base de données.

#### 🛒 Exemple (application e-commerce) :
- **UI** → Affichage des produits.
- **Logique métier** → Calcul de promotions.
- **DAL** → Lecture/écriture en base.

---

### 1.3. Modularité

La **modularité** consiste à diviser une application en **modules indépendants** avec des responsabilités claires.

#### 🧩 Exemple :
Dans une app de gestion scolaire :
- Module "Étudiants"
- Module "Cours"
- Module "Notes"
- Module "Authentification"

#### ✅ Avantages :
- Code plus **lisible**, **réutilisable**.
- Maintenance facilitée.

---

### 1.4. Responsabilités

Le **principe de responsabilité unique** (SRP) dit qu’un module, classe ou fonction doit **faire une seule chose**.

#### 🧠 Application :
- **Controller** : reçoit les requêtes.
- **Service** : applique les règles métier.
- **Repository** : gère la persistance.

---

## 🧱 2. Types d’architectures courantes

### 2.1. Architecture Monolithique

#### 🧱 Définition :
L’application est un **bloc unique**, tout est regroupé dans un seul déploiement.

#### ✅ Avantages :
- Simple à développer et déployer.
- Moins de complexité initiale.

#### ❌ Inconvénients :
- Difficile à faire évoluer.
- Risque élevé de bugs globaux.

#### 🔧 Cas d’usage :
- Petits projets, MVP, prototypes.

---

### 2.2. Architecture N-tiers (ex. 3 tiers)

#### 🧱 Structure :
1. **Présentation**
2. **Logique métier**
3. **Données**

#### ✅ Avantages :
- Bonne **séparation des responsabilités**.
- Maintenance facilitée.

#### ❌ Inconvénients :
- Plus de **latence** entre couches.
- Peut devenir rigide.

#### 🔧 Cas d’usage :
- Applications web classiques, CRM, ERP.

---

### 2.3. Architecture Client-Serveur

#### 🧱 Définition :
Deux entités distinctes :
- **Client** : UI, envoie des requêtes.
- **Serveur** : traite les données et répond.

#### ✅ Avantages :
- Facile à comprendre.
- Clients multiples possibles.

#### ❌ Inconvénients :
- Le serveur est un point de défaillance unique.

#### 🔧 Cas d’usage :
- Sites web, jeux en ligne, outils en réseau.

---

### 2.4. Architecture Microservices

#### 🧱 Définition :
Application décomposée en **services indépendants**, chacun responsable d’un domaine.

#### ✅ Avantages :
- **Scalabilité fine**.
- Déploiement et mise à jour indépendants.
- Choix technologique libre par service.

#### ❌ Inconvénients :
- Plus complexe (orchestration, tests, CI/CD).
- Besoin de DevOps solide.

#### 🔧 Cas d’usage :
- Grands systèmes distribués, SaaS à grande échelle.

---

### 2.5. Architecture Event-Driven (orientée événements)

#### 🧱 Définition :
Les composants interagissent via des **événements** (asynchrones).

#### ✅ Avantages :
- Forte **découplage**.
- Bonne réactivité, extensibilité.

#### ❌ Inconvénients :
- **Debugging difficile**.
- Tests plus complexes.

#### 🔧 Cas d’usage :
- Systèmes temps réel, IoT, applications financières.

---

### 2.6. Architecture Hexagonale (Ports & Adapters)

#### 🧱 Définition :
- Le cœur de l’application (logique métier) est **indépendant** des détails techniques.
- Communication via **ports** (interfaces).
- Interaction avec l’extérieur via **adapters** (implémentations).

#### ✅ Avantages :
- Code testable et **technologiquement indépendant**.
- Grande **flexibilité** à long terme.

#### ❌ Inconvénients :
- Courbe d’apprentissage plus élevée.
- Parfois surdimensionné pour de petits projets.

#### 🔧 Cas d’usage :
- Domain-Driven Design (DDD), projets à long cycle de vie.

---

