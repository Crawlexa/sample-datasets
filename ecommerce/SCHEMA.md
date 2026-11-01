# eCommerce feed schema

## products
| Field | Type | Description |
|---|---|---|
| product_id | string | Stable ID assigned by Crawlexa |
| source | string | Website the record came from |
| title / brand / category | string | As listed on the source page |
| price / list_price | number | Current and pre-discount price |
| currency | string | ISO 4217 code |
| in_stock | boolean | Availability at capture time |
| rating / review_count | number | Average rating and number of reviews |
| seller | string | Marketplace seller, where shown |
| url | string | Source product page |
| captured_at | ISO 8601 UTC | When the record was collected |

## price_monitoring
| Field | Type | Description |
|---|---|---|
| your_sku / your_price | string / number | Client's product and price |
| competitor / competitor_price | string / number | Matched competitor listing |
| price_gap_pct | number | (competitor - yours) / yours x 100 |
| competitor_in_stock / promo_flag | boolean | Availability and active promotion |

Quality checks on every delivery: required fields present, price > 0, valid URLs, no duplicate product_id per source, refresh timestamp within SLA.
