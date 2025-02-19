---
slug: "vtex-local-Catalog-API"
title: "Catalog API"
provider: "vtex.local"
description: "\r\n> Check the new [Catalog onboarding guide](https://developers.vtex.com/docs/guides/catalog-overview).\
  \ We created this guide to improve the onboarding experience for developers at VTEX.\
  \ It assembles all documentation on our Developer Portal about Catalog and is organized\
  \ by focusing on the developer's journey.\r\n\r\nMethods for collecting product/SKU\
  \ catalog data, categories, brands and other information. All content that comes\
  \ between `{{}}` keys must be replaced with the correct data before performing the\
  \ request.\r\n\r\n\r\n## Index\r\n\r\n- [Product](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog_system/pvt/products/GetProductAndSkuIds)\
  \ - Here you can consult, create, or update a Product. For more information, check\
  \ [this article](https://help.vtex.com/tracks/catalog-101--5AF0XfnjfWeopIFBgs3LIQ/1wmX3QvQVxbKVmalhIE5Ru).\r\
  \n- [Product Specification](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog_system/pvt/products/-productId-/specification)\
  \ - You can consult, create, or update additional information of a Product.  For\
  \ more information, check [this article](https://help.vtex.com/tracks/catalog-101--5AF0XfnjfWeopIFBgs3LIQ/2NQoBv8m4Yz3oQaLgDRagP#product-specification).\r\
  \n- [SKU](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog_system/pvt/sku/stockkeepingunitids)\
  \ - Here you can consult, create, or update an SKU. For more information, check\
  \ [this article](https://help.vtex.com/tracks/catalog-101--5AF0XfnjfWeopIFBgs3LIQ/3mJbIqMlz6oKDmyZ2bKJoA).\r\
  \n- [SKU Complement](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog/pvt/stockkeepingunit/-skuId-/complement)\
  \ - You can consult, create, or update an SKU Complement. An SKU Complement is a\
  \ new SKU that has a Parent SKU.\r\n- [SKU EAN](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog_system/pvt/sku/stockkeepingunitbyean/-ean-)\
  \ -  Here you can consult, create, or update an SKU unique identification code (barcode).\r\
  \n- [SKU Attachment](https://developers.vtex.com/docs/api-reference/catalog-api#post-/api/catalog/pvt/skuattachment)\
  \ - You can consult, create, or update an SKU Attachment. An attachment is used\
  \ to add custom information about the item. For more information, check [this article](https://help.vtex.com/tutorial/what-is-an-attachment--aGICk0RVbqKg6GYmQcWUm?locale=en).\r\
  \n- [SKU File](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog/pvt/stockkeepingunit/-skuId-/file)\
  \ - Here you can consult, create, or update an SKU File. An SKU File is an image\
  \ associated with an SKU.\r\n- [SKU Kit](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog/pvt/stockkeepingunitkit)\
  \ - You can consult, create, or update an SKU Kit. A kit is an SKU composed of one\
  \ or more SKUs. For more information, check [this article](https://help.vtex.com/tutorial/what-is-a-kit--5ov5s3eHM4AqAAgqWwoc28?locale=en).\r\
  \n- [SKU Seller](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog_system/pvt/skuseller/-sellerId-/-sellerSkuId-)\
  \ - Here you can consult and delete an SKU Seller. An SKU Seller is a seller associated\
  \ with an SKU. For more information, check [this article](https://help.vtex.com/tutorial/what-is-a-seller--5FkLvhZ3Few4CWWIuYOK2w?locale=en).\r\
  \n- [SKU Service](https://developers.vtex.com/docs/api-reference/catalog-api#put-/api/catalog/pvt/skuservice/-skuServiceId-)\
  \ - You can create, update, or delete an SKU Service. A service is an item that\
  \ may come with a product, optionally, and with a cost. For more information, check\
  \ [this article](https://help.vtex.com/tutorial/what-is-a-service--46Ha8CEEQoC6Y40i6akG0y?locale=en).\r\
  \n- [SKU Service Attachment](https://developers.vtex.com/docs/api-reference/catalog-api#post-/api/catalog/pvt/skuservicetypeattachment)\
  \ - Here you can associate or disassociate an Attachment to an SKU Service.\r\n\
  - [SKU Service Type](https://developers.vtex.com/docs/api-reference/catalog-api#post-/api/catalog/pvt/skuservicetype)\
  \ - You can create, update, or delete an SKU Service Type. A service type is the\
  \ behavior configuration of a service.\r\n- [SKU Service Value](https://developers.vtex.com/docs/api-reference/catalog-api#post-/api/catalog/pvt/skuservicevalue)\
  \ - Here you can create, update, or delete an SKU Service Value. Service value is\
  \ how much the customer will be charged for the service.\r\n- [SKU Specification](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog/pvt/stockkeepingunit/-skuId-/specification)\
  \ - You can consult, create, or delete an SKU Specification. SKU Specification is\
  \ used to create site browsing filters and to differentiate SKUs within the product\
  \ page. For more information, check [this article](https://help.vtex.com/tracks/catalog-101--5AF0XfnjfWeopIFBgs3LIQ/2NQoBv8m4Yz3oQaLgDRagP?locale=en#sku-specifications).\r\
  \n- [Legacy Subcollection](https://developers.vtex.com/docs/api-reference/catalog-api#post-/api/catalog/pvt/subcollection/-subCollectionId-/stockkeepingunit)\
  \ - Here you can can consult, create, or delete an SKU, Brand or Category from a\
  \ Subcollection, as well as create, delete and update subcollections. A subcollection\
  \ is a group type associated with a collection. For more information, check [this\
  \ article](https://help.vtex.com/tracks/catalog-101--5AF0XfnjfWeopIFBgs3LIQ/3moFonW33dgOYDrU21Z1X0#group-types).\r\
  \n- [Category](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog_system/pub/category/tree/-categoryLevels-)\
  \ - You consult, create, or update a Category. A category is a hierarchical level\
  \ of product classification. For more information, check [this article](https://help.vtex.com/tracks/catalog-101--5AF0XfnjfWeopIFBgs3LIQ/2gkZDjXRqfsq62TlAkj4uf).\r\
  \n- [Similar Category](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog/pvt/product/-productId-/similarcategory/)\
  \ - Here you can create and delete a Similar Category to a Product. This way the\
  \ Product will be shown in both categories (main and similar).\r\n- [Category Specification](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog_system/pub/specification/field/listByCategoryId/-categoryId-)\
  \ - You can consult all Specifications by Category. For more information about Specification,\
  \ check [this article](https://help.vtex.com/tracks/catalog-101--5AF0XfnjfWeopIFBgs3LIQ/2NQoBv8m4Yz3oQaLgDRagP).\r\
  \n- [Brand](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog_system/pvt/brand/list)\
  \ - You can consult, create, update, or delete a Brand. A brand is a product property.\
  \ For more information, check [this article](https://help.vtex.com/tracks/catalog-101--5AF0XfnjfWeopIFBgs3LIQ/7i3sB8fgkqUp5NoH5yJtfh).\r\
  \n- [Attachment](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog/pvt/attachment/-attachmentid-)\
  \ - You can consult, create, or update an Attachment. An attachment is used to add\
  \ custom information about the item. For more information, check [this article](https://help.vtex.com/tutorial/what-is-an-attachment--aGICk0RVbqKg6GYmQcWUm?locale=en).\r\
  \n- [Collection Beta](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog_system/pvt/collection/search)\
  \ - The new [Beta Collections module](https://help.vtex.com/announcements/new-beta-collections-module-easily-create-and-manage-product-collections--6KvFxylC5SNsbVm8L8XZpZ#)\
  \ launch allowed us to engineer new endpoints that create and manage Collections.\
  \ For more information, check [this article](https://help.vtex.com/en/tutorial/creating-collections-beta--yJBHqNMViOAnnnq4fyOye?&utm_source=autocomplete#).\r\
  \n- [Legacy Collection](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog/pvt/collection/-collectionId-)\
  \ - Here you can consult, create, update, or delete a Collection. A collection is\
  \ a group of items. For more information, check [this article](https://help.vtex.com/tracks/catalog-101--5AF0XfnjfWeopIFBgs3LIQ/4hN41yU8IPeb8HKmmaXoca?locale=en).\r\
  \n- [Specification](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog/pvt/specification/-specificationId-)\
  \ - Here you can consult, create, or delete a Specification. A specification is\
  \ used to create site browsing filters and to differentiate SKUs and Products within\
  \ the product page. For more information, check [this article](https://help.vtex.com/tracks/catalog-101--5AF0XfnjfWeopIFBgs3LIQ/2NQoBv8m4Yz3oQaLgDRagP?locale=en).\r\
  \n- [Specification Field](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog_system/pub/specification/fieldGet/-fieldId-)\
  \ - You can consult, create, or update a Specification Field. A specification field\
  \ allows you to present more detailed items. \r\n- [Specification Field Value](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog_system/pvt/specification/fieldValue/-fieldValueId-)\
  \ - Here you can consult, create, or update a Specification Field Value. \r\n- [Specification\
  \ Value](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog/pvt/specificationvalue/-specificationValueId-)\
  \ - You can consult, create, or update a Specification Value.\r\n- [Specification\
  \ Group](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog_system/pvt/specification/groupbycategory/-categoryId-)\
  \ - Here you can consult, create, or update a Specification Group.\r\n- [Non Structured\
  \ Specification](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog/pvt/specification/nonstructured/-Id-)\
  \ - You can consult or delete a Non Structured Specification.\r\n- [Sales Channel](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog_system/pvt/saleschannel/list)\
  \ - Here you can consult Sales Channel.\r\n- [Seller](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog_system/pvt/seller/list)\
  \ - You can consult, create, or update a Seller. A seller is the _product owner_.\
  \ For more information, check [this article](https://help.vtex.com/tutorial/what-is-a-seller--5FkLvhZ3Few4CWWIuYOK2w?locale=en).\r\
  \n- [Supplier](https://developers.vtex.com/docs/api-reference/catalog-api#post-/api/catalog/pvt/supplier)\
  \ - Here you can consult, create, or update a Supplier.\r\n- [Trade Policy](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog/pvt/product/-productId-/salespolicy)\
  \ - You can create, update, or delete a Trade Policy. Trade policy is required when\
  \ one of the above factors is different among the sale channel. For more information,\
  \ check [this article](https://help.vtex.com/tutorial/what-is-a-sales-policy--563tbcL0TYKEKeOY4IAgAE?locale=en).\r\
  \n- [Product Indexing](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog_system/pvt/products/GetIndexedInfo/-productId-)\
  \ - Here you can consult Product Indexed information.\r\n- [Commercial Conditions](https://developers.vtex.com/docs/api-reference/catalog-api#get-/api/catalog_system/pvt/commercialcondition/list)\
  \ - Here you can consult commercial conditions registered in the store.\r\n\r\n\r\
  \n## Common parameters\r\n\r\n| Parameter name              | Description      \
  \                                                                       |\r\n|---------------------------|-----------------------------------------------------------------------------------------|\r\
  \n| `{{accountName}}`         | Store account name                             \
  \                                         |\r\n| `{{environment}`          | The\
  \ environment that will be called. Change for vtexcommercestable or vtexcommmercebeta\
  \ |\r\n| `{{X-VTEX-API-AppKey}}`   | Located in the headers of the requests, user\
  \ authentication key                         |\r\n| `{{X-VTEX-API-AppToken}}` |\
  \ Located in the headers of the requests, authentication password              \
  \           |"
logo: "vtex.local-Catalog-API-logo.svg"
logoMediaType: "image/svg+xml"
tags: []
stubs: "vtex.local-Catalog-API-stubs.json"
swagger: "vtex.local-Catalog-API-swagger.json"
---
