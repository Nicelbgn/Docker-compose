# Image Debian comme base
FROM debian:12

# Mise à jour et installation de Node.js et npm
RUN apt-get update 
RUN apt-get install -y nodejs npm

# Exposition du port 4000
EXPOSE 4000

WORKDIR /app/results

# Copie de l'application et installation des dépendances
COPY . . 
RUN npm install

# Commande pour démarrer le serveur Node.js
CMD ["node", "server.js"]
