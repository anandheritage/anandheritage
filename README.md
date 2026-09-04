# Anand Kumar Shaw

I'm a platform and distributed systems architect working on data infrastructure
— realtime OLAP engines, high-throughput storage, and the kernel and network
datapaths underneath them. My work spans distributed query execution, transport security,
in-memory data representation, and per-packet processing in the Linux XDP
datapath.

Much of it traces back to a single primitive: compressed (Roaring) bitmaps. I've
carried that primitive across a Java bitmap library, a Java OLAP engine, a C++
column store, and a Go eBPF datapath. Solving the same problem in very different
languages and architectures is where most of what I know about distributed
systems design actually came from.

> **I'd rather build the Ferrari than own one.**

In India we've gotten very good at buying technology, and we're still learning to
build it at the deepest layers. I'd like to help change that, one upstream patch
at a time. If you'd rather build the thing than own it, I'd like to hear from
you.

## Open source

**Merged upstream**

- **[ClickHouse](https://github.com/ClickHouse/ClickHouse/pulls?q=is%3Apr+author%3Aanandheritage+is%3Aclosed)**
  — computing bitmap intersection cardinality without materializing the
  intersection, and filtering for access entity statements.
  
- **[Apache Pinot](https://github.com/apache/pinot/pulls?q=is%3Apr+author%3Aanandheritage+is%3Amerged)**
  — realtime distributed OLAP datastore. TLS across the multi-stage query engine
  and dispatch layer, GROUP BY execution correctness, and controller
  availability handling.
- **[RoaringBitmap](https://github.com/RoaringBitmap/RoaringBitmap/pulls?q=is%3Apr+author%3Aanandheritage+is%3Amerged)**
  — the compressed bitmap library behind Apache Spark, Apache Pinot, and Netflix
  Atlas. Copy-on-write bitmaps and container-level accounting.
- **[Linux kernel](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=39948c2d42b5093b49f1ad6c3b75df455331ac99)**
  — `bpf: Add missing XDP_ABORTED handling in cpumap`. The cpumap XDP fast path
  reported aborts as invalid actions instead of tracing them, unlike the skb,
  devmap, and generic XDP paths; this restores `trace_xdp_exception()` there.
- **[Cilium](https://github.com/cilium/cilium/pulls?q=is%3Apr+author%3Aanandheritage+is%3Amerged)**
  — eBPF-based networking, security, and observability. Host endpoint QoS setup
  in the datapath.
- **[Apache Pinot docs](https://github.com/pinot-contrib/pinot-docs/pulls?q=is%3Apr+author%3Aanandheritage+is%3Amerged)**
  — query option documentation.

**In review**



[All merged contributions across GitHub](https://github.com/search?q=is%3Apr+author%3Aanandheritage+is%3Amerged&type=pullrequests)

## Talks

- **[Going Deeper: A Journey from Databases to Data Structures to the Kernel](https://www.youtube.com/watch?v=shamgF8WHHk)**
  — Mosaic 2026.

---

*What you know is a drop in an Ocean.*
