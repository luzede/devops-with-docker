FROM ubuntu:22.04


COPY script.sh .

RUN apt-get update
RUN apt-get -y install curl

RUN chmod +x script.sh

CMD ./script.sh