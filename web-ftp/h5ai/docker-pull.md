---
description: h5ai New UI Authentication
---

# Docker pull

## Docker pull

docker pull fanvinga/docker-h5ai

```bash
docker run -d -p 8090:80 -v /srv/h5aiwebftp:/share --restart=always fanvinga/docker-h5ai
```

```bash
docker run -d -p 8090:80 -v /srv/h5aiwebftp:/share -e USER=aaaaaa -e PASSWD=aaaaaa --restart=always fanvinga/docker-h5ai:auth
```

