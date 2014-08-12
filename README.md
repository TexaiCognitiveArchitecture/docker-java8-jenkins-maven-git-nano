docker-java8-jenkins-maven-git-nano
===================================

This repository provides the Dockerfile that builds a continuous integration container from Ubuntu 14.04 LTS, plus Oracle Java 8, Jenkins 1.574, Maven 3, Git and Nano.

Sets up a container with jenkins installed listening on port 8080.

Usage

To run the container with the same time zone as the host, do the following:

    sudo docker run -t -i -p 8080:8080 -v /etc/localtime:/etc/localtime:ro -P stephenreed/java8-jenkins-maven-git-nano

To start Jenkins from the container's command prompt . . .

    java -jar opt/jenkins.war

You can configure Jenkins continuous integration jobs at http://127.0.0.1:8080 .  The Jenkins GitHub plugin needs to be installed by you if you use GitHub.

More information on Jenkins state persistence can be found at https://registry.hub.docker.com/u/aespinosa/jenkins/ .
