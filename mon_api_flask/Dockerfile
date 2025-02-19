# Utiliser une image officielle de Python
FROM python:3.9-slim

# Définir un répertoire de travail dans le conteneur
WORKDIR /app


RUN mkdir -p /app/data

# Copier le fichier requirements.txt dans le conteneur
COPY requirements.txt /app/

# Installer les dépendances
RUN pip install --no-cache-dir -r requirements.txt

# Copier tout le code de l’application dans le conteneur
COPY app.py /app

# Exposer le port 5000 pour l’application Flask
EXPOSE 5000

# Lancer l’application Flask
CMD ["python", "app.py"]
