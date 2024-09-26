---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

## Hardware Support for Microservices in the Cloud (UIUC)

Current processors are not designed for microservices, an  emerging cloud-computing paradigm. 
Contrary to long-running monolithic applications, microservice environments execute short
functions that only interact with one another via remote procedure calls  and are subject to stringent tail-latency constraints.
During the third year of my PhD, I designed 1) an architecture optimized for cloud-native environments that 
minimizes unnecessary architecture and removes contention hot-spots that degrade the tail latency
(<span>&#181;</span>Manycore, ISCA'23), and 2) a processor architecture that enables efficient and secure resource harvesting in the cloud (<span>&#181;</span>Harvest, YArch'23). During the fourth year of my PhD, I have been working on 1) a hardware-software co-design that improves micro-architectural resource utilization in microservice/serverless environments (Mosaic, MICRO '24), and 2) a hardware cache coherence protocol that enables servers running microservices to scale to thousands of cores.

## High-Performant Serverless Computing (UIUC, IBM, and Microsoft) 

Current serverless workloads exhibit multiple levels of overheads, including cold start, virtualization, RPC, and the need to persist temporal outputs in remote storage. To make the matter worse, the overheads have significant cascading effects for applications that orchestrate multiple functions through control and data dependencies, which is a common practice in complex real-world applications. During the second and third year of my PhD, I redesigned serverless platforms by 1) applying data and control speculation techniques (SpecFaaS, HPCA'23), 2) creating a novel container abstraction that ensures high cpu, memory and I/O resource utilization while minimizing the response time (MXFaaS, ISCA'23), and 3) providing a systematic approach for mapping the unique characteristics of serverless workload to the design and organization of distributed caching scheme (UniCache, AIOps'24). 
During the fourth year of my PhD, I have been working on 1) a design of energy efficient serverless system (EcoFaaS, ISCA'24), 2) a design of a cost-efficient cloud overclocking (SmartOClock ISCA'24), and 3) an efficient coherence protocol for distributed software caches in serverless environments.

## Energy-Efficient LLM Inference Servers (UIUC and Microsoft) 

The rapid evolution and widespread adoption of generative large language models (LLMs) have made them a pivotal workload in various applications. Today, LLM inference clusters receive a large number of queries with strict Service Level Objectives (SLOs). To achieve the desired performance, these models execute on power-hungry GPUs causing the inference clusters to consume large amount of energy and, consequently, result in excessive carbon emissions.
During the fourth year of my PhD, I conducted a comprehensive analysis of these systems and redesigned LLM inference architectures, making energy efficiency a first-class citizen in the design process (DynamoLLM, arxiv).

## Leveraging Parallelism in Virtualized Address Translation (UIUC)

In spite of nearly twenty years since the inception of virtualization hardware, address translation still introduces substantial performance overhead in virtualized systems. A major reason why address translation has high overhead is because page tables are currently organized in a multi-level tree that is accessed in a sequential manner. This organization is called radix page tables. During my first year of PhD, I redesigned the virtual memory subsystem in virtualized environments to improve its 1) performance by exploiting available memory level parallelism (Nested ECPTs, ASPLOS'22) and 2) memory efficiency by breaking the hashed page table into multiple small
allocation units while maintaining the same performance through carefully chosen design decisions (ME-HPTs, HPCA'23). 

## Exploring the Design Space of Virtual Memory: Performance, Memory, Energy Efficiency, Security and Hardware Heterogeneity (UIUC)

I did an extensive study of the virtual memory subsystem in virtualized environments and conducted sensitivity analyses on helper hardware structures. My results suggest that the current radix organization of page tables is not scalable with a large memory footprint workload. Moreover, I reproduced literature solutions to avoid hardware-based address translation and instead used compiler and runtime protection mechanisms. I also explored the virtual memory design for GPUs and available prefetching opportunities inherently exposed by the SIMT model of execution. Finally, I conducted a study on the security implications of different page table and TLB organizations with existing attack and defense schemes.

## Edge Computing Platform for Collaborative Augmented Reality (Duke)

I built a platform that allows multiple users’ related images, captured with Android phones running Google ARCore, to be processed jointly on an edge server, improving user’s quality of object recognition. Additionally, I improved performance by reusing cached results from the database. I also did comparative benchmarking of two image recognition tools (AWS Rekognition and Yolo) in terms of quality and time efficiency. I went further to explore possible trade-offs. The project was presented at Duke's REU Symposium and published at IPSN and SenSys.
