---
layout: post
title: Columnar In-Memory Analytics using Arrow
---

Today marks the 3rd anniversary of Apache Arrow and I thought why not write about this highly underated library which is slowly and steadily [taking the analytics community by storm](https://twitter.com/wesmckinn/status/1097871072622460928).

So, what is **Arrow**.

>Well,  Apache Arrow is a cross-language development platform for in-memory data. It specifies a standardized language-independent columnar memory format for flat and hierarchical data, organized for efficient analytic operations on modern hardware. It also provides computational libraries and zero-copy streaming messaging and interprocess communication. Languages currently supported include C, C++, C#, Go, Java, JavaScript, MATLAB, Python, R, Ruby, and Rust.

Engineers from across the Apache Hadoop community are collaborating to establish Arrow as a de-facto standard for columnar in-memory processing and interchange. Here’s how it works.

[Apache Arrow](https://arrow.apache.org) is an in-memory data structure specification for use by engineers building data systems. It has several key benefits:

* A columnar memory-layout permitting O(1) random access. The layout is highly cache-efficient in analytics workloads and permits SIMD optimizations with modern processors. Developers can create very fast algorithms which process Arrow data structures.
* Efficient and fast data interchange between systems without the serialization costs associated with other systems like Thrift, Avro, and Protocol Buffers.
* A flexible structured data model supporting complex types that handles flat tables as well as real-world JSON-like data engineering workloads.

Arrow isn’t a standalone piece of software but rather a component used to accelerate analytics within a particular system and to allow Arrow-enabled systems to exchange data with low overhead. It is sufficiently flexible to support most complex data models.

For the Python and R communities, Arrow is extremely important, as data interoperability has been one of the biggest roadblocks to tighter integration with big data systems (which largely run on the JVM).
