FROM debian:jessie

RUN apt-get update && apt-get install -y \
        mailutils \
        ssmtp \
    && apt-get clean

COPY ssmtp_custom.conf /etc/ssmtp/ssmtp_custom.conf
COPY entrypoint.sh /usr/local/bin/
ENTRYPOINT ["sh","/usr/local/bin/entrypoint.sh"]
