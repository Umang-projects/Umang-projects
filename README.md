### Hi there, I'm Umang 👋

#### **Systems Engineer | HPC & AI Infrastructure | NVIDIA RAPIDS Contributor**

I bridge the gap between **Python's flexibility** and **Hardware's raw power**. While others fine-tune models, I optimize the infrastructure they run on. My focus is squeezing every last FLOP out of GPUs by writing custom kernels in **CUDA C++** and **OpenAI Triton**.

---

### 🔥 Recent Impact: NVIDIA RAPIDS (cuDF)

I recently identified a critical memory bottleneck in **NVIDIA's cuDF library** (Pandas on GPU). Standard string splitting operations were causing massive memory pressure.

*   **Problem:** `split().get(n)` was materializing millions of unnecessary tokens.
*   **Solution:** Engineered a custom **Fused "Lazy Extraction" CUDA Kernel** using `CuPy` and `Cython` bindings.
*   **Result:** **~160x Speedup** (137ms → 0.85ms) on Tesla T4 GPUs with **Zero Memory Overhead**.
*   **Status:** Proposed and contributed the fix to `libcudf`.

---

### 🛠️ The Arsenal (Tech Stack)

| **Languages & Compute** | **AI & Deep Learning** | **Systems & Tools** |
| :--- | :--- | :--- |
| ![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white) | ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white) | ![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black) |
| ![CUDA](https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white) | ![Triton](https://img.shields.io/badge/OpenAI_Triton-000000?style=for-the-badge&logo=openai&logoColor=white) | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white) |
| ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) | ![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black) | ![Nsight](https://img.shields.io/badge/NVIDIA_Nsight-76B900?style=for-the-badge&logo=nvidia&logoColor=white) |
| ![Shell](https://img.shields.io/badge/Shell_Script-121011?style=for-the-badge&logo=gnu-bash&logoColor=white) | ![LLMs](https://img.shields.io/badge/LLMs-Llama_3.2-blue?style=for-the-badge) | ![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white) |

---

### 🧠 Core Competencies (Under the Hood)

I don't just use libraries; I understand how they work on the metal.

*   **GPU Architecture:** Memory Coalescing, Shared Memory Banking (avoiding conflicts), Warp Divergence, Tensor Cores, Occupancy tuning.
*   **Operating Systems:** Virtual Memory & Paging, Concurrency (Mutex/Semaphores/Deadlocks), Process vs Thread memory models.
*   **Model Optimization:** Kernel Fusion, KV-Cache Management (PagedAttention), Quantization (INT4/INT8), FlashAttention logic.

---

### 🚀 Engineering Highlights

| Project | Description | Impact |
| :--- | :--- | :--- |
| **FastInfer** | Custom CUDA inference backend for Llama-3.2 | **30.3 tokens/sec** on T4 GPU (Broken the 30TPS barrier) |
| **cudf-lazy-split** | Fused kernel for string extraction | **160x Speedup** vs Standard cuDF implementation |
| **Triton-Kernels** | Re-implementation of RMSNorm & MatMul | Benchmarking Python-based GPU programming vs Raw CUDA |
| **Hy-LoRA** | Hybrid SVD-LoRA fine-tuning strategy | **51%** reduction in trainable params with minimal accuracy loss |

---

<p align="center">
<img src="https://github-readme-stats.vercel.io/api?username=Umang-projects&show_icons=true&theme=radical&hide_border=true" alt="Umang's Stats" />
</p>
