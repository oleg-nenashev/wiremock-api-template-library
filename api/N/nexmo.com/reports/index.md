---
slug: "nexmo-com-reports"
title: "Reports API"
provider: "nexmo.com"
description: "The [Reports API](/reports/overview) enables you to request a report\
  \ of activity for your Vonage account.\n\nDepending on your query pattern, you can\
  \ choose from one of the two versions of the Reports API: asynchronous and synchronous.\
  \ The asynchronous version is optimized for infrequent and large data queries (from\
  \ several records to tens of millions). The synchronous version is optimized for\
  \ frequent and periodic retrievals of small batches of data records (from one record\
  \ to tens of thousand per query).\n\nOnly synchronous version supports retrival\
  \ of data records by message/record ID.\n\nVonage recommends that you limit asynchronous\
  \ queries to a maximum of 20 million records, by setting the start and end dates\
  \ accordingly. On average, the asynchronous Reports API takes 5 - 10 minutes to\
  \ generate 1 million records.\n"
logo: "nexmo.com-reports-logo.svg"
logoMediaType: "image/svg+xml"
tags: []
stubs: "nexmo.com-reports-stubs.json"
swagger: "nexmo.com-reports-swagger.json"
---
