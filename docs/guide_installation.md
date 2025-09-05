Créer le projet site web dans Docker


a) Créer les fichiers
Dans le dossier site/ :
index.html :
<html>
  <h1>Bienvenue sur le site de Nathan 🚀</h1>
  <p>Mon premier projet avec Docker Desktop sur Windows.</p>
</html>

Dockerfile :
# Image NGINX officielle
FROM nginx:alpine

# Copier le site web dans NGINX
COPY index.html /usr/share/nginx/html/index.html

b) Construire l’image Docker
docker build -t mon-site-docker .

c) Lancer le site
docker run -d -p 8081:80 mon-site-docker

Accéder au site : http://localhost:8081

