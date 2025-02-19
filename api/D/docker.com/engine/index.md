---
slug: "docker-com-engine"
title: "Docker Engine API"
provider: "docker.com"
description: "The Engine API is an HTTP API served by Docker Engine. It is the API\
  \ the Docker client uses to communicate with the Engine, so everything the Docker\
  \ client can do can be done with the API.\n\nMost of the client's commands map directly\
  \ to API endpoints (e.g. `docker ps` is `GET /containers/json`). The notable exception\
  \ is running containers, which consists of several API calls.\n\n# Errors\n\nThe\
  \ API uses standard HTTP status codes to indicate the success or failure of the\
  \ API call. The body of the response will be JSON in the following format:\n\n```\n\
  {\n  \"message\": \"page not found\"\n}\n```\n\n# Versioning\n\nThe API is usually\
  \ changed in each release of Docker, so API calls are versioned to ensure that clients\
  \ don't break.\n\nFor Docker Engine 17.09, the API version is 1.32. To lock to this\
  \ version, you prefix the URL with `/v1.32`. For example, calling `/info` is the\
  \ same as calling `/v1.32/info`.\n\nEngine releases in the near future should support\
  \ this version of the API, so your client will continue to work even if it is talking\
  \ to a newer Engine.\n\nIn previous versions of Docker, it was possible to access\
  \ the API without providing a version. This behaviour is now deprecated will be\
  \ removed in a future version of Docker.\n\nThe API uses an open schema model, which\
  \ means server may add extra properties to responses. Likewise, the server will\
  \ ignore any extra query parameters and request body properties. When you write\
  \ clients, you need to ignore additional properties in responses to ensure they\
  \ do not break when talking to newer Docker daemons.\n\nThis documentation is for\
  \ version 1.33 of the API. Use this table to find documentation for previous versions\
  \ of the API:\n\nDocker version  | API version | Changes\n----------------|-------------|---------\n\
  17.09.x | [1.31](https://docs.docker.com/engine/api/v1.32/) | [API changes](https://docs.docker.com/engine/api/version-history/#v1-32-api-changes)\n\
  17.07.x | [1.31](https://docs.docker.com/engine/api/v1.31/) | [API changes](https://docs.docker.com/engine/api/version-history/#v1-31-api-changes)\n\
  17.06.x | [1.30](https://docs.docker.com/engine/api/v1.30/) | [API changes](https://docs.docker.com/engine/api/version-history/#v1-30-api-changes)\n\
  17.05.x | [1.29](https://docs.docker.com/engine/api/v1.29/) | [API changes](https://docs.docker.com/engine/api/version-history/#v1-29-api-changes)\n\
  17.04.x | [1.28](https://docs.docker.com/engine/api/v1.28/) | [API changes](https://docs.docker.com/engine/api/version-history/#v1-28-api-changes)\n\
  17.03.1 | [1.27](https://docs.docker.com/engine/api/v1.27/) | [API changes](https://docs.docker.com/engine/api/version-history/#v1-27-api-changes)\n\
  1.13.1 & 17.03.0 | [1.26](https://docs.docker.com/engine/api/v1.26/) | [API changes](https://docs.docker.com/engine/api/version-history/#v1-26-api-changes)\n\
  1.13.0 | [1.25](https://docs.docker.com/engine/api/v1.25/) | [API changes](https://docs.docker.com/engine/api/version-history/#v1-25-api-changes)\n\
  1.12.x | [1.24](https://docs.docker.com/engine/api/v1.24/) | [API changes](https://docs.docker.com/engine/api/version-history/#v1-24-api-changes)\n\
  1.11.x | [1.23](https://docs.docker.com/engine/api/v1.23/) | [API changes](https://docs.docker.com/engine/api/version-history/#v1-23-api-changes)\n\
  1.10.x | [1.22](https://docs.docker.com/engine/api/v1.22/) | [API changes](https://docs.docker.com/engine/api/version-history/#v1-22-api-changes)\n\
  1.9.x | [1.21](https://docs.docker.com/engine/api/v1.21/) | [API changes](https://docs.docker.com/engine/api/version-history/#v1-21-api-changes)\n\
  1.8.x | [1.20](https://docs.docker.com/engine/api/v1.20/) | [API changes](https://docs.docker.com/engine/api/version-history/#v1-20-api-changes)\n\
  1.7.x | [1.19](https://docs.docker.com/engine/api/v1.19/) | [API changes](https://docs.docker.com/engine/api/version-history/#v1-19-api-changes)\n\
  1.6.x | [1.18](https://docs.docker.com/engine/api/v1.18/) | [API changes](https://docs.docker.com/engine/api/version-history/#v1-18-api-changes)\n\
  \n# Authentication\n\nAuthentication for registries is handled client side. The\
  \ client has to send authentication details to various endpoints that need to communicate\
  \ with registries, such as `POST /images/(name)/push`. These are sent as `X-Registry-Auth`\
  \ header as a Base64 encoded (JSON) string with the following structure:\n\n```\n\
  {\n  \"username\": \"string\",\n  \"password\": \"string\",\n  \"email\": \"string\"\
  ,\n  \"serveraddress\": \"string\"\n}\n```\n\nThe `serveraddress` is a domain/IP\
  \ without a protocol. Throughout this structure, double quotes are required.\n\n\
  If you have already got an identity token from the [`/auth` endpoint](#operation/SystemAuth),\
  \ you can just pass this instead of credentials:\n\n```\n{\n  \"identitytoken\"\
  : \"9cbaf023786cd7...\"\n}\n```\n"
logo: "docker.com-engine-logo.png"
logoMediaType: "image/png"
tags:
- "developer_tools"
stubs: "docker.com-engine-stubs.json"
swagger: "docker.com-engine-swagger.json"
---
