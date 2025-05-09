# Utiliser une version spécifique de NGINX pour éviter les vulnérabilités
FROM nginx:stable-alpine

# Copier le répertoire front-end dans le conteneur
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copier le fichier de configuration NGINX
COPY softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Exposer le port 9000
EXPOSE 9000

# Lancer NGINX avec le conteneur
CMD ["nginx", "-g", "daemon off;"]