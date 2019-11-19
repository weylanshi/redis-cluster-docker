FROM redis

COPY redis.conf /usr/local/etc/redis/redis.conf

RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo 'Asia/Shanghai' >/etc/timezone && \
    chmod 777 /usr/local/etc/redis/redis.conf 

EXPOSE 6371 

EXPOSE 16371 

CMD [ "redis-server", "/usr/local/etc/redis/redis.conf" ]