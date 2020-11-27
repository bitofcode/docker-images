FROM alpine:3
RUN apk add --no-cache bash git && \
  addgroup -S git-user && \
  adduser -S git-user -G git-user -s /bin/bash -h /home/git-user

USER git-user
WORKDIR /home/git-user

ENTRYPOINT ["/bin/bash"]
