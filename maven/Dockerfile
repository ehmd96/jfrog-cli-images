FROM releases-docker.jfrog.io/jfrog/jfrog-cli-full-v2-jf:2.77.0 AS jfrog

FROM maven:3.9.9-eclipse-temurin-21-alpine

COPY --from=jfrog --chmod=755 /usr/local/bin/jf /usr/local/bin/jf

ENTRYPOINT ["jf"]

CMD ["mvn","--help"]
