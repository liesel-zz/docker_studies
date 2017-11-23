FROM openjdk:6-jdk
RUN mkdir /opt/vr
WORKDIR /opt/vr
RUN wget http://download.jboss.org/jbossas/7.1/jboss-as-7.1.1.Final/jboss-as-7.1.1.Final.zip
RUN unzip jboss-as-7.1.1.Final.zip
RUN mv jboss-as-7.1.1.Final jboss
WORKDIR /opt/vr/jboss/bin
# RUN ./standalone.sh
RUN mkdir /opt/vr/codigo
ADD ./codigo /opt/vr/codigo
RUN mv /opt/vr/jboss/standalone/configuration/standalone.xml /opt/vr/jboss/standalone/configuration/standalone.xml_original
ADD ./jboss-config/standalone.xml /opt/vr/jboss/standalone/configuration/standalone.xml