# docker-svelte-kit

Docker container with Svelte-Kit

## Supported tags and respective <code>Dockerfile</code> links

* [<code>js-adapter-node</code>, <code>latest</code>](https://github.com/asknotbad/docker-svelte-kit/blob/main/docker/Dockerfile)
* [<code>js-adapter-node-alpine</code>, <code>latest-alpine</code>, <code>alpine</code>](https://github.com/asknotbad/docker-svelte-kit/blob/main/docker/Dockerfile.alpine)
* [<code>js-adapter-node-dev</code>, <code>latest-dev</code>, <code>dev</code>](https://github.com/asknotbad/docker-svelte-kit/blob/main/docker/Dockerfile.dev)
* [<code>js-adapter-node-dev-alpine</code>, <code>latest-dev-alpine</code>, <code>dev-alpine</code>](https://github.com/asknotbad/docker-svelte-kit/blob/main/docker/Dockerfile.dev.alpine)

## docker-compose.yml

```yaml
version: '3.8'

services:
  svelte-kit:
    container_name: svelte-kit
    restart: always
    build:
      context: ./docker
    volumes:
      - ./docker/js/adapter-node/:/app
      - /app/node_modules
    ports:
      - 3000:3000
```

## docker-compose.dev.yml

```yaml
version: '3.8'

services:
  svelte-kit:
    container_name: svelte-kit-dev
    dockerfile: Dockerfile.dev
    restart: always
    build:
      context: ./docker
    volumes:
      - ./docker/js/adapter-node/:/app
      - /app/node_modules
    ports:
      - 3000:3000
      - 24678:24678
```

## Support

[Bugs](https://github.com/asknotbad/docker-svelte-kit/issues)

## Stay in touch

- Author: [Den Kochetkov](https://github.com/dkochetkov)
- E-mail: <d@asknotbad.com>
- Website: [asknotbad.com](https://asknotbad.com/)

## License

[Apache-2.0](LICENSE)

Copyright &copy; 2021 <a href="https://asknotbad.com" target="_blank">Not Bad</a>
