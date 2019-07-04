FROM debian:stretch-slim AS download-tika
ENV TIKA_VERSION=1.21
RUN apt-get update && apt-get install -y wget
RUN wget -O /opt/tika.jar http://it.apache.contactlab.it/tika/tika-server-${TIKA_VERSION}.jar
# Application
FROM debian:stretch
LABEL maintainer "Giacomo Longo <gabibbo97@gmail.com>"

COPY --from=download-tika /opt/tika.jar /opt

RUN apt-get update && apt-get install -y \
  default-jre-headless \
  tesseract-ocr-all \
  && rm -rf /var/lib/apt/lists/*

ENTRYPOINT [ "java", "-jar", "/opt/tika.jar", \
  "--host", "0.0.0.0", \
  "--port", "9998" \
  ]