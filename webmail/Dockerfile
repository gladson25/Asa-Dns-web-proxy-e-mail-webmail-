FROM debian:buster

RUN apt-get update \
    && apt-get install -y \
    apache2 apache2-utils libapache2-mod-php \
    php php-cli php-curl php-xml php-imap \
    nano 

RUN apt-get upgrade -y 

COPY email_1.sh .
COPY email_2.sh .
COPY 000-default.conf /etc/apache2/sites-availiable
RUN ./email_2.sh
RUN service apache2 start

CMD tail -F /dev/null
