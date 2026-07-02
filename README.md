# Category_checker

Allegro REST API application (`Category_checker/1.0.0`).

## API usage

| Endpoint | Purpose |
|---|---|
| `/sale/categories` | Retrieve product category tree |
| `/sale/products` | Query catalogue products by EAN / name |
| `/sale/product-offers/{offerId}` | Read offer details |
| `/sale/offers` | List seller offers |
| `/sale/shipping-rates` | Read, create and update delivery price lists |
| `/sale/offers/{offerId}` (PATCH) | Assign shipping rate tables to offers |
| `/billing/billing-entries` | Retrieve commission rates per category |

All operations are performed on the operator's own seller accounts.
