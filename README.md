<div align="center">
  <h1>Hi there, I'm Umang 👋</h1>
  <h3>GPU Systems & AI Compiler Engineer | High-Performance Computing (HPC)</h3>
  <p><i>I bridge the gap between Python's flexibility and Silicon's raw power. While others fine-tune models, I engineer the infrastructure they run on—squeezing every last FLOP out of GPUs.</i></p>
</div>

---

### ⚙️ What I Do
My core expertise lies in **Hardware-Software Co-Design**. I specialize in identifying severe memory bottlenecks in LLM inference pipelines and writing custom fused kernels to bypass them. I am currently transitioning from manual kernel engineering to automated **AI Compiler (MLIR)** development.

> **Current Focus:** Deep-diving into **MLIR** and reverse-engineering the OpenAI Triton backend to write custom compiler passes for automated IR-level optimizations.

---

### 🔥 Signature Projects & Open Source Impact

#### 1. Accelerated FP8 MoE Kernels for NVIDIA B200 (Blackwell)
*Developed for the global MLSys'26 FlashInfer-Bench Contest (NVIDIA Track).*
* **The Challenge:** Standard PyTorch MoE implementations suffer from extreme kernel launch starvation and memory-bound `aten::index_add_` reductions.
* **The Fix:** Engineered custom Fused FP8 (E4M3) GEMM kernels in **OpenAI Triton** and wrote custom **Atomic Scatter-Add** operations to bypass CPU dispatch latency.
* **The Result:** Hit **832 TFLOPS** peak throughput and achieved a **4.68x end-to-end speedup** over PyTorch BF16 on highly fragmented architectural configs (Grok/DeepSeek styles).

#### 2. Liger-Kernel (LinkedIn Open Source) | *Core Contributor*
*Optimizing enterprise-scale LLM serving infrastructure (15K+ Stars).*
* **The Fix:** Engineered an inference-optimized Fused RMSNorm kernel in Triton.
* **The Result:** Achieved a **24.6% throughput speedup** (126 → 157 tok/s) and eliminated **2.1 GB/s of redundant HBM traffic** by removing RSTD gradient state writes. Validated strictly via NVIDIA Nsight Compute profiling.

#### 3. NVIDIA RAPIDS (cuDF) | *Core Contributor*
*Accelerating GPU data science workflows (10K+ Stars).*
* **The Fix:** Reversed-engineered C++/Cython bindings (`.pxd`, `.pyx`) and authored a custom "Lazy Extraction" **CUDA C++** kernel to prevent token materialization during string splits.
* **The Result:** Achieved a **~160x execution speedup** (137ms → 0.85ms) on 10M+ row DataFrames with zero memory overhead. Merged into the main repository.

#### 4. LemonadeBench (AMD)
*Built for the AMD AI Developer Lemonade Challenge.*
* **Details:** An open-source profiling suite to benchmark Local AI workflows (NPU/iGPU). Connects to OpenAI-compatible APIs to automatically measure TTFT (Time To First Token) and TPS (Tokens Per Second) across varying FP16/INT4 quantizations.

---

### 🛠️ The Arsenal (Tech Stack)

| **Languages & Compilers** | **GPU Compute & Profiling** | **AI Infrastructure** |
| :--- | :--- | :--- |
| ![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white) | ![CUDA](https://img.shields.io/badge/CUDA_C%2B%2B-76B900?style=for-the-badge&logo=nvidia&logoColor=white) | ![PyTorch](https://img.shields.io/badge/PyTorch_Internals-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white) |
| ![Python](https://img.shields.io/badge/Python_3-3776AB?style=for-the-badge&logo=python&logoColor=white) | ![Triton](https://img.shields.io/badge/OpenAI_Triton-000000?style=for-the-badge&logo=openai&logoColor=white) | ![vLLM](https://img.shields.io/badge/vLLM_/_FlashInfer-blue?style=for-the-badge) |
| ![MLIR](https://img.shields.io/badge/LLVM_/_MLIR-8D0000?style=for-the-badge) | ![Nsight](https://img.shields.io/badge/NVIDIA_Nsight_Compute-76B900?style=for-the-badge&logo=nvidia&logoColor=white) | ![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black) |

---

### 🧠 Core Competencies (Under the Hood)
I don't just use libraries; I understand how they map to physical hardware.

* **GPU Architecture:** Memory Coalescing, Shared Memory Banking (avoiding conflicts), Warp Divergence, FP8 Tensor Cores utilization, Occupancy tuning.
* **Systems Engineering:** Intermediate Representations (TTIR/TTGIR), Kernel Fusion logic, Atomic Operations & Contention management.
* **Operating Systems:** Virtual Memory & Paging, Concurrency (Mutex/Deadlocks), Process vs Thread memory models.

---

<p align="center">
  <img src="https://github-readme-stats.vercel.io/api?username=Umang-projects&show_icons=true&theme=radical&hide_border=true&bg_color=0D1117" alt="Umang's Stats" />
</p>
