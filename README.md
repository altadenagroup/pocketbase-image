# pocketbase-image
dockerized pocketbeam image, published on ghcr for easier management

## Docker Compose Example

```yml
version: '3.9'

services:
  pb:
    container_name: pocketbase
    image: ghcr.io/altadenagroup/pocketbase-image:main
    restart: unless-stopped
    volumes:
      - pocketbase-volume:/app/data
    ports:
      - '8090:8090'
    
volumes:
  pocketbase-volume:
    name: pocketbase-volume
```

Note: if you are using a dockerized reverse proxy, you don't have to publish any ports. Just use the URL `http://<container name>:8090`.
