FROM releases-docker.jfrog.io/jfrog/jfrog-cli-full-v2-jf:2.77.0 AS jfrog

FROM maven:3.9.9-eclipse-temurin-21-alpine

COPY --from=jfrog /usr/local/bin/jf /usr/local/bin/jf

# Permissions pour JFrog CLI
RUN chmod +x /usr/local/bin/jf

# Vérifications
RUN jf --version && jf mvn --help

# Entrypoint par défaut
ENTRYPOINT ["/bin/sh"]