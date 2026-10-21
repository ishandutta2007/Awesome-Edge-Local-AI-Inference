# Awesome-Edge-Local-AI-Inference

## Top Edge & Local AI Inference Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on On-Device LLM Runtimes, Local API Servers & Edge ML Deployment*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Edge & Local AI Inference**. These tools enable running machine learning models—especially large language models—directly on consumer hardware, edge devices, and private infrastructure, eliminating cloud dependency for privacy, latency, and cost reasons.



**Examples** include Ollama, LM Studio, Jan.ai, LocalAI, GPT4All, llama.cpp, Exo, MLC LLM, Edge Impulse, and MediaPipe (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, custom model deployment, and transparent edge inference—ideal for developers, privacy-conscious users, and organizations building sovereign AI infrastructure. The open-source edge AI landscape spans universal LLM runtimes (llama.cpp, MLC LLM), distributed inference frameworks (Exo), and specialized edge ML platforms (MediaPipe, ExecuTorch, TensorFlow Lite Micro).



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Ollama (Cloud Tier)](https://ollama.com/)**  

  Primarily open-source local runtime, but offers an optional cloud tier for running models too large for local hardware. The desktop app (v0.10.0+) provides GUI access for macOS and Windows, while the core CLI remains the primary developer interface .



- **[LM Studio](https://lmstudio.ai/)**  

  Free desktop application (not fully open-source) for discovering, downloading, and running local LLMs via a polished GUI. Runs an OpenAI-compatible server while the app is open. Best-in-class in-app model catalog with hardware compatibility checks .



- **[Jan.ai](https://jan.ai/)**  

  Open-source desktop chat assistant with a privacy-first design. Provides a GUI for local inference via llama.cpp, with optional connections to hosted models (OpenAI, Anthropic). Includes a local Cortex server with OpenAI-compatible endpoints and MCP support .



- **[Edge Impulse (Enterprise)](https://www.edgeimpulse.com/)**  

  Commercial edge ML platform for building and deploying TinyML models to microcontrollers and edge devices. The Developer Plan is now free, including GPU training, advanced models (FOMO, YOLO-Pro), and production licensing . Enterprise adds dataset management, cloud integrations, and dedicated support.



- **[Google MediaPipe (Solutions/Tasks)](https://developers.google.com/mediapipe)**  

  Google's on-device ML framework for vision, text, and audio pipelines. While the framework is open-source, the primary development and documentation have moved to Google's platform with pre-built Tasks APIs for Android, iOS, Web, and Python .



## Open-Source GitHub Projects



- **[llama.cpp](https://github.com/ggml-org/llama.cpp)**  

  The foundational C/C++ inference engine for LLaMA-family models. Powers most local LLM tools (Ollama, LM Studio, Jan) under the hood. Supports CPU, GPU (CUDA, Metal, Vulkan), and exotic architectures via GGUF quantization. 96k+ stars .



- **[Ollama](https://github.com/ollama/ollama)**  

  The de facto standard for running local LLMs with minimal friction. One-line install, one-line model pull, automatic quantization and GPU acceleration. Exposes OpenAI-compatible API at `localhost:11434`. Cross-platform on macOS, Linux, and Windows . Best for developers and terminal-comfortable users.



- **[LocalAI](https://github.com/mudler/LocalAI)**  

  Drop-in OpenAI API replacement for self-hosted inference. Supports text generation, image generation (Stable Diffusion), text-to-speech, speech-to-text, and embeddings through a unified OpenAI-compatible API. Docker-friendly and ideal for backend services .



- **[GPT4All](https://github.com/nomic-ai/gpt4all)**  

  Beginner-friendly desktop application from Nomic AI. One-click model downloads, built-in LocalDocs for private RAG over your own files, and a clean chat UI. Particularly popular on Windows. Best for non-technical users who want private AI with document Q&A .



- **[Exo](https://github.com/exo-explore/exo)**  

  Open-source distributed AI inference framework that connects your devices (Mac Studio, Mac mini, MacBook) into a local cluster. Supports tensor parallelism via MLX backend, automatic device discovery, and RDMA over Thunderbolt 5 for near-zero latency. Can run 235B+ parameter models across 4 Mac Studios .



- **[MLC LLM](https://github.com/mlc-ai/mlc-llm)**  

  Universal LLM deployment engine powered by ML compilation. Runs models natively on iOS, Android, Web (WebGPU/WASM), Windows, Linux, and macOS across NVIDIA, AMD, Apple, and Intel GPUs. Provides OpenAI-compatible API via MLCEngine. 22k+ stars .



- **[ExecuTorch](https://github.com/pytorch/executorch)**  

  PyTorch's official on-device inference framework for mobile and edge AI. Optimized backends for iOS, Android, and embedded systems. Designed for deploying PyTorch models to resource-constrained devices .



- **[TensorFlow Lite Micro](https://github.com/tensorflow/tflite-micro)**  

  TensorFlow Lite for microcontrollers—ML inference on devices with kilobytes of memory. The standard for TinyML on Arduino, ESP32, and other MCUs .



- **[Whisper.cpp](https://github.com/ggml-org/whisper.cpp)**  

  Port of OpenAI's Whisper speech recognition model to C/C++ for CPU-only and embedded inference. Companion to llama.cpp from the same ggml ecosystem. 47k+ stars .



- **[MediaPipe Framework](https://github.com/google/mediapipe)**  

  Google's cross-platform on-device ML framework with graph-based computation (Packets, Graphs, Calculators). Provides pre-built Solutions/Tasks for hand landmarks (21 points), pose (33 points), face mesh, and object detection. Apache 2.0 licensed .



### Additional Strong Open-Source Options



- **TinyLlama** — 1.1B parameter model pre-trained on 3 trillion tokens, explicitly designed for edge and resource-constrained deployment .

- **text-generation-webui** — Popular open-source web UI for running LLMs locally with support for multiple backends (llama.cpp, Transformers, ExLlama) .

- **vLLM** — High-throughput serving engine optimized for concurrent requests. Overkill for single-user local use but essential for serving models to teams on local infrastructure .

- **Frameworks for building custom systems**: Combine **llama.cpp** as the inference core with **Ollama** for API management, **LocalAI** for multi-modal endpoints, and **Exo** for distributed multi-device setups. For edge vision tasks, pair **MediaPipe** with **ExecuTorch** for mobile deployment.



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
