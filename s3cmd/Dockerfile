FROM debian:stretch-slim
LABEL maintainer "Giacomo Longo <gabibbo97@gmail.com>"

RUN apt-get update && apt-get install --no-install-recommends -y \
  ca-certificates \
  s3cmd \
  && rm -rf /var/lib/apt/lists/*

ENTRYPOINT [ "s3cmd" ]