FROM dn365/java:openjdk7

# Install ElasticSearch

RUN \
  cd /tmp && \
  wget https://download.elasticsearch.org/elasticsearch/elasticsearch/elasticsearch-0.90.10.tar.gz && \
  tar xvzf elasticsearch-0.90.10.tar.gz  && \
  rm -f elasticsearch-0.90.10.tar.gz z && \
  mv /tmp/elasticsearch-0.90.10 /elasticsearch && \
  mkdir -p /data

# Define working directory.
WORKDIR /data

# Define default command.
# -Des.config=/opt/config/elasticsearch.yml
# -f

CMD ["/elasticsearch/bin/elasticsearch"]

# Expose ports.
#   - 9200: HTTP
#   - 9300: transport
EXPOSE 9200
EXPOSE 9300