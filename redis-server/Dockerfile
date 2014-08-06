FROM ubuntu:12.04


RUN apt-get clean
RUN apt-get update
RUN apt-get install -y wget make gcc

# Install redis-server

RUN \
  cd /tmp && \
  wget http://download.redis.io/redis-stable.tar.gz && \
  tar xvzf redis-stable.tar.gz && \
  rm -f redis-stable.tar.gz && \
  cd /tmp/redis-stable && \
  make && \
  make install && \
  mv /tmp/redis-stable /redis && \
  mkdir -p /data

# Define working directory.
WORKDIR /data

# Define default command.
# /opt/config/redis.conf
CMD ["/redis/src/redis-server"]

# Expose ports.
#   - 6379: TCP server
EXPOSE 6379