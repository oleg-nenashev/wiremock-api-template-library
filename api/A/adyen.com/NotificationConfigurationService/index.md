---
slug: "adyen-com-NotificationConfigurationService"
title: "Notification Configuration API"
provider: "adyen.com"
description: "This API is used for the classic integration. If you are just starting\
  \ your implementation, refer to our [new integration guide](https://docs.adyen.com/marketplaces-and-platforms)\
  \ instead.\n\nThe Notification Configuration API provides endpoints for setting\
  \ up and testing notifications that inform you of events on your platform, for example\
  \ when a verification check or a payout has been completed.\n\nFor more information,\
  \ refer to our [documentation](https://docs.adyen.com/marketplaces-and-platforms/classic/notifications).\n\
  ## Authentication\nYour Adyen contact will provide your API credential and an API\
  \ key. To connect to the API, add an `X-API-Key` header with the API key as the\
  \ value, for example:\n\n ```\ncurl\n-H \"Content-Type: application/json\" \\\n\
  -H \"X-API-Key: YOUR_API_KEY\" \\\n...\n```\n\nAlternatively, you can use the username\
  \ and password to connect to the API using basic authentication. For example:\n\n\
  ```\ncurl\n-U \"ws@MarketPlace.YOUR_PLATFORM_ACCOUNT\":\"YOUR_WS_PASSWORD\" \\\n\
  -H \"Content-Type: application/json\" \\\n...\n```\nWhen going live, you need to\
  \ generate new web service user credentials to access the [live endpoints](https://docs.adyen.com/development-resources/live-endpoints).\n\
  \n## Versioning\nThe Notification Configuration API supports [versioning](https://docs.adyen.com/development-resources/versioning)\
  \ using a version suffix in the endpoint URL. This suffix has the following format:\
  \ \"vXX\", where XX is the version number.\n\nFor example:\n```\nhttps://cal-test.adyen.com/cal/services/Notification/v6/createNotificationConfiguration\n\
  ```"
logo: "adyen.com-NotificationConfigurationService-logo.svg"
logoMediaType: "image/svg+xml"
tags:
- "payment"
stubs: "adyen.com-NotificationConfigurationService-stubs.json"
swagger: "adyen.com-NotificationConfigurationService-swagger.json"
---
