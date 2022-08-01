FROM ubuntu
RUN apt-get update && apt-get -y install unzip default-jre curl
COPY pc2-9.8build-6259.develop.zip /tmp/pc2.zip
COPY startSystem / 
copy realm.properties /usr/local/pc2
RUN rm /usr/local/pc2 ; cd /usr/local && unzip /tmp/pc2.zip &&  ln -s pc2-9.8build pc2 && chmod a+x /usr/local/pc2/bin/*
RUN mkdir /pc2data  && touch /1strun && chmod a+x /startSystem
ENTRYPOINT ["/bin/bash", "-c" , "/startSystem $EXTRAS" ]
