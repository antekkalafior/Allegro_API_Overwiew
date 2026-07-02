# Category_checker

Public documentation for the **Category_checker** Allegro REST API application.

User-Agent: `Category_checker/1.0.0 (+https://github.com/antekkalafior/Allegro_API_Overwiew)`

## Endpoints used

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/sale/categories` | Retrieve category tree |
| GET | `/sale/products` | Look up products by EAN / phrase |
| GET | `/offers/listing` | Resolve product category from listings |
| GET | `/sale/product-offers/{offerId}` | Read offer details |
| GET | `/sale/offers` | List seller offers |
| GET | `/sale/delivery-methods` | List available delivery methods |
| GET | `/sale/shipping-rates` | Read delivery price lists |
| POST | `/sale/shipping-rates` | Create delivery price lists |
| PUT | `/sale/shipping-rates/{id}` | Update delivery price lists |
| PATCH | `/sale/offers/{offerId}` | Assign shipping rate to offer |
