FROM dn365/java:openjdk7

# install logstash

RUN cd tmp && \
    wget https://download.elasticsearch.org/logstash/logstash/logstash-1.4.2.tar.gz && \
    tar zxvf logstash-1.4.2.tar.gz && \
    mv logstash-1.4.2 /logstash && \
    rm -f logstash-1.4.2.tar.gz && \
    mkdir -p /data
    

# Define working directory.
WORKDIR /data

# Define default command.
# --config /opt/config
# -l /data/logstash.log
CMD ["/logstash/bin/logstash"]

# Expose ports




