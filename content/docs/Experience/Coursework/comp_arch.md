---
title: Computer Architecture
---

# Computer Architecture

To paraphrase the course descriptions: At the end, I understood everything that happened to computer hardware from the time the power button was pressed.

We covered all sorts of topics:
- Pipelined processors and hazards
- Memory Hierarchy and Cache Types
- Multi-threading
- Multi-processor coherence
- IO and Storage
- Basic Networking

I took a total of 3 classes in this area, ECE 3058 (Computer Architecture), CS 3220 (Processor Design), and CS 4290 (Advanced COmputer Architecture).

As I moved onto the more advanced topics, I learned
- Branch Prediction
- VLIW Processors
- Out-of-Order Processors
- Super-scalar Processors
- GPU Architecture
- and more that I am forgetting right now

These courses were surprisingly hands on. The moment we covered something like a pipelined processor, I had to implement a 5-stage pipelined processor in Verilog along with a branch-predictor.

For some of the more complex hardware designs like branch predictors, out-of-order processor, or caches, I did software emulation of desgins in C/C++. At the end, I would do a design space exploration of my design against various parameters like cache size, predictor size, etc, to find the optimal design against a set of benchmarks.