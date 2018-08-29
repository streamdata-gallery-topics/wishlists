---
swagger: "2.0"
x-collection-name: Reverb
x-complete: 0
info:
  title: Reverb Delete My Wishlist
  description: Remove a listing from your wishlist
  termsOfService: https://reverb.com/page/terms
  contact:
    name: Reverb API
    url: https://dev.reverb.com
    email: integrations@reverb.com
  version: "3.0"
host: api.reverb.com
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /my/wishlist:
    get:
      summary: Get My Wishlist
      description: Get a list of wishlisted items
      operationId: getMyWishlist
      x-api-path-slug: mywishlist-get
      responses:
        200:
          description: OK
      tags:
      - My
      - Wishlist
  /my/wishlist/{id}:
    delete:
      summary: Delete My Wishlist
      description: Remove a listing from your wishlist
      operationId: deleteMyWishlist
      x-api-path-slug: mywishlistid-delete
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - My
      - Wishlist
      - Id
    put:
      summary: Put My Wishlist
      description: Add a listing to your wishlist
      operationId: putMyWishlist
      x-api-path-slug: mywishlistid-put
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - My
      - Wishlist
      - Id
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