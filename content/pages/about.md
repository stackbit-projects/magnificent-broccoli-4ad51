---
title: The Manifesto
subtitle: "At Einst.AI, We're embracing the meta universe and consider ourselves a meta-learning enterprise that is model-agnostic, in the sense that we're pretty compatible with any model trained with stochastic gradient descent and applicable to a variety of different learning problems, including classification, regression, and reinforcement learning."
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
Einst.AI uses *domain randomization *to train in a very diverse set of simulated environments that enables transfer to the real world. Domain randomization is the extension of data augmentation, which has been used in computer vision since the inception of convolutional networks, from data sets to simulators. Randomizing many aspects of the simulation that do not match the real world forces the learned model to be robust to these variations.

Distractions can look technically similar to domain randomization but distractions are part of the problem that the agent has to solve rather than part of the solution. As a result, the agent does not have control over distractions, i.e. cannot affect these distractions, cannot arbitrarily sample more of them, and has to handle them during evaluation.

The magnitude of each distraction type can be controlled by a “difficulty magnitude” scalar between 0 and 1. Distractions can be set to either change during episodes or change only between episodes, which we will refer to as *dynamic *and *static *settings, respectively.
to the reward for achieving its current buffer state, eectively inuencing the current scheduling decisio by the potential future reward.

Traditional databases are designed by database architects based on their experiences, but database architects can only explore a limited number of possible design spaces. Recently some learning based self-design techniques have been proposed. 

EinstI argues that the machine learning (ML) model is a perfect cache structure for the tree-based index, termed learned cache. Based on it, EinstAI builds on an RDMA-based ordered key-value store using EinsteinDB and MilevaDB.



EinstAI serves as a distributed hybrid architecture that retains a tree-based index at the server to perform dynamic workloads (e.g., inserts via AlterTables) and leverages a learned cache at the client to perform static workloads (e.g., gets and scans with MilevaDB). The key idea is to decouple ML model retraining from index updating by maintaining a layer of indirection from logical to actual positions of key-value pairs. It allows a stale learned cache to continue predicting a correct position for a lookup key.  Causets, the tuples EinsteinDB stores in Append-Logt and Binary format, ensures correctness using a validation mechanism with a fallback path and further uses speculative execution to minimize the cost of cache misses. Evaluations with YCSB benchmarks and production workloads show that a single EinstAI server can achieve over 80 million read-only requests per second. This number outperforms state-of-the-art RDMA-based ordered key-value store by up to 5.9× (from 3.7×). For workloads with inserts, EinsteinDB still provides up to 3.5× (from 2.7×) throughput speedup, achieving 53M reqs/s. The learned cache can also reduces client-side memory usage and further provides an efficient memory-performance tradeoff, e.g., saving 99% memory at the cost of 20% peak throughput.