# exo-maven-setup-done-docker

Default usernames and password:

* Normal user:

	username: exo
	password: password

* Administrative user:

	 username: admin
	 password: password

exo-maven-setup-done image have parent is exoplatform/exo-maven

* In tomcat/gatein/conf rename exo-sample.properties to exo.properties

	Set <strong>exo.accountsetup.skip</strong> value to <strong>true</strong> to skip Account Setup and Greeting Screen

* Start tomcat: first start creates DB schema and jcr 

* Stop tomcat 

This image saves a lot of time when you start the runner in codenvy.


## How to

* run the container


    docker run -d -p 8080:8080 --name=exo-maven-setup-done exoplatform/exo-maven-setup-done

* watch container logs


    docker logs --follow exo-maven-setup-done
