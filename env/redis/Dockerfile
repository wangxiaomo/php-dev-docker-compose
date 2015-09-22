FROM redis:3

ADD redis.conf /etc/redis/redis.conf
WORKDIR /data
ENTRYPOINT ["redis-server", "/etc/redis/redis.conf"]
