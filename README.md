# 📚 Bibliothèque de Citations

Application web développée avec **Symfony 7** permettant de constituer et gérer une bibliothèque de citations (CRUD complet) via une interface simple, moderne et intuitive.

> 🎓 **Cadre du projet** : Réalisé dans le cadre d'un cahier des charges académique.

---

## 🛠 Stack Technique

- **Backend** : PHP 8.2 / Symfony 7
- **ORM** : Doctrine
- **Moteur de templates** : Twig
- **Base de données** : MySQL 8.0
- **Environnement** : Docker Compose (`php-app`, `mysql`, `phpMyAdmin`, `MailDev`)

---

## 🗄 Modèle de Données (`Quote`)

| Champ | Type | Obligatoire | Description |
| :--- | :--- | :---: | :--- |
| `id` | `int` (Auto) | — | Identifiant unique |
| `title` | `string` | **Oui**\* | Texte de la citation |
| `author` | `string` | **Oui**\* | Auteur de la citation |
| `source` | `string` | **Non**\* | Source / origine de la citation |
| `addedAt` | `datetime` | **Oui** | Date d'ajout automatique |
| `category` | `string` | Non | Thème / catégorie |
| `language` | `string` | Non | Langue de la citation |
| `favorite` | `bool` | Non | Marqueur de favori |
| `rating` | `int` | Non | Note personnelle (ex: 1 à 5) |

> ⚠️ **Note technique** : Actuellement, `title` et `author` sont définis comme *nullable* et `source` est obligatoire dans l'entité. Un refactoring sera effectué avant la validation des formulaires afin d'être en conformité avec le cahier des charges (*texte et auteur obligatoires, source facultative*).

---

## ✨ Fonctionnalités

### 📌 Fonctionnalités obligatoires
- [x] Affichage de la bibliothèque (liste des citations)
- [ ] Gestion de l'état "Bibliothèque vide"
- [ ] Consultation d'une citation (vue dédiée)
- [ ] Ajout d'une citation via formulaire
- [ ] Validation des saisies
- [ ] Modification d'une citation
- [ ] Suppression d'une citation
- [ ] Confirmation / Modal de suppression
- [ ] Navigation fluide entre les pages

### 💡 Fonctionnalité créative (Obligatoire)
- [ ] *À définir*

### 🎁 Fonctionnalités bonus
- [ ] Tirage d'une citation aléatoire
- [ ] Recherche textuelle globale
- [ ] Filtrage par auteur et par catégorie
- [ ] Compteur total & statistiques par auteur
- [ ] Tri dynamique (par date, auteur, note)
- [ ] Système de mise en favoris
- [ ] Authentification utilisateur

---

## 🚀 Installation & Configuration

### Prérequis
- [Docker](https://www.docker.com/) & [Docker Compose](https://docs.docker.com/compose/) installés sur votre machine.

### Étapes d'installation

1. **Cloner le projet**
   ```bash
   git clone <url-du-repo>
   cd symphony_control
