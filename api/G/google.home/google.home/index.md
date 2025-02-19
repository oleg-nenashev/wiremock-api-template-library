---
slug: "google-home"
title: "Google Home"
provider: "google.home"
description: "# Google Home Local API\nThis is an unofficial documentation of the\
  \ local API used by the Home app to communicate with GH devices.\n[GitHub Repo](https://github.com/rithvikvibhu/GHLocalApi)\n\
  \n[![GitHub stars](https://img.shields.io/github/stars/rithvikvibhu/GHLocalApi)](https://github.com/rithvikvibhu/GHLocalApi/stargazers)\
  \ [![GitHub license](https://img.shields.io/github/license/rithvikvibhu/GHLocalApi)](https://github.com/rithvikvibhu/GHLocalApi/blob/master/LICENSE.md)\n\
  \n## Getting Started\n\nRequests must be made over HTTPS, port 8443, so the base\
  \ URL for these endpoints is: `https://<google-home-ip>:8443/setup/`\n\nGet the\
  \ IP of Google Home from the Google Home app (Device Settings -> End of the list)\
  \ or from your router.\n\nGET requests are simple, in the browser kind.  \nPOST\
  \ requests need to set the header (when there's a body): `content-type: application/json`\n\
  \n## Authentication\n\nSince June 2019, most requests (with exceptions like `/setup/eureka_info`)\
  \ need a local authorization token.\n\nThere are 3 kinds of tokens involved here:\n\
  \n### Local Authorization Token\nThis token must be sent in all requests in the\
  \ header `cast-local-authorization-token`. It is short-lived (~1 day) and may change\
  \ unexpectedly (with a sync, change in homegraph, etc.)\n##### Get this token\n\
  - With access to an android device, [get this token directly by either method](https://gist.github.com/rithvikvibhu/1a0f4937af957ef6a78453e3be482c1f).\n\
  - Without a device, or to integrate it with a script, use an access token to get\
  \ the homegraph and extract the token. To get an access token, read the next section.\
  \ Check the example section for more info.\n\n### Access Token\nThis is a standard\
  \ google oauth2 access token. It is in the form `ya29.***`.\nThis gives access to\
  \ the Google Home Foyer API. These expire in an hour.\nUse this to get the homegraph\
  \ (and then the local authorization token above).\n##### Get this token\nTo get\
  \ this access token, either a Google account username/password or a Google Master\
  \ Token is needed. More info in the gist.\nUse the script [from this gist](https://gist.github.com/rithvikvibhu/952f83ea656c6782fbd0f1645059055d).\n\
  \n### Master Token\nThis is in the form `aas_et/***` and can be used to request\
  \ access tokens.\n##### Get this token\nThe same [script in the gist](https://gist.github.com/rithvikvibhu/952f83ea656c6782fbd0f1645059055d)\
  \ that gets the access token can also get the master token. Needs Google account\
  \ creds.\n\n## Example\n\nHere's the whole flow from just a pair of username/password\
  \ to using the local API.\n\nPrerequisites:\n- [grpcurl](https://github.com/fullstorydev/grpcurl)\n\
  - [Proto files](https://drive.google.com/drive/folders/1RvnN3y-G23pd2SWHmfV_7sef8QU5GNF4?usp=sharing)\
  \ (preserve folder structure)\n\n### 1. Get an access token with the script\n- Download\
  \ get_tokens.py\n- Fill in username and password\n```sh\npython3 get_tokens.py\n\
  # Note down the access token printed.\n```\n\n### 2. Use the access token and get\
  \ home graph\n- This prints the json and uses jq to parse and filter out the fields\
  \ deviceName and localAuthToken\n- This will give a list of all devices and their\
  \ local auth tokens\n```sh\n./grpcurl -H 'authorization: Bearer ya29.a0Af****' \\\
  \n\t-import-path /path/to/protos \\\n\t-proto /path/to/protos/google/internal/home/foyer/v1.proto\
  \ \\\n\tgooglehomefoyer-pa.googleapis.com:443 \\\n\tgoogle.internal.home.foyer.v1.StructuresService/GetHomeGraph\
  \ | jq '.home.devices[] | {deviceName, localAuthToken}'\n# Note down the local auth\
  \ token for the device you want.\n```\n\n### 3. Make the call to the local device\
  \ using the local auth token\n```sh\ncurl -H \"cast-local-authorization-token: LOCAL_AUTH_TOKEN\"\
  \ --verbose --insecure https://192.168.0.18:8443/setup/bluetooth/status\n```"
logo: "google.home-logo.svg"
logoMediaType: "image/svg+xml"
tags: []
stubs: "google.home-stubs.json"
swagger: "google.home-swagger.json"
---
