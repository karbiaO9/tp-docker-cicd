# Image de base : Node.js 18 sur Alpine Linux (légère)
FROM node:18-alpine

# Répertoire de travail dans le conteneur
WORKDIR /app

# Optimisation du cache Docker : copier d’abord les dépendances
COPY package*.json ./
RUN npm install --production

# Copier le reste du code source
COPY . .

# Exposer le port sur lequel tourne l’application
EXPOSE 3000

# Commande de démarrage par défaut
CMD ["npm", "start"]
