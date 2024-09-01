# Verwende ein Python-Image als Basis
FROM python:3.10-slim

# Setze das Arbeitsverzeichnis im Container
WORKDIR /app

# Kopiere die requirements-Datei und installiere die Abhängigkeiten
COPY requirements.txt requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Kopiere den Rest des Codes
COPY . .

# Setze die Umgebungsvariablen
ENV PORT=5000
ENV MONGO_URL=<your_mongo_url>

# Exponiere den Port, auf dem die App läuft
EXPOSE 5000

# Starte den Server
CMD ["python", "index.py"]