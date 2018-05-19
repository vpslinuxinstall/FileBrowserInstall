---
description: h5ai
---

# Docker pull

### Docker hub

docker pull clue/h5ai

```bash
docker run -it --rm -p 8090:80 -v /srv/h5aiwebftp:/var/www clue/h5ai     
```

```bash
docker run -d --rm -p 8090:80 -v /srv/h5aiwebftp:/var/www clue/h5ai
```

```bash
chmod 777 /srv/h5aiwebftp
```

folder /var/lib/docker/volumes

