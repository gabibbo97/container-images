FROM debian:stretch-slim
LABEL maintainer "Giacomo Longo <gabibbo97@gmail.com>"

RUN apt-get update && apt-get install -y \
  asterisk \
  asterisk-core-sounds-en \
  asterisk-core-sounds-es \
  asterisk-core-sounds-fr \
  asterisk-core-sounds-it \
  asterisk-dahdi \
  asterisk-espeak \
  asterisk-flite \
  asterisk-moh-opsound-wav \
  asterisk-mp3 \
  asterisk-opus \
  asterisk-voicemail-imapstorage \
  asterisk-voicemail-odbcstorage \
  odbc-postgresql \
  && rm -rf /var/lib/apt/lists/*

ENTRYPOINT [ "asterisk", "-f" ]