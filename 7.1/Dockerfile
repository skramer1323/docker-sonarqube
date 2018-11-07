FROM sonarqube:latest
ENV SONARQUBE_JDBC_USERNAME=$JDBC_USERNAME \
    SONARQUBE_JDBC_PASSWORD=$JDBC_PASSWORD \
    SONARQUBE_JDBC_URL=$JDBC_URL

USER root
ADD run.sh /opt/sonarqube/bin/run.sh
CMD /opt/sonarqube/bin/run.sh
RUN chown root:root /opt/sonarqube -R; \
    chmod 6775 /opt/sonarqube -R
USER 1001
