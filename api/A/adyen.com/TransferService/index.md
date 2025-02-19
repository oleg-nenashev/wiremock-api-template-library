---
slug: "adyen-com-TransferService"
title: "Transfers API"
provider: "adyen.com"
description: "The Transfers API provides endpoints that you can use to get information\
  \ about all your transactions, move funds within your balance platform or send funds\
  \ from your balance platform to a [transfer instrument](https://docs.adyen.com/api-explorer/#/legalentity/latest/post/transferInstruments).\n\
  \n## Authentication\nYour Adyen contact will provide your API credential and an\
  \ API key. To connect to the API, add an `X-API-Key` header with the API key as\
  \ the value, for example:\n\n ```\ncurl\n-H \"Content-Type: application/json\" \\\
  \n-H \"X-API-Key: YOUR_API_KEY\" \\\n...\n```\n\nAlternatively, you can use the\
  \ username and password to connect to the API using basic authentication. For example:\n\
  \n```\ncurl\n-H \"Content-Type: application/json\" \\\n-U \"ws@BalancePlatform.YOUR_BALANCE_PLATFORM\"\
  :\"YOUR_WS_PASSWORD\" \\\n...\n```\n## Roles and permissions\nTo use the Transfers\
  \ API, you need an additional role for your API credential. Transfers must also\
  \ be enabled for the source balance account. Your Adyen contact will set up the\
  \ roles and permissions for you.\n## Versioning\nThe Transfers API supports [versioning](https://docs.adyen.com/development-resources/versioning)\
  \ using a version suffix in the endpoint URL. This suffix has the following format:\
  \ \"vXX\", where XX is the version number.\n\nFor example:\n```\nhttps://balanceplatform-api-test.adyen.com/btl/v3/transfers\n\
  ```\n## Going live\nWhen going live, your Adyen contact will provide your API credential\
  \ for the live environment. You can then use the username and password to send requests\
  \ to `https://balanceplatform-api-live.adyen.com/btl/v3`.\n\n"
logo: "adyen.com-TransferService-logo.svg"
logoMediaType: "image/svg+xml"
tags:
- "payment"
stubs: "adyen.com-TransferService-stubs.json"
swagger: "adyen.com-TransferService-swagger.json"
---
