---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<span class='anchor' id='about-me'></span>

# About Me 🚀

I am an M.Eng. candidate in Computer Technology at the University of Science and Technology of China (USTC), expected to graduate in June 2027. My work focuses on **LLM inference systems, high-performance model serving, communication-computation overlap, and CPU-GPU heterogeneous inference**.

I have worked on inference acceleration and serving-system optimization across Tencent, ByteDance, and Huawei 2012 Laboratories. My recent projects involve adapting Hunyuan Image inference pipelines to vLLM/vLLM-Omni, optimizing NCCL AllReduce bottlenecks in tensor-parallel inference, and designing heterogeneous CPU-GPU collaborative inference architectures.

Contact 📫: `xuduo_iat@mail.ustc.edu.cn`  
Phone 📱: `(+86) 173-9830-8282`  
GitHub 🐙: [https://github.com/blackwargreymonX](https://github.com/blackwargreymonX)  
Resume 📄: [PDF](/files/resume_xuduo.pdf)

<span class='anchor' id='news'></span>

# News 📰

- *2026.06* Completed Tencent Project Up work on Hunyuan Image 3.0/3.5 inference acceleration and service integration.
- *2026* First-author manuscript **Heterogeneous Collaborative Inference Architecture for Large Language Models** submitted to ICPADS 2026.
- *2026* Co-first-author manuscript **When Overlap Hurts: Closed-Form Scheduling Theory for Tensor-Parallel LLM Inference** submitted to EMNLP 2026.
- *2025.12* Deployed Two-Batch-Overlap vLLM communication-overlap optimization to TikTok Southeast Asia business during the Double 11 campaign.

<span class='anchor' id='education'></span>

# Education 🎓

- *2024.09 - Present* **University of Science and Technology of China**, Hefei, Anhui  
  M.Eng. Candidate, Computer Technology. Expected graduation: June 2027.
- *2020.09 - 2024.06* **Harbin Engineering University**, Harbin, Heilongjiang  
  B.Eng., Computer Science and Technology.

<span class='anchor' id='experience'></span>

# Experience 💼

<img src="/images/company-icons/tencent.svg" alt="Tencent logo" class="company-icon company-logo--wide"> **Tencent AI Infra, Project Up, Hunyuan Image Model Inference Acceleration, 2026.01 - 2026.06.**  
Migrated Hunyuan Image 3.0 inference to `vLLM 0.11.0` for reinforcement-learning-oriented training scenarios, covering model loading, request construction, generation parameter passing, output parsing, and service interface adaptation. Adapted the Hunyuan Image 3.5 text generation module to `vLLM 0.19.0`, refactoring tokenizer/processor logic, sampling configurations, batched request handling, and serving interfaces for large-scale online generation.

For image generation workloads, adapted the pipeline to `vLLM-Omni` to support complex multimodal inputs, long invocation chains, and image-related output processing. Used a plugin-style, non-intrusive adaptation strategy to reduce maintenance costs while completing accuracy alignment and end-to-end service integration.

![ByteDance logo](/images/company-icons/bytedance.svg){: .company-icon } **ByteDance Data, Two-Batch-Overlap vLLM Communication Overlap Optimization, 2025.09 - 2025.12.**  
Analyzed dense-model inference bottlenecks in a 2-card NVIDIA L20 PCIe Gen4 environment, where NCCL AllReduce accounted for 50%-55% of forward-pass time. Designed a Two-Batch Overlap mechanism based on `vLLM 0.11.0`, using inter-batch independence in Transformer inference to overlap computation and communication while preserving the original small-batch path.

Built a token-count-based batch-splitting strategy with over 95% load balance and memory alignment to multiples of 256. Designed an asymmetric dual-stream execution architecture with CPU-thread/GPU-stream synchronization, per-schedule event pools, cyclic signal chains, and `UBatchContext` state management. Under the 8K input scenario, throughput improved from 0.22 QPS to 0.29 QPS, a 31.1% increase; average latency dropped by 5.4% and P99 latency by 2.9%.

![Huawei logo](/images/company-icons/huawei.svg){: .company-icon } **Huawei 2012 Laboratories, Heterogeneous LLM Inference Framework, 2025.05 - 2025.08.**  
Proposed `xInfer`, a vLLM-based CPU-GPU collaborative inference architecture that decomposes LLM inference at the operator level. The system dynamically identifies compute-intensive and memory-intensive operators, keeps compute-heavy operators on GPU, and partially offloads bandwidth-sensitive attention operators to CPU for parallel execution.

Designed an asymmetric pipeline that alternates two mixed-computation batches across CPU and GPU, hiding cross-device transfer and computation latency while improving hardware utilization. On small-scale LLMs such as Llama3-8B, the asymmetric pipeline achieved a 1.18x throughput improvement.

<span class='anchor' id='publications'></span>

# Publications 📚

- **Heterogeneous Collaborative Inference Architecture for Large Language Models**  
  **Duo Xu**, Kunpeng Xu, Li Li. Submitted to ICPADS 2026. First author.
- **When Overlap Hurts: Closed-Form Scheduling Theory for Tensor-Parallel LLM Inference**  
  Kunpeng Xu, **Duo Xu**, Yuchen Wang, Li Li. Submitted to EMNLP 2026. Co-first author.

<span class='anchor' id='skills'></span>

# Technical Skills 🧠

- **LLM inference systems:** vLLM, KV cache management, continuous batching, PagedAttention, prefix caching, tensor parallelism, and model serving.
- **Performance optimization:** PyTorch Profiler, Perfetto, NCCL communication analysis, CUDA Runtime, CPU-GPU heterogeneous execution, asynchronous scheduling, and distributed debugging.
- **Engineering:** Python, C++, Shell, performance benchmarking, service integration, system-level experiment design, and large-model inference pipeline adaptation.
- **Models and frameworks:** Llama, Hunyuan Image, PyTorch, Transformers, LMDeploy, vLLM-Omni, and related inference frameworks.

<span class='anchor' id='interests'></span>

# Interests 🔍

- High-throughput and low-latency LLM serving systems
- Communication-computation overlap for tensor-parallel inference
- CPU-GPU heterogeneous inference and operator-level scheduling
- Multimodal generation serving with vLLM and vLLM-Omni
- Reinforcement-learning data generation and evaluation pipelines

<span class='anchor' id='additional'></span>

# Additional Experience 🧩

- Part-time Campus Ambassador: Yanfu Investments, Tencent, Taotian Group, Meituan.
