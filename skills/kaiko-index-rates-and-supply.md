---
name: Pull Kaiko index rates, composition, and supply rankings
description: Retrieve Kaiko index reference rates, index composition/replication data, and asset supply / market-cap rankings from the Kaiko Market Data REST API.
api: openapi/kaiko-index-reference-data-api-openapi.yml
operations: [getIndexReferenceRates, getIndexDigitalAssetRatesComposition, getTopSupplyAssets]
generated: '2026-07-22'
method: generated
---

# Pull Kaiko index rates, composition, and supply rankings

Combine three read-only Kaiko Market Data endpoints to build an index/NAV data picture.
All requests are authenticated with the `X-Api-Key` header against
`https://us.market-api.kaiko.io/v2`.

## Steps

1. `GET /data/index_reference_data.v1/rates` (`getIndexReferenceRates`,
   spec `openapi/kaiko-index-reference-data-api-openapi.yml`) — reference-rate data for
   Kaiko indices.
2. `GET /data/index.v1/digital_asset_rates_compo` (`getIndexDigitalAssetRatesComposition`,
   spec `openapi/kaiko-indices-api-openapi.yml`) — index composition data for Kaiko's
   digital-asset rate indices.
3. `GET /data/supply.v2/top` (`getTopSupplyAssets`,
   spec `openapi/kaiko-supply-api-openapi.yml`) — market-capitalization rankings for top
   assets, for cross-checking constituents.

## Rules

- Check the JSON envelope on every call: `result` is `success` or `error`, with `message` on
  error and your entitlement ranges in `access`.
- Paginate with `continuation_token` (or follow `next_url`); set `page_size` only on the
  first request (docs: https://docs.kaiko.com/rest-api/general/getting-started/pagination.md).
- Pin an explicit dataset version (`data_version`) in production rather than `latest`; the
  resolved version is echoed in the `query` field.
- Read-only GETs, safe to retry; back off on 429 (6000 requests per key per minute).
