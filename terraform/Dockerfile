# Récupération du CLI JFrog
FROM releases-docker.jfrog.io/jfrog/jfrog-cli-full-v2-jf:2.77.0 AS jfrog

# Image finale basée sur Akamai Terraform
FROM hashicorp/terraform:1.12.2

# Copie du binaire JFrog
COPY --from=jfrog --chmod=755 /usr/local/bin/jf /usr/local/bin/jf

ENTRYPOINT ["jf"]

CMD ["terraform","--help"]
