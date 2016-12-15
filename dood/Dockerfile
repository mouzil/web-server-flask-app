FROM jenkins:1.596

USER root

RUN apt-get update \
      && apt-get install -y sudo \
      && rm -rf /var/lib/apt/lists/*
RUN echo "jenkins ALL=NOPASSWD: ALL" >> /etc/sudoers

USER jenkins
COPY plugins.txt /usr/share/jenkins/plugins.txt
RUN /usr/local/bin/plugins.sh /usr/share/jenkins/plugins.txt

#cat plugins.txt

# Mettre ces lignes dans un fichier plugin
#scm-api:latest
#git-client:latest
#git:latest
#greenballs:latest

# exécuter cette commande dans terminal
#$ docker build -t myjenk .
#Successfully built 471fc0d22bff

#Exécuter cette commande dans terminal
#$ docker run -d -v /var/run/docker.sock:/var/run/docker.sock \-v $(which docker):/usr/bin/docker -p 8080:8080 myjenk