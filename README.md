# test
Test Repo

master branch
2020-11-25 new line
commit test

Bookmap backend

## REST services

JAXRS_URL = http[s]://host[:port]/context-name

### Cart

CART_URL: ${JAXRS_URL}/card

1. Get cart
  - *URL:* ${CART_URL}
  - *Method:* GET
2. Add product to cart
  - *URL:* ${CART_URL}/add
  - *Method:* POST
  - *Content-Type:* application/json
  - *Parameter(s):* {productId: string, productName: string, currency: object, opts: [number,...]
    - productId: product identifier as a LOng
    - productName: product name
    - currency: selected currency as JSON-object
    - opts: selected options identifiers
3. Remove product from cart
  - *URL:* ${CART_URL}
  - *Method:* DELETE
  - *Parameter:* product - product identifier (Long)

