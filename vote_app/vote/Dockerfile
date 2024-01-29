# Image Python comme base
FROM python:3.11

WORKDIR /app

# Copie de l'application et installation des dépendances
COPY . /app 
RUN pip3 install -r requirements.txt --break-system-packages

# Exposition du port 5000
EXPOSE 5000

# Variables d'environnement pour l'application
ENV OPTION_A=CATS
ENV OPTION_B=DOGS

# Commande pour démarrer l'application
CMD ["python", "app.py"]
