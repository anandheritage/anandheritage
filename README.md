# Anand Kumar Shaw

I work on compressed bitmap internals, and on the query engines and datapaths
that depend on them. Most of my contributions start from the same primitive —
Roaring bitmaps — and follow it into whatever system needs it: a Java bitmap
library, a Java OLAP engine, a C++ column store, a Go eBPF datapath, and most
recently an LLM serving stack.

Based in India.

## Selected work

A curated subset of merged upstream contributions, not an exhaustive list.

**Compressed bitmap internals**

- [RoaringBitmap#780](https://github.com/RoaringBitmap/RoaringBitmap/pull/780) —
  implemented copy-on-write roaring bitmaps.
- [RoaringBitmap#742](https://github.com/RoaringBitmap/RoaringBitmap/pull/742) —
  added container size accounting.

**OLAP query engines**

- [apache/pinot#13645](https://github.com/apache/pinot/pull/13645) — added TLS
  configuration support for the QueryServer and the dispatch client.
- [apache/pinot#15844](https://github.com/apache/pinot/pull/15844),
  [#15966](https://github.com/apache/pinot/pull/15966) — corrected GROUP BY-only
  query processing under the `accurateGroupByWithoutOrderBy` query option.
- [apache/pinot#13954](https://github.com/apache/pinot/pull/13954) — handled
  empty server tags in the controller's availability check.

**Kernel and eBPF datapath**

- [cilium/cilium#43998](https://github.com/cilium/cilium/pull/43998) — optimized
  host endpoint QoS setup in the datapath.

## Currently working on

- [ClickHouse#117478](https://github.com/ClickHouse/ClickHouse/pull/117478)
  (open) — computing bitmap intersection cardinality without materializing the
  intersection.
- [ClickHouse#114647](https://github.com/ClickHouse/ClickHouse/pull/114647)
  (open) — `LIKE`/`NOT LIKE`/`ILIKE` filtering for `SHOW` access entity
  statements.
- [vllm-project/vllm#29296](https://github.com/vllm-project/vllm/pull/29296)
  (draft) — RoaringBitmap-based sparse attention mask.

---

*What you know is a drop in an Ocean.*
