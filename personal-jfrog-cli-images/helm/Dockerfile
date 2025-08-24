# Récupération du CLI JFrog
FROM releases-docker.jfrog.io/jfrog/jfrog-cli-full-v2-jf:2.77.0 AS jfrog

# Récupération de Helm
FROM alpine/helm:3.14.4

# Copie du binaire JFrog
COPY --from=jfrog /usr/local/bin/jf /usr/local/bin/jf

# Permissions
RUN chmod +x /usr/local/bin/jf

# Vérifications
RUN helm version && jf --version

# Entrypoint par défaut
ENTRYPOINT ["/bin/sh"]