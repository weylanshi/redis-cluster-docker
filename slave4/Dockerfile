FROM redis

COPY redis.conf /usr/local/etc/redis/redis.conf

RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo 'Asia/Shanghai' >/etc/timezone && \
    chmod 777 /usr/local/etc/redis/redis.conf 

EXPOSE 6374 

EXPOSE 16374

CMD [ "redis-server", "/usr/local/etc/redis/redis.conf" ]