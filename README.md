# CareerTrackr, suivi de candidatures

Projet d'équipe réalisé en 2e année du cycle ingénieur à 3IL. Application web qui aide un étudiant à
suivre ses candidatures de stage ou d'emploi et à gérer ses CV.

## Fonctionnalités

- **Suivi des candidatures** : entreprise, poste, date, état de la candidature.
- **Import depuis Gmail** : un script Python se connecte à la boîte mail en lecture seule (API Gmail,
  OAuth 2.0), repère les e-mails de candidature et en extrait l'entreprise et le poste avec la
  reconnaissance d'entités nommées de spaCy.
- **Gestion des CV** : dépôt, téléchargement et suppression de CV, stockés dans la base.
- **Connexion** avec un compte Google (OAuth 2.0).

## Technique

- Java, Spring Boot (Web, Data JPA, Security, OAuth2 Client), Thymeleaf
- PostgreSQL
- Python : API Gmail, spaCy

## Lancer le projet

Prérequis : Java 17, Maven, PostgreSQL.

```bash
export DB_PASSWORD=mot_de_passe_postgres   # et DB_USER si différent de postgres
cd demo
./mvnw spring-boot:run
```

L'application est disponible sur http://localhost:8080. Pour l'import Gmail, il faut créer des
identifiants OAuth dans la console Google Cloud et les placer à côté de `scriptMail.py`
(ils ne sont pas versionnés).

## Équipe

Projet réalisé à plusieurs ; l'historique des commits montre les contributions de chacun.
