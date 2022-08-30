# servidor SMTP no Debian

FROM debian:buster

RUN apt update
RUN apt upgrade -y 

RUN apt install postfix -y
RUN apt install telnet -y

COPY main.cf /etc/postfix

EXPOSE 25

CMD [ "postfix", "start-fg" ]
