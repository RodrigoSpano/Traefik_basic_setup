- create docker network => ``docker network create traefik``

- to enable traefik in any other container >
  1. Use the same network (traefik)
  2. Add traefik labels > for example
  ```
  labels:
      - "traefik.enable=true"
      - "traefik.http.routers.nginx.rule=Host(`nginx.(your.domain)`)"
      - "traefik.http.routers.nginx.entrypoints=web"
  ```