# Récupération du CLI JFrog
FROM releases-docker.jfrog.io/jfrog/jfrog-cli-full-v2-jf:2.77.0 AS jfrog

# Récupération de l'image finale Node.js
FROM node:24.3.0-alpine

# Copie du binaire JFrog
COPY --from=jfrog /usr/local/bin/jf /usr/local/bin/jf

# Permissions
RUN chmod +x /usr/local/bin/jf

# Vérifications
RUN jf --version && jf npm --help

# Entrypoint par défaut
ENTRYPOINT ["/bin/sh"]