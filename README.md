# test
Test Repo

master branch
2020-11-25 new line
commit test

# Bookmap backend

## REST services

**JAXRS_URL** = http[s]://host[:port]/context-name

**Response:**
    Content-Type: application/json
        {
          "status": 0(OK) | 1(ERROR),
          "count": number >= 0 (count of records in field "data"),
          "data": null | JSON-object | JSON-array,
          "message": null | error message if status equals 1
        }

### Cart

**CART_URL**: ${JAXRS_URL}/card

1. Get cart
  - **URL:** ${CART_URL}
  - **Method:** GET
2. Add/replace product to/in cart
  - **URL:** ${CART_URL}/add
  - **Method:** POST
  - **Content-Type:** application/json
  - **Parameter(s):** {productId: string, productName: string, currency: object, opts: [number,...]
    - productId: product identifier as a Long
    - productName: product name
    - currency: selected currency as JSON-object
    - opts: selected options identifiers
3. Remove product from cart
  - **URL:** ${CART_URL}
  - **Method:** DELETE
  - **Parameter:** product - product identifier (Long)

### Product 

**PRODUCT_URL**: ${JAXRS_URL}/product

1. Get product by identifier
  - **URL:** ${PRODUCT_URL}/<product-identifier>
  - **Method:** GET
2. Get product list (all or by categories)
  - **URL:** ${PRODUCT_URL}/list
  - **Method:** GET
  - **Content-Type:** application/x-www-form-urlencoded
  - **Parameters:** category(optional,multiple) - category identifier

### Category

**CATEGORY_URL**: ${JAXRS_URL}/category

1. Get category by identifier
  - **URL:** ${CATEGORY_URL}/<category-identifier>
  - **Method:** GET
2. Get categories list
  - **URL:** ${CATEGORY_URL}/list
  - **Method:** GET

### Currency

**CURRENCY_URL**: ${JAXRS_URL}/currency

1. Get currency by identifier
  - **URL:** ${CURRENCY_URL}/<currency-identifier>
  - **Method:** GET
2. Get currency list
  - **URL:** ${CURRENCY_URL}/list
  - **Method:** GET

### Country

**COUNTRY_URL**: ${JAXRS_URL}/country

1. Get country by identifier
  - **URL:** ${COUNTRY_URL}/<country-identifier>
  - **Method:** GET
2. Get country list
  - **URL:** ${COUNTRY_URL}/list
  - **Method:** GET


