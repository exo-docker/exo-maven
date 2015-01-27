FROM exoplatform/exo-maven
MAINTAINER Nam Phung <namph@exoplatform.com>

ENV TOMCAT_HOME /opt/exo/platform-community-4.1.0/

RUN cd TOMCAT_HOME/gatein/conf/ && \
	mv exo-sample.properties exo.properties && \
	sed -i 's/#exo.accountsetup.skip=false/exo.accountsetup.skip=true/g' exo.properties

# Create users

RUN cd TOMCAT_HOME/gatein/conf/ && \
	mkdir portal && cd portal && mkdir portal && \
	curl -L -o configuration.xml https://raw.githubusercontent.com/exo-docker/exo-maven/master/exo-maven-setup-done/configuration.xml

# Start eXo Platform Tomcat

RUN cd TOMCAT_HOME/ && \
	./start_eXo.sh

RUN ./stop_eXo.sh






