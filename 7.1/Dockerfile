FROM sonarqube:latest

ENV SONAR_VERSION=7.1 \
    SONARQUBE_HOME=/opt/sonarqube \
    # Database configuration
    # Defaults to using H2
    SONARQUBE_JDBC_USERNAME=$JDBC_USERNAME \
    SONARQUBE_JDBC_PASSWORD=$JDBC_PASSWORD \
    SONARQUBE_JDBC_URL=$JDBC_URL

USER root

RUN chgrp -R 0 /opt \
 && chmod -R g+rwX /opt

RUN chown root:root /opt/sonarqube -R; \
    chmod 6775 /opt/sonarqube -R
    
ADD run.sh /opt/sonarqube/bin/run.sh

CMD /opt/sonarqube/bin/run.sh
  
USER 1001
