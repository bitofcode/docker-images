FROM alpine:3
RUN apk add --no-cache git && \
  addgroup -S git-user && \
  adduser -S git-user -G git-user -s /bin/sh -h /home/git-user

USER git-user
WORKDIR /home/git-user

ENTRYPOINT ["/bin/sh"]
