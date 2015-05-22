FROM mongo:latest

MAINTAINER mazzy <salvo.mazzarino@motorsquare.eu>

VOLUME ["/data/db", "/data/db/journal", "/log/mongodb"]

RUN sed -i "s|chown.*|chown -R mongodb:mongodb /data/db /data/db/journal /log/mongodb|g" /entrypoint.sh

ADD mongod.conf /etc/

EXPOSE 27017
EXPOSE 28017

ENTRYPOINT ["/entrypoint.sh"]
