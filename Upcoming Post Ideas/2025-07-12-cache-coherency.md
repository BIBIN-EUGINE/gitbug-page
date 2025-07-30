---
title: "Core and Uncore Devices"
excerpt_separator: "<!--more-->"
categories:
  - Tech
tags:
  - Memory
---

# Core and Uncore Devices
 - A walkthrough on Core devices and uncore devices of a processor

Computer architecture is the combination of microarchitecture and ISA. The mircroarchitecture
facilate the parts and defines how to connect interconnect and interpolate to implement ISA.
Microarchitecture is also called as computer organization and it mainly contains Core and Uncore devices. Core is something is which based on architecuture, for example ArmV8-A architecture and Uncore is term defined to address the functions that are not part of this architecture, but they set very close to Core in order to enable high performance. For instance, Memory controller, bus controllers are part of uncore functions.

## Interface with Core
cBox, pBox, ...

**cBox**: The main uncore interface with the core, which interfaces the last level cache and is responsible for managing cache coherency.

## Last Level Cache and Cache Coherency

In a multi core system, it has L1,L2,L3 and so on..Generally, L1 per core, L2 intermediate shared between pair of cores, L3 global between all cores.

In this case L3 is the last level Cache and are responsible for cache coherency.
*Cache Coherency* : In a multiprocessing system, each CPU may cache a local copy of the same region of  a shared memory resource, and all copies should be same. Cache Coherency protocol
ensures that it changes in values of operands are propagated throughout the system in a timely manner.

## SuperScalar
it's executing multiple instrucitions in parallles, in out of order if there is no dependency between those instructions. Register renaming is one of the techinquies used in this mechanism