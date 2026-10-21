# Awesome-Edge-Local-AI-Inference

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/ishandutta2007/Awesome-Edge-Local-AI-Inference/pulls)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/ishandutta2007/Awesome-Edge-Local-AI-Inference)
[![GitHub Stars](https://img.shields.io/github/stars/ishandutta2007/Awesome-Edge-Local-AI-Inference?style=flat-square&logo=github)](https://github.com/ishandutta2007/Awesome-Edge-Local-AI-Inference/stargazers)

> **A curated, comprehensive catalog of enterprise SaaS solutions, hosted platforms, open-source runtimes, and TinyML frameworks for on-device and local AI inference.** Run cutting-edge Large Language Models (LLMs), multimodal vision networks, and speech models offline on consumer GPUs, Apple Silicon, embedded NPUs, and edge gateways—guaranteeing data sovereignty, zero API latency, and predictable compute costs.

---

## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [Edge AI Taxonomy & Architectural Matrix](#edge-ai-taxonomy--architectural-matrix)
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
  - [Universal LLM Inference Engines](#universal-llm-inference-engines)
  - [Desktop GUI & Turnkey Workstations](#desktop-gui--turnkey-workstations)
  - [High-Throughput Enterprise API Serving](#high-throughput-enterprise-api-serving)
  - [Distributed & Mesh Device Inference](#distributed--mesh-device-inference)
  - [Mobile, NPU & Embedded TinyML Runtimes](#mobile-npu--embedded-tinyml-runtimes)
  - [Hardware Compilers & Acceleration Toolkits](#hardware-compilers--acceleration-toolkits)
- [Hardware & Acceleration Compatibility](#hardware--acceleration-compatibility)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

---

## Sector Overview & Market Dynamics

The global Edge AI inference market is estimated at **$20.8 billion in 2024** and is projected to surpass **$100 billion by 2030** (growing at a ~26% CAGR), accelerated by escalating cloud inference costs, strict data sovereignty regulations (GDPR, HIPAA, AI Act), and ultra-low-latency on-device demands. The ecosystem exhibits a split structure: the underlying silicon and NPU layer is **highly concentrated** among major semiconductor leaders (NVIDIA, Qualcomm, Apple, AMD, Intel), whereas the software runtime, edge orchestration, and desktop inference tooling layer remains **moderately-to-highly fragmented** across diverse open engines, local frameworks, and cross-platform runtimes rather than a winner-take-all monopoly.

---

## Edge AI Taxonomy & Architectural Matrix

To help developers and enterprise architects choose the optimal edge runtime, tools are organized across four core architectural deployment paradigms:

| Architectural Tier | Primary Target Hardware | Representative Tools | Primary Use Case |
| :--- | :--- | :--- | :--- |
| **Turnkey Desktop Clients** | macOS, Windows, Linux workstations | Ollama, LM Studio, Jan, GPT4All | Private developer copilot, offline research, local RAG document Q&A |
| **High-Throughput Local Servers** | On-prem GPU nodes, edge servers | vLLM, SGLang, LocalAI, LiteLLM | Multi-tenant team API serving, production microservices, OpenAI drop-in replacement |
| **Distributed / Peer Mesh** | Mixed Apple Silicon, consumer PCs | Exo | Running giant 70B–405B parameter models partitioned across local LAN devices |
| **Embedded & Mobile TinyML** | Microcontrollers, iOS/Android, NPUs | ExecuTorch, MediaPipe, TF Lite Micro, Candle | On-device computer vision, real-time sensor processing, edge audio transcription |

---

## SaaS/Hosted Platforms

| Platform | Company / Backer | Valuation / Revenue | Pricing (Starting Tier) | Free Tier Limits | Key Edge / Local Features |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **[Google MediaPipe](https://developers.google.com/mediapipe)** | Alphabet Inc. (Google) | **$2.14T Valuation** / $350B+ Revenue | **$0** (Client SDKs free; Cloud endpoints start at $0.0001/1K chars) | **Forever free** on-device SDK with unlimited local client execution; 90-day $300 credit trial for Google Cloud APIs | Pre-built vision & audio task pipelines (Hand landmarks, Pose, Face mesh, Object detection) optimized for mobile and web |
| **[Edge Impulse](https://www.edgeimpulse.com/)** | Qualcomm | **$195B Parent MCap** ($234M Series B) / $15M ARR | **$39/month** (Pro seat / Enterprise fleet from $500/mo) | **Forever free** Developer Plan with 60 min compute time per training job, 3 private projects, GPU acceleration, and commercial license | TinyML & edge ML development studio, FOMO/YOLO-Pro model optimization, direct firmware deployment for MCUs and NPUs |
| **[Ollama (Cloud Tier)](https://ollama.com/)** | Ollama Inc. (Benchmark / Theory) | **~$600M Valuation** ($88M raised) / ~$15M ARR | **$20/month** (Ollama Cloud Pro with $60 monthly token credits; Max $100/mo) | **Forever free** local CLI runtime with unlimited on-device inference; Cloud tier offers free tier with 1 concurrent request | Zero-config local LLM runner (`localhost:11434`), hybrid cloud fallback, cross-platform GGUF quantization, and OpenAI API compatibility |
| **[Roboflow](https://roboflow.com/)** | Roboflow (Craft / YC) | **$200M Valuation** ($64M raised) / ~$12M ARR | **$79/month** (Core plan with dedicated team credits) | **Forever free** starter tier with 10 monthly credits (~30 cloud trainings, ~10,000 auto-labeled images, or ~80k inferences) and local export | Vision AI dataset management, edge model deployment via Roboflow Inference container, auto-labeling, and active learning |
| **[LM Studio](https://lmstudio.ai/)** | Element Labs (Google / Conviction) | **~$80M Valuation** ($19.3M raised) / ~$1.8M ARR | **$20/month** (Bionic+ tier; Pro at $100/mo) | **Forever free** desktop app for personal & commercial use with unlimited local inference; Bionic free tier for agent sync | Polished desktop UI, hardware compatibility calculator, local OpenAI-compatible server, in-app Hugging Face model discovery |
| **[Jan.ai](https://jan.ai/)** | Menlo Research | **~$5M Valuation** / ~$1.2M ARR | **$24 one-time** (Offline dictation add-on; BYO API keys for hosted models) | **Forever free** open-source local desktop runtime (Apache 2.0 / AGPL-3.0) with unlimited offline inferences | Privacy-first local assistant, local Cortex engine with OpenAI-compatible endpoints, MCP server support, and local RAG |



## Open-Source GitHub Projects

- **[Ollama](https://github.com/ollama/ollama)** [![Stars](https://img.shields.io/github/stars/ollama/ollama?style=social&color=white)](https://github.com/ollama/ollama/stargazers)  
  The de facto standard for running local LLMs with minimal friction. Features one-line model pull, automatic quantization, and GPU acceleration. Exposes an OpenAI-compatible API at `localhost:11434` with cross-platform support across macOS, Linux, and Windows.

- **[Open WebUI](https://github.com/open-webui/open-webui)** [![Stars](https://img.shields.io/github/stars/open-webui/open-webui?style=social&color=white)](https://github.com/open-webui/open-webui/stargazers)  
  Extensible, feature-rich, and self-hosted AI interface designed to operate entirely offline. Offers first-class native integration with Ollama and OpenAI-compatible local APIs, multi-model chat, local RAG pipelines, and granular user role management.

- **[llama.cpp](https://github.com/ggml-org/llama.cpp)** [![Stars](https://img.shields.io/github/stars/ggml-org/llama.cpp?style=social&color=white)](https://github.com/ggml-org/llama.cpp/stargazers)  
  The foundational pure C/C++ inference engine for LLaMA, Mistral, Gemma, and hundreds of other architectures. Serves as the high-performance backbone powering Ollama, LM Studio, and Jan. Supports CUDA, Apple Metal, Vulkan, SYCL, and extreme GGUF quantization.

- **[vLLM](https://github.com/vllm-project/vllm)** [![Stars](https://img.shields.io/github/stars/vllm-project/vllm?style=social&color=white)](https://github.com/vllm-project/vllm/stargazers)  
  High-throughput, memory-efficient LLM serving engine featuring PagedAttention algorithm. The gold standard for self-hosting high-concurrency local inference on private enterprise servers and edge workstations with continuous batching.

- **[GPT4All](https://github.com/nomic-ai/gpt4all)** [![Stars](https://img.shields.io/github/stars/nomic-ai/gpt4all?style=social&color=white)](https://github.com/nomic-ai/gpt4all/stargazers)  
  Privacy-first desktop ecosystem from Nomic AI. Delivers one-click model downloads, built-in LocalDocs for private RAG over local documents, and a turnkey chat UI without any telemetry or GPU requirements.

- **[LiteLLM](https://github.com/BerriAI/litellm)** [![Stars](https://img.shields.io/github/stars/BerriAI/litellm?style=social&color=white)](https://github.com/BerriAI/litellm/stargazers)  
  Lightweight proxy gateway to call 100+ LLMs using the standardized OpenAI input/output format. Seamlessly routes requests across local backends (Ollama, vLLM, LocalAI) and cloud providers with built-in fallbacks, rate limiting, and spend tracking.

- **[Whisper.cpp](https://github.com/ggml-org/whisper.cpp)** [![Stars](https://img.shields.io/github/stars/ggml-org/whisper.cpp?style=social&color=white)](https://github.com/ggml-org/whisper.cpp/stargazers)  
  High-performance C/C++ port of OpenAI's Whisper automatic speech recognition model. Provides zero-memory-allocation, CPU/GPU accelerated on-device transcription for desktops, mobile devices, and embedded hardware.

- **[LocalAI](https://github.com/mudler/LocalAI)** [![Stars](https://img.shields.io/github/stars/mudler/LocalAI?style=social&color=white)](https://github.com/mudler/LocalAI/stargazers)  
  Drop-in OpenAI API replacement for self-hosted community AI. Supports text generation, Stable Diffusion image synthesis, whisper audio transcription, text-to-speech, and vector embeddings through a unified REST container.

- **[Exo](https://github.com/exo-explore/exo)** [![Stars](https://img.shields.io/github/stars/exo-explore/exo?style=social&color=white)](https://github.com/exo-explore/exo/stargazers)  
  Decentralized distributed AI inference framework that clusters everyday consumer devices (MacBooks, Mac Minis, PCs) into an elastic compute mesh. Leverages peer-to-peer discovery and tensor parallelism to run frontier 70B–405B models locally.

- **[text-generation-webui](https://github.com/oobabooga/text-generation-webui)** [![Stars](https://img.shields.io/github/stars/oobabooga/text-generation-webui?style=social&color=white)](https://github.com/oobabooga/text-generation-webui/stargazers)  
  The Swiss Army knife Gradio interface for running large language models locally. Supports multiple backends including transformers, llama.cpp, ExLlamaV2, AutoGPTQ, and TensorRT-LLM with extension support for LoRA training and character cards.

- **[SGLang](https://github.com/sgl-project/sglang)** [![Stars](https://img.shields.io/github/stars/sgl-project/sglang?style=social&color=white)](https://github.com/sgl-project/sglang/stargazers)  
  Fast serving framework designed for complex LLM programs and structured generation. Integrates RadixAttention for automatic KV cache reuse across multi-turn chats, few-shot prompting, and reasoning agent workflows.

- **[MediaPipe Framework](https://github.com/google-ai-edge/mediapipe)** [![Stars](https://img.shields.io/github/stars/google-ai-edge/mediapipe?style=social&color=white)](https://github.com/google-ai-edge/mediapipe/stargazers)  
  Google's cross-platform on-device machine learning framework with graph-based computation pipelines. Provides production-ready models for real-time 3D hand tracking, face mesh, body pose estimation, and mobile object detection.

- **[MLX](https://github.com/ml-explore/mlx)** [![Stars](https://img.shields.io/github/stars/ml-explore/mlx?style=social&color=white)](https://github.com/ml-explore/mlx/stargazers)  
  Array framework designed specifically for machine learning on Apple Silicon, engineered by Apple machine learning research. Features unified memory access, lazy computation, and multi-device capabilities for high-speed local inference.

- **[llamafile](https://github.com/mozilla-ai/llamafile)** [![Stars](https://img.shields.io/github/stars/mozilla-ai/llamafile?style=social&color=white)](https://github.com/mozilla-ai/llamafile/stargazers)  
  Mozilla's open-source initiative that turns LLM weights into single multi-OS executable binaries. Runs on six operating systems (macOS, Windows, Linux, FreeBSD, NetBSD, OpenBSD) without installation or external runtimes.

- **[MLC LLM](https://github.com/mlc-ai/mlc-llm)** [![Stars](https://img.shields.io/github/stars/mlc-ai/mlc-llm?style=social&color=white)](https://github.com/mlc-ai/mlc-llm/stargazers)  
  Universal deployment engine powered by machine learning compiler technology (Apache TVM Unity). Executes cross-platform native LLMs on iOS, Android, WebGPU in-browser, Windows, Linux, and macOS with unified Vulkan and Metal acceleration.

- **[ONNX Runtime](https://github.com/microsoft/onnxruntime)** [![Stars](https://img.shields.io/github/stars/microsoft/onnxruntime?style=social&color=white)](https://github.com/microsoft/onnxruntime/stargazers)  
  Cross-platform, high-performance scoring engine for Open Neural Network Exchange models by Microsoft. Accelerates inference across diverse hardware execution providers including DirectML, OpenVINO, CUDA, TensorRT, and CoreML.

- **[Candle](https://github.com/huggingface/candle)** [![Stars](https://img.shields.io/github/stars/huggingface/candle?style=social&color=white)](https://github.com/huggingface/candle/stargazers)  
  Minimalist, lightweight ML framework for Rust built by Hugging Face. Focuses on performance, memory footprint minimization, and zero-overhead deployments on resource-limited IoT and WASM edge environments.

- **[Apache TVM](https://github.com/apache/tvm)** [![Stars](https://img.shields.io/github/stars/apache/tvm?style=social&color=white)](https://github.com/apache/tvm/stargazers)  
  End-to-end open-source machine learning compiler framework for CPUs, GPUs, and specialized edge accelerators. Compiles deep learning models into ultra-efficient bare-metal machine code.

- **[OpenVINO](https://github.com/openvinotoolkit/openvino)** [![Stars](https://img.shields.io/github/stars/openvinotoolkit/openvino?style=social&color=white)](https://github.com/openvinotoolkit/openvino/stargazers)  
  Intel's open-source toolkit for optimizing and deploying deep learning models on Intel CPUs, integrated GPUs, discrete GPUs, and specialized NPUs with zero cloud latency.

- **[ExecuTorch](https://github.com/pytorch/executorch)** [![Stars](https://img.shields.io/github/stars/pytorch/executorch?style=social&color=white)](https://github.com/pytorch/executorch/stargazers)  
  PyTorch's official end-to-end on-device inference runtime for mobile and edge devices. Delivers a compact footprint, modular execution backends, and hardware acceleration for iOS, Android, and embedded Linux.

- **[ExLlamaV2](https://github.com/turboderp-org/exllamav2)** [![Stars](https://img.shields.io/github/stars/turboderp-org/exllamav2?style=social&color=white)](https://github.com/turboderp-org/exllamav2/stargazers)  
  Fastest local inference library for consumer NVIDIA GPUs, designed from scratch to maximize throughput with custom EXL2 quantization, speculative decoding, and low VRAM footprint.

- **[TensorFlow Lite Micro](https://github.com/tensorflow/tflite-micro)** [![Stars](https://img.shields.io/github/stars/tensorflow/tflite-micro?style=social&color=white)](https://github.com/tensorflow/tflite-micro/stargazers)  
  Lightweight runtime tailored for TinyML inference on microcontrollers, DSPs, and embedded microprocessors with as little as a few tens of kilobytes of memory (ARM Cortex-M, ESP32, Arduino).



## Hardware & Acceleration Compatibility

| Hardware Ecosystem | Supported Acceleration APIs | Recommended Runtime Stack | Typical Latency / Throughput Profile |
| :--- | :--- | :--- | :--- |
| **NVIDIA RTX / Workstation GPUs** | CUDA, TensorRT, FlashAttention-2/3 | vLLM, SGLang, ExLlamaV2, llama.cpp | Maximum tokens/sec, full precision & EXL2/AWQ quantization |
| **Apple Silicon (M1/M2/M3/M4)** | Metal, Accelerate, MLX | llama.cpp (Metal), MLX, Exo | Exceptional memory bandwidth, zero unified memory copy overhead |
| **AMD Radeon / Instinct GPUs** | ROCm, Vulkan, DirectML | llama.cpp, MLC LLM, vLLM (ROCm) | High compute density, open compute runtime |
| **Intel Core / ARC / Xeon / NPU** | OpenVINO, SYCL, oneAPI | OpenVINO, llama.cpp (SYCL), ONNX Runtime | Optimized on-chip NPU and integrated Iris Xe/Arc GPU offloading |
| **Qualcomm Snapdragon / Hexagon NPU** | QNN, ONNX, MediaPipe | Qualcomm AI Hub, ExecuTorch, MediaPipe | Ultra-low power mobile AI, on-device vision and speech |
| **ARM Cortex-M & Embedded MCUs** | CMSIS-NN, Ethos-U | TensorFlow Lite Micro, Edge Impulse | Kilobyte-memory footprint, sub-milliwatt real-time inference |

---

## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Local inference performance varies significantly by hardware (VRAM, memory bandwidth, quantization support); benchmark before committing to a stack.

- Self-hosted inference servers should be secured behind a reverse proxy with authentication if exposed beyond localhost .



---



**Made for developers, privacy advocates, edge AI engineers, and organizations building sovereign AI infrastructure.**  

Let's make AI inference more local, private, and accessible.
