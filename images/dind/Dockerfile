FROM docker:28.2.2-dind-alpine3.22

RUN apk add --no-cache ca-certificates

# cleanup warning: https://github.com/docker-library/docker/issues/55
RUN addgroup -g 2999 docker

COPY preentry.sh /usr/local/bin/

ENTRYPOINT ["preentry.sh"]

# USAGE: Add a CMD to your own Dockerfile to use this (NOT an ENTRYPOINT), eg:
# CMD ["./runner"]
