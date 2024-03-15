# pocketbase-image

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

