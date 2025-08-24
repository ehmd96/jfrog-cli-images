# Récupération du CLI JFrog
FROM releases-docker.jfrog.io/jfrog/jfrog-cli-full-v2-jf:2.77.0 AS jfrog

# Image finale basée sur Akamai Terraform
FROM hashicorp/terraform:1.12.2

# Copie du binaire JFrog
COPY --from=jfrog /usr/local/bin/jf /usr/local/bin/jf

# Permissions
RUN chmod +x /usr/local/bin/jf

# Vérifications
RUN jf --version && terraform version && jf terraform --help

# Entrypoint par défaut
ENTRYPOINT ["/bin/sh"]
