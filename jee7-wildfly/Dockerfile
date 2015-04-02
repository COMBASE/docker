#JEE7 Plattform mit Wildfly

FROM combase/java8
MAINTAINER lm "lm@combase.de"

#wildfly nach /opt speichern und entpacken
RUN cd /opt && wget http://download.jboss.org/wildfly/8.2.0.Final/wildfly-8.2.0.Final.tar.gz \
&& gunzip wildfly-8.2.0.Final.tar.gz \
&& tar xf wildfly-8.2.0.Final.tar \
&& rm -f wildfly-8.2.0.Final.tar

#wildfly user und group anlegen
RUN addgroup -g 433 wildfly\
&& adduser -u 431 -S -g wildfly -h /opt/wildfly-8.1.0.Final -s /sbin/nologin wildfly

# Change the owner of the /opt/wildfly directory
RUN chown -R wildfly:wildfly /opt/wildfly-8.2.0.Final
RUN /opt/wildfly-8.2.0.Final/bin/add-user.sh --silent admin admin

#webapp und admin port nach aussen legen
EXPOSE 8080 9990

CMD ["/opt/wildfly-8.2.0.Final/bin/standalone.sh", "-b", "0.0.0.0", "-bmanagement", "0.0.0.0"]
