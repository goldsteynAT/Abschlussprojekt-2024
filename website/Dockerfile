# Verwende ein Node-Image als Basis
FROM node:18-alpine

# Setze das Arbeitsverzeichnis im Container
WORKDIR /app

# Kopiere package.json und package-lock.json und installiere die Abhängigkeiten
COPY package*.json ./
RUN npm install

# Kopiere den Rest des Codes
COPY . .

# Exponiere den Port, auf dem die App läuft
EXPOSE 3000

# Baue die App für die Produktion
RUN npm run build

# Starte den Server
CMD ["npm", "start"]
