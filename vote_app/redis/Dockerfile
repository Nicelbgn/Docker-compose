# Image Debian comme base
FROM debian

# Mise à jour et installation de Redis
RUN apt-get update
RUN apt-get install -y redis

# Exposition du port 6379
EXPOSE 6379

# Commande pour démarrer le serveur Redis
CMD ["redis-server"]
