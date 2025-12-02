# 📅 Projet : Agenda Étudiant - Gestion d'Emploi du Temps

## Introduction

Ceci est le code source de l'application **Agenda Étudiant**, développée dans le cadre du projet de développement mobile Android. L'application a pour but d'offrir aux utilisateurs (étudiants) une solution simple et efficace pour **consulter, ajouter, modifier et supprimer** les cours et activités de leur semaine universitaire.

Le projet respecte l'ensemble des **fonctionnalités attendues** et des **objectifs pédagogiques** énoncés dans le cahier des charges, notamment l'utilisation de l'architecture MVVM et la persistance des données via Room.

---

## 🚀 Fonctionnalités Implémentées

L'application couvre les fonctionnalités principales suivantes :

1.  **Affichage de l'Emploi du Temps**
    * Liste réactive des cours (via **LiveData** et **RecyclerView**).
    * Tri par jour de la semaine et heure de début.
2.  **Opérations CRUD Complètes (Ajout, Modification, Suppression)**
    * Formulaire de saisie pour le nom, professeur, salle, jour, heures (début/fin), et type de cours (CM/TD/TP).
    * Validation des champs (non-vides, cohérence des heures).
3.  **Filtrage et Recherche Dynamique**
    * Barre de recherche intégrée (SearchView) permettant de filtrer instantanément les cours par **nom**, **professeur**, **salle** ou **jour de la semaine**.
4.  **Persistance des Données**
    * Utilisation de la bibliothèque **Room** (couche au-dessus de SQLite) pour le stockage local fiable.
5.  **Notifications de Rappel (Bonus)** 🔔
    * Implémentation d'un système de rappel hebdomadaire 10 minutes avant le début de chaque cours, géré par l'**AlarmManager**.
6.  **Ergonomie et Design**
    * Utilisation des composants **Material Design** pour une interface moderne et soignée (CardView, TextInputLayout, FloatingActionButton).

---

## 📐 Architecture Technique

Le projet suit rigoureusement le pattern **MVVM (Model-View-ViewModel)** recommandé par Google, garantissant la séparation des préoccupations et la gestion correcte du cycle de vie.

* **View (`.view`)** : `MainActivity`, `AddEditCourseActivity`, `CourseAdapter`. S'occupe de l'affichage et de la gestion des événements UI.
* **ViewModel (`.viewmodel`)** : `CourseViewModel`. Gère la logique d'affichage et fournit les données à la `View` via `LiveData`.
* **Repository (`.repository`)** : `CourseRepository`. Fait le lien entre le `ViewModel` et les sources de données locales/distantes.
* **Data (`.model`, `.db`)** : Contient l'entité `Course` et les composants Room (`AppDatabase`, `CourseDao`).

| Technologie      | Rôle                                                      |
| :---             | :---                                                      |
| **Room**         | Persistance des données (stockage des cours).             |
| **LiveData**     | Réactivité de l'UI (mise à jour automatique de la liste). |
| **AlarmManager** | Planification des notifications récurrentes.              |
| **RecyclerView** | Affichage de la liste des cours triée et filtrée.         |

---

## ⚙️ Installation et Démarrage

### Pré-requis

* Android Studio (version Arctic Fox 2020.3.1 ou supérieure)
* SDK Android API 33 (ou version utilisée pour la compilation)

### Instructions de Compilation

1.  **Cloner le dépôt :**
    ```bash
    git clone [https://github.com/votre_identifiant/projet-dev-mobile.git](https://github.com/votre_identifiant/projet-dev-mobile.git)
    ```
2.  **Ouvrir dans Android Studio :**
    Ouvrez le dossier du projet dans Android Studio.
3.  **Synchronisation Gradle :**
    Laissez Gradle se synchroniser pour télécharger toutes les dépendances (Room, Lifecycle, Material).
4.  **Exécution :**
    Exécutez l'application sur un émulateur ou un appareil physique (Android 13+ nécessite l'acceptation de la permission **POST\_NOTIFICATIONS**).

---

## 📧 Contact

Pour toute question ou information supplémentaire concernant ce projet, veuillez contacter :

* **Nom du développeur :** OUEDRAOGO Issa
* **Email :** iissa6345@gmail.com

***

*Ce projet a été réalisé en respectant les bonnes pratiques de développement Android et en s'appuyant sur l'architecture MVVM.*
