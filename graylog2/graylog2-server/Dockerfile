FROM dn365/java:openjdk7

# install graylog2-server

RUN cd tmp && \
    wget https://github.com/Graylog2/graylog2-server/releases/download/0.20.4/graylog2-server-0.20.4.tgz && \
    tar zxvf graylog2-server-0.20.4.tgz && \
    mv graylog2-server-0.20.4 /graylog2-server && \
    rm -f graylog2-server-0.20.4.tgz && \
    mkdir -p /data && \

# Define working directory.
WORKDIR /data

# Define default command.
# -f /opt/config/graylog2.conf
# log file
# java -Dlog4j.configuration=file:///opt/config/logj4.xml -jar /graylog2-server/graylog2-server.jar

CMD ["java -jar /graylog2-server/graylog2-server.jar"]

# Expose ports
#   - 12201: GELF (UDP & TCP)
#   - 12900: REST API
EXPOSE 12201 12201/udp 12900


