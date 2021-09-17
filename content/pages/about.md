---
title: The Manifesto
subtitle: "EinstAI is an AI4DB Stochastic Context Free Grammar transmuting Transformer Regression Metadata collected with EinsteinDB's \_Timeshare Coordinator, FIDel, a deterministic oracle. Our Platform works great with Docker, Kubernetes, Ansible, and Natively. EinstAI provides 60% improvement of TPC SOTA benchmarks with zero-shot learning key-value stores in under 8 ms approx 300M Files-at-training. \_EinstAI provides a domain mixing contextual-switch with pushdown-serverless, leaderless, and globally available ANN-infrastructure built with distributed computing and chaos in mind. Runs on Kubernetes, CentOS7, Linux and BSD Kernels."
image: /images/Transparent.png
image_alt: Team members in a conference room
seo:
  title: About Us
  description: This is the about page
  extra:
    - name: 'og:type'
      value: website
      keyName: property
    - name: 'og:title'
      value: About Us
      keyName: property
    - name: 'og:description'
      value: This is the about page
      keyName: property
    - name: 'og:image'
      value: images/about.jpg
      keyName: property
      relativeUrl: true
    - name: 'twitter:card'
      value: summary_large_image
    - name: 'twitter:title'
      value: About Us
    - name: 'twitter:description'
      value: This is the about page
    - name: 'twitter:image'
      value: images/about.jpg
      relativeUrl: true
layout: PostLayout
---
Language has evolved to communicate intent, to state objectives, or to describe complex situations. It conveys information compactly by relying on composition and highlighting salient facts with a grammar. With the advent of the Transformer, a model architecture eschewing recurrence and relying entirely on an attention mechanism to draw global dependencies between input and output.

Music relies heavily on repetition to build structure and meaning. Self-reference occurs on multiple timescales, from motifs to phrases to reusing of entire sections of music, such as in pieces with ABA structure. The Transformer, a sequence model based on self-attention, While the original Transformer allows us to capture self-reference through attention, it relies on absolute timing signals and thus has a hard time keeping track of regularity that is based on relative distances, event orderings, and periodicity. 

As the Transformer model relies solely on positional sinusoids to represent timing information, EinstAI introduces relative position representations to allow attention to be informed by how far two positions are apart in a sequence.

EinstAI is a learned query scheduler that automatically learns how to order the execution of queries to minimize disk access requests. The core of  EinstAI includes a deep reinforcement learning (DRL) agent that learns:

*   a query scheduling policy through continuous interactions

    with its environment,

<!---->

*   a scheduling policy that maximizes its total reward.

<!---->

*   the maximum reward attainable from future buffer states to the reward for achieving its current buffer state, eectively inuencing the current scheduling decisio by the potential future reward.

Traditional databases are designed by database architects based on their experiences, but database architects can only explore a limited number of possible design spaces. Recently some learning based self-design techniques have been proposed. 

EinstI argues that the machine learning (ML) model is a perfect cache structure for the tree-based index, termed learned cache. Based on it, EinstAI builds on an RDMA-based ordered key-value store using EinsteinDB and MilevaDB.



EinstAI serves as a distributed hybrid architecture that retains a tree-based index at the server to perform dynamic workloads (e.g., inserts via AlterTables) and leverages a learned cache at the client to perform static workloads (e.g., gets and scans with MilevaDB). The key idea is to decouple ML model retraining from index updating by maintaining a layer of indirection from logical to actual positions of key-value pairs. It allows a stale learned cache to continue predicting a correct position for a lookup key.  Causets, the tuples EinsteinDB stores in Append-Logt and Binary format, ensures correctness using a validation mechanism with a fallback path and further uses speculative execution to minimize the cost of cache misses. Evaluations with YCSB benchmarks and production workloads show that a single EinstAI server can achieve over 80 million read-only requests per second. This number outperforms state-of-the-art RDMA-based ordered key-value store by up to 5.9× (from 3.7×). For workloads with inserts, EinsteinDB still provides up to 3.5× (from 2.7×) throughput speedup, achieving 53M reqs/s. The learned cache can also reduces client-side memory usage and further provides an efficient memory-performance tradeoff, e.g., saving 99% memory at the cost of 20% peak throughput.