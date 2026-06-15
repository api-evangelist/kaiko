# Kaiko (kaiko)

Kaiko is an institutional-grade crypto market data provider. Its product line spans Kaiko REST (historical and reference data), Kaiko Stream (real-time WebSocket and gRPC), Cloud Delivery (S3 and Snowflake direct shares), Kaiko On-chain, and Kaiko Indices (regulated benchmark indices). Authentication uses API keys; access is sales-led.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/kaiko/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/kaiko/refs/heads/main/apis.yml)

## Tags

- Web3
- Crypto
- Market Data
- Institutional
- FX
- Indices
- On-Chain
- Streaming

## Timestamps

- **Created:** 2026-05-08
- **Modified:** 2026-05-29

## APIs

### Kaiko REST API

REST endpoints for trades, order books, OHLCV, market reference, trade flows, FX rates, and derivatives across 100+ exchanges. Historical depth back to 2014. Authentication via X-Api-Key header.

- **Human URL:** [https://docs.kaiko.com/](https://docs.kaiko.com/)
- **Base URL:** `https://us.market-api.kaiko.io/v2`

#### Tags

- Crypto
- Market Data
- Reference Data
- Historical
- Institutional

#### Properties

- [Documentation](https://docs.kaiko.com/)
- [Postman Collection](collections/kaiko.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kaiko.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Kaiko Stream

Real-time crypto market data delivered over gRPC server-streaming. Feeds include tick-level trades, top-of-book (best bid/ask), level-2 order book updates, level-1 aggregations (OHLCV, VWAP), derivatives reference data, and analytics (Best Execution, Fair Market Value, Derivatives Risk Indicators). Transport is gRPC only; Kaiko does not publish a WebSocket interface (see review.yml).

- **Human URL:** [https://docs.kaiko.com/stream/general/introduction](https://docs.kaiko.com/stream/general/introduction)

#### Tags

- Streaming
- Real-time
- gRPC

#### Properties

- [Documentation](https://docs.kaiko.com/stream/general/introduction)
- [SDK](https://github.com/kaikodata/kaiko-sdk-examples)
- [Review](review.yml)
- [Postman Collection](collections/kaiko.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kaiko.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Kaiko On-chain API

On-chain metrics including DEX trades, liquidity, lending markets, and MEV signals across major chains.

- **Human URL:** [https://docs.kaiko.com/onchain/overview](https://docs.kaiko.com/onchain/overview)
- **Base URL:** `https://us.market-api.kaiko.io/v2/data/onchain`

#### Tags

- On-Chain
- DEX
- Liquidity
- Multi-chain

#### Properties

- [Documentation](https://docs.kaiko.com/onchain/overview)
- [Postman Collection](collections/kaiko.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kaiko.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Kaiko Indices

Regulated benchmark crypto indices designed for fund administrators and ETF/ETP issuers.

- **Human URL:** [https://www.kaiko.com/products/indices](https://www.kaiko.com/products/indices)
- **Base URL:** `https://us.market-api.kaiko.io/v2/data/index.v1`

#### Tags

- Indices
- Benchmark
- Regulated

#### Properties

- [Documentation](https://www.kaiko.com/products/indices)
- [Postman Collection](collections/kaiko.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/kaiko.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/kaikodata)
- [LinkedIn](https://www.linkedin.com/company/kaikodata)
- [Portal](https://www.kaiko.com/)
- [Documentation](https://docs.kaiko.com/)
- [Plans](plans/kaiko-plans-pricing.yml)
- [Rate Limits](rate-limits/kaiko-rate-limits.yml)
- [Fin Ops](finops/kaiko-finops.yml)
- [L L Ms Txt](https://docs.kaiko.com/llms.txt)
- [Review](review.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
