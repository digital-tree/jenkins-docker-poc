FROM jenkins/jenkins:lts

USER root
RUN usermod -aG users jenkins

USER jenkins

COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt

COPY init-groovy/* /var/jenkins_home/init.groovy.d/

COPY seedjobDefinition.groovy /var/jenkins_home/
