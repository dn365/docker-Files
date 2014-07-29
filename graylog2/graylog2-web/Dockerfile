FROM dn365/java:openjdk7

# install graylog2-web

RUN cd tmp && \
    wget https://github.com/Graylog2/graylog2-web-interface/releases/download/0.20.6/graylog2-web-interface-0.20.6.tgz && \
    tar zxvf graylog2-web-interface-0.20.6.tgz && \
    mv graylog2-web-interface-0.20.6 /graylog2-web && \
    rm -f graylog2-web-interface-0.20.6.tgz && \
    mkdir -p /data
    

# Define working directory.
WORKDIR /data


# Define default command.
#  -Dconfig.file=/opt/config/graylog2-web-interface.conf
# Log File
#  -Dlogger.file=/opt/config/graylog2-web-interface-log.xml
CMD ["/graylog2-web/bin/graylog2-web-interface"]

# Expose ports
#   - 9000 (http)
EXPOSE 9000




