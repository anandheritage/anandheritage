# Anand Kumar Shaw

I'm a systems architect working on distributed data infrastructure — realtime
OLAP engines, high-throughput storage, and the kernel and network datapaths
underneath them. My work spans distributed query execution, transport security,
in-memory data representation, and per-packet processing in the Linux XDP
datapath.

Much of it traces back to a single primitive: compressed (Roaring) bitmaps. I've
carried that primitive across a Java bitmap library, a Java OLAP engine, a C++
column store, a Go eBPF datapath, and an LLM serving stack. Solving the same
problem across five languages and five very different architectures is where
most of what I know about distributed systems design actually came from.

I contribute upstream to the systems I build on, rather than maintaining private
forks of them.

Based in India.

## Open source

**Merged upstream**

- **[Apache Pinot](https://github.com/apache/pinot/pulls?q=is%3Apr+author%3Aanandheritage+is%3Amerged)**
  — realtime distributed OLAP datastore. TLS across the multi-stage query engine
  and dispatch layer, GROUP BY execution correctness, and controller
  availability handling.
- **[RoaringBitmap](https://github.com/RoaringBitmap/RoaringBitmap/pulls?q=is%3Apr+author%3Aanandheritage+is%3Amerged)**
  — the compressed bitmap library behind Apache Spark, Apache Pinot, and Netflix
  Atlas. Copy-on-write bitmaps and container-level accounting.
- **[Cilium](https://github.com/cilium/cilium/pulls?q=is%3Apr+author%3Aanandheritage+is%3Amerged)**
  — eBPF-based networking, security, and observability. Host endpoint QoS setup
  in the datapath.
- **[Apache Pinot docs](https://github.com/pinot-contrib/pinot-docs/pulls?q=is%3Apr+author%3Aanandheritage+is%3Amerged)**
  — query option documentation.

**In review**

- **[ClickHouse](https://github.com/ClickHouse/ClickHouse/pulls?q=is%3Apr+author%3Aanandheritage+is%3Aopen)**
  — computing bitmap intersection cardinality without materializing the
  intersection, and filtering for access entity statements.
- **[vLLM](https://github.com/vllm-project/vllm/pulls?q=is%3Apr+author%3Aanandheritage+is%3Aopen)**
  — RoaringBitmap-backed sparse attention masks.

[All merged contributions across GitHub](https://github.com/search?q=is%3Apr+author%3Aanandheritage+is%3Amerged&type=pullrequests)

---

*What you know is a drop in an Ocean.*
