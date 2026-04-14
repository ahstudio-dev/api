# AHStudio — API

> API REST au cœur des services AHStudio, construite avec Java & Spring Boot.

## Stack technique

- **Java 21**
- **Spring Boot 3**
- **Spring Security** — authentification JWT
- **Spring Data JPA** — accès base de données
- **PostgreSQL** — base de données principale
- **Docker** — containerisation

## Démarrage rapide

### Prérequis

- Java 21+
- Maven 3.9+
- Docker & Docker Compose
- PostgreSQL 15+

### Lancer en local

```bash
# Cloner le repo
git clone https://github.com/ahstudio-dev/api.git
cd api

# Démarrer la base de données
docker compose up -d

# Lancer l'application
./mvnw spring-boot:run
```

L'API sera disponible sur `http://localhost:8080`

## Structure du projet

```
src/
├── main/
│   ├── java/dev/ahstudio/api/
│   │   ├── config/        # Sécurité, CORS, beans
│   │   ├── controller/    # Contrôleurs REST
│   │   ├── service/       # Logique métier
│   │   ├── repository/    # Accès base de données
│   │   ├── model/         # Entités
│   │   └── dto/           # Objets de transfert de données
│   └── resources/
│       └── application.yml
└── test/
```

## Stratégie de branches

| Branche | Rôle |
|---------|------|
| `main` | Production — versions stables uniquement |
| `develop` | Branche d'intégration |
| `feat/*` | Nouvelles fonctionnalités |
| `fix/*` | Corrections de bugs |

## Convention de commits

```
feat: ajout de l'authentification utilisateur
fix: correction de l'expiration du JWT
docs: mise à jour de la documentation API
refactor: nettoyage de la couche service
```

## Licence

Privé — © 2025 AHStudio. Tous droits réservés.
