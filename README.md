# AI Computer Cookbook

**A curated list of resources, links, and materials for making your very own open-source AI computer.**

## Contents

- [Inference engines](#inference-engines)
- [Models](#models)
- [Agentic memory systems](#agentic-memory-systems)
- [Agent harnesses](#agent-harnesses)
- [Interfaces](#interfaces)
- [Builds](#builds)

## Inference engines
- [llama.cpp](https://github.com/ggml-org/llama.cpp)
- [vLLM](https://vllm.ai/)
- [Llamafile](https://llamafile.ai/)
- [Ollama](https://ollama.com/)
- [TensorFold](https://github.com/ashhart/TensorFold)
- [Halogen](https://github.com/peonist-ai/halogen-flash-server)
- [Strata](https://github.com/Niko1221/Strata)
- [Mia's AI Lab](https://mia-ai.net/) (useful recipes for getting models running on Nvidia Spark and RTX)

## Models
- [GLM 5.3 Flash](https://huggingface.co/zai-org/GLM-5.3-Flash)
- [DeepSeek 4.1 Flash 1017](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash-1017)
- [Qwen 3.8 Flash Next](https://huggingface.co/Qwen/Qwen3.8-Flash-Next)
- [Nemotron 3.5 Lightning](https://huggingface.co/nvidia/NVIDIA-Nemotron-3.5-Lightning-30B-A3B-NVFP4)
- [Nemotron 3.5 Bolt](https://huggingface.co/nvidia/NVIDIA-Nemotron-3.5-Bolt-74B-A9B-24GB)
- [Inkling](https://huggingface.co/thinkingmachines/Inkling)
- [Muse Glimmer](https://huggingface.co/meta-models/Muse-Glimmer-30B)
- [Gemma 4](https://huggingface.co/google/gemma-4-31B-it)

## Agentic memory systems
- [Honcho](https://honcho.dev/)
- [GBrain](https://gbrain.io/)
- [mem0](https://mem0.ai/)
- [OpenViking](https://github.com/volcengine/OpenViking)
- [Solstone](https://solstone.app/)
- [Hindsight](https://github.com/vectorize-io/hindsight)
  
## Agent harnesses
- [Hermes Agent](https://hermes-agent.nousresearch.com/)
- [OpenClaw](https://openclaw.ai/)
- [NanoClaw](https://nanoclaw.dev/)
- [Pi](https://pi.dev/)
- [OpenCode](https://opencode.ai/)
- [Thunderbolt](https://www.thunderbolt.io/)

## Interfaces
- [Television](https://television.run)
- [Hermes Desktop](https://hermes-agent.nousresearch.com/desktop)

## Builds
These are example configurations for AI PCs.

### The Beast
- In a nutshell: dedicated GPU hardware and large amounts of RAM (either VRAM or unified RAM), enabling you to run large, frontier-class models locally.
- Hardware:
-   Nvidia DGX Spark, Nvidia RTX 3000/4000/5000 series cards (likely multiple), or AMD Strix Halo.
-   Ideally paired with a dedicated separate machine to run the agent (so that it doesn't eat into available RAM for inference).
-   A large amount of storage (2-4 TB+) to store large model weights.

### The Mac
- In a nutshell: use the MacBook or Mac Mini you already have to run smaller but capable models locally, preserving your privacy and control.
- Hardware:
-   Apple Silicon (M1+) MacBook Air, MacBook Pro, Mac Mini, or iMac with at least 24GB of unified RAM.
- Notes:
-   If you use a laptop, your agent will shut down when you close the lid.
-   Be extremely cautious when running an agent harness on your primary machine. Recommend running in a container and ensuring that any "yolo mode" is turned off.

### The Droplet
- In a nutshell: run your agent and your model in the cloud, avoiding the need to manage any hardware at all.
- Services:
-   Cloud VPS: Use DigitalOcean, Hetzner, or other VPS server to run your agent harness; many offer a one-click setup option for this.
-   Cloud inference: Use a provider like Fireworks.AI, Cerebras, Modal, or Together.AI to provide inference on the cloud model of your choice.
- Notes:
-   Set maximum spending caps for your cloud inference providers, or look for a provider who offers a flat monthly subscription rate; you don't want to get caught by surprise with a big bill if your agent uses a lot of tokens.

### The Raspberry Pi
- In a nutshell: yes, you can use one of the world's cheapest computers as an AI personal computer, with a few compromises.
- Hardware:
-   Raspberry Pi 4 or higher.
- Services:
-   A cloud inference provider, as above.
- Notes:
-   Very small (<1B parameters) models exist that will run on Raspis, but they are very slow and have limited capabilities.
-   The Raspi has a GPU but getting it to work can be difficult; expect that any inference you run locally will be CPU-based.
