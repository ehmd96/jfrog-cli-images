# Récupération du CLI JFrog
FROM releases-docker.jfrog.io/jfrog/jfrog-cli-full-v2-jf:2.77.0 AS jfrog

# Récupération de l'image finale Node.js
FROM node:24.3.0-alpine

# Copie du binaire JFrog
COPY --from=jfrog --chmod=755 /usr/local/bin/jf /usr/local/bin/jf

ENTRYPOINT ["jf"]

CMD ["npm","--help"]