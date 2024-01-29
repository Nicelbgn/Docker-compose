# Image PostgreSQL comme base
FROM postgres

# Mise à jour et installation des composants nécessaires
RUN apt-get update && apt-get install -y postgresql postgresql-contrib

# Variables d'environnement pour la configuration
ENV POSTGRES_USER=postgres
ENV POSTGRES_PASSWORD=postgres
ENV POSTGRES_DB=postgres

# Exposition du port 5432
EXPOSE 5432

# Volume pour la persistance des données
VOLUME /var/lib/postgresql/data

# Commande pour démarrer le serveur PostgreSQL
CMD ["postgres", "-D", "/var/lib/postgresql/data"]