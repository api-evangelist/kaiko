---
name: Read Canton oracle BTC-USD pricing
description: Fetch the current Canton oracle price and Benchmark Reference Rate (BRR) for BTC-USD from the Kaiko Market Data REST API.
api: openapi/kaiko-canton-oracle-api-openapi.yml
operations: [getCantonOracleBtcUsdPrice, getCantonOracleBtcUsdBrr]
generated: '2026-07-22'
method: generated
---

# Read Canton oracle BTC-USD pricing

Kaiko's Canton oracle endpoints expose signed institutional pricing for the Canton Network.
Access is enterprise/sales-led: you need a Kaiko client API key.

## Auth

Send the API key on every request in the `X-Api-Key` header. There is no OAuth; keys are
provisioned by Kaiko (docs: https://docs.kaiko.com/rest-api/general/getting-started/authentication.md).

## Steps

1. `GET /data/canton/oracle/price/btc-usd` (`getCantonOracleBtcUsdPrice`) on
   `https://us.market-api.kaiko.io/v2` — returns the current Canton oracle BTC-USD price.
2. `GET /data/canton/oracle/brr/btc-usd` (`getCantonOracleBtcUsdBrr`) — returns the current
   Canton oracle BRR (Benchmark Reference Rate) for BTC-USD.

## Rules

- Every response is a JSON envelope: check `result` (`success`|`error`); on error read
  `message`. The `access` object echoes your entitlement windows (see
  `conventions/kaiko-conventions.yml`).
- All operations are read-only GETs; safe to retry. Respect the standard limit of
  6000 requests per API key per minute — back off on HTTP 429.
- A 401 means the `X-Api-Key` header is missing/invalid; a 403 means your contract does not
  cover the Canton oracle product.
