---
swagger: "2.0"
x-collection-name: Broadleaf Commerce
x-complete: 0
info:
  title: Broadleaf Commerce API Put Wishlist Items
  description: Put wishlist items.
  version: 1.0.0
host: demo.broadleafcommerce.org
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /wishlist:
    get:
      summary: Get Wishlist
      description: Get wishlist.
      operationId: getWishlist
      x-api-path-slug: wishlist-get
      parameters:
      - in: query
        name: wishlistName
        description: wishlistName
      responses:
        200:
          description: OK
      tags:
      - Wishlist
    post:
      summary: Post Wishlist
      description: Post wishlist.
      operationId: postWishlist
      x-api-path-slug: wishlist-post
      parameters:
      - in: query
        name: wishlistName
        description: wishlistName
      responses:
        200:
          description: OK
      tags:
      - Wishlist
  /wishlist/configure-item:
    post:
      summary: Post Wishlist Configure Item
      description: Post wishlist configure item.
      operationId: postWishlistConfigureItem
      x-api-path-slug: wishlistconfigureitem-post
      parameters:
      - in: body
        name: orderItemWrapper
        description: orderItemWrapper
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: wishlistName
        description: wishlistName
      responses:
        200:
          description: OK
      tags:
      - Wishlist
      - Configure
      - Item
  /wishlist/item:
    post:
      summary: Post Wishlist Item
      description: Post wishlist item.
      operationId: postWishlistItem
      x-api-path-slug: wishlistitem-post
      parameters:
      - in: body
        name: orderItemWrapper
        description: orderItemWrapper
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: wishlistName
        description: wishlistName
      responses:
        200:
          description: OK
      tags:
      - Wishlist
      - Item
  /wishlist/items/{itemId}:
    put:
      summary: Put Wishlist Items
      description: Put wishlist items.
      operationId: putWishlistItemsItem
      x-api-path-slug: wishlistitemsitemid-put
      parameters:
      - in: path
        name: itemId
        description: itemId
      - in: query
        name: quantity
        description: quantity
      - in: query
        name: wishlistName
        description: wishlistName
      responses:
        200:
          description: OK
      tags:
      - Wishlist
      - Items
    delete:
      summary: Delete Wishlist Items
      description: Delete wishlist items.
      operationId: deleteWishlistItemsItem
      x-api-path-slug: wishlistitemsitemid-delete
      parameters:
      - in: path
        name: itemId
        description: itemId
      - in: query
        name: wishlistName
        description: wishlistName
      responses:
        200:
          description: OK
      tags:
      - Wishlist
      - Items
  /wishlist/items/{itemId}/move:
    post:
      summary: Post Wishlist Items Move
      description: Post wishlist items move.
      operationId: postWishlistItemsItemMove
      x-api-path-slug: wishlistitemsitemidmove-post
      parameters:
      - in: path
        name: itemId
        description: itemId
      - in: query
        name: wishlistName
        description: wishlistName
      responses:
        200:
          description: OK
      tags:
      - Wishlist
      - Items
      - Move
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---