# Giveth Redis
Our own redis setup, with special configs that are able to support our backend application usage case. With specific extra configurations `redis.conf`

## Usage
You can find the docker-compose configuration snippet example here:
```
# REDIS
  redis-all:
    image: ghcr.io/giveth/giveth-redis:latest
    container_name: redis-all
    networks:
      - giveth
    environment:
      - REDIS_ALLOW_EMPTY_PASSWORD=yes
    restart: always
    volumes:
      - redis-data:/data
```
