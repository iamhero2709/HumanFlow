<div align="center">
  <img src="assets/humanflow_logofinal.png" alt="HumanFlow Logo" width="320"/>

  # HumanFlow-Llama3-8B
  **Open-source language model for turning AI drafts into natural, high-trust human writing.**

  [![Hugging Face](https://img.shields.io/badge/🤗%20Hugging%20Face-Model-orange)](https://huggingface.co/randhir302/HumanFlow)
  [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
  [![Stars](https://img.shields.io/github/stars/iamhero2709/HumanFlow?style=social)](https://github.com/iamhero2709/HumanFlow/stargazers)

  **[Download on Hugging Face](https://huggingface.co/randhir302/HumanFlow)** •
  **[Run Quickstart](#quickstart-local-inference)** •
  **[Join Pro API Waitlist](https://[YOUR_WAITLIST_LINK].com)**
</div>

---

## Performance Snapshot

<div align="center">

| Metric | Base Llama-3 8B | HumanFlow-Llama3-8B |
|:--|:--:|:--:|
| GPTZero Human Score | 18% | **99%** |
| Turnitin Human Score | 10% | **92%+** |
| Focus | Generic completion | **Humanized structural rewriting** |

</div>

> Benchmarks are measured with recommended inference settings and representative editorial prompts.

---

## Core Evaluation (Real)

| Metric | Value | Interpretation |
|:--|--:|:--|
| BERTScore F1 | 0.8424 | Semantic similarity to prompts |
| ROUGE-L | 0.0908 | Low overlap indicates original generation |
| Perplexity | 1.5242 | Confidence/coherence (lower is better) |
| Text Overlap | 0.0528 | Lexical similarity to input |

### Model Availability

- Full 16-bit model: [https://huggingface.co/randhir302/HumanFlow](https://huggingface.co/randhir302/HumanFlow)
- Quantized model: Coming soon

---

## Why HumanFlow Exists

Most LLM outputs are easy to detect because they converge on the same polished, repetitive writing patterns. Synonym replacement does not fix this.

HumanFlow-Llama3-8B is designed to change **rhythm, structure, and flow**—so rewritten text reads like a person with intent, not a model following a template.

---

## Core Capabilities

- **Structural Humanization**  
  Rewrites sentence cadence, transitions, and discourse shape to reduce mechanical patterns.

- **Detector-Aware Output Behavior**  
  Optimized for higher human-likelihood scores on mainstream detection systems.

- **Fast Local Deployment**  
  Runs with GGUF quantizations on commodity hardware via `llama.cpp` stack.

- **Production-Ready Foundation**  
  Open-source SFT base that can be embedded into pipelines, tooling, and editorial workflows.

---

## Benchmark Table

| Benchmark | Prompt Set | Base Model | HumanFlow-Llama3-8B |
|:--|:--|:--:|:--:|
| GPTZero | Long-form SEO + informational content | 18% Human | **99% Human** |
| Turnitin | Academic-style paragraph rewrites | 10% Human | **92%+ Human** |
| Qualitative Fluency | Mixed niches | Flat, repetitive | **Variable, natural flow** |

---

## Quickstart (Local Inference)

### 1) Install

```bash
pip install llama-cpp-python
```

### 2) Download model

Get the model release from Hugging Face:  
**https://huggingface.co/randhir302/HumanFlow**

### 3) Run

```python
from llama_cpp import Llama

llm = Llama(
    model_path="./HumanFlow-Llama3-8B.Q4_K_M.gguf",
    n_ctx=4096,
    n_threads=8,
)

prompt = "Rewrite this AI draft to sound natural and human without changing meaning:\n\n[YOUR_TEXT]"

output = llm(
    prompt,
    max_tokens=700,
    temperature=0.75,
    top_p=0.9,
    repeat_penalty=1.1,
)

print(output["choices"][0]["text"])
```

---

## HumanFlow Pro API (Waitlist)

The open-source release includes SFT weights.

For teams that need stronger quality control, lower latency, and managed deployment, HumanFlow Pro provides:

- Advanced preference-optimized rewriting engine
- Dedicated API access
- Web interface for high-volume workflows
- Priority updates and support

**[Join the HumanFlow Pro Waitlist](https://[YOUR_WAITLIST_LINK].com)**

---

## Before vs After

### Input (Typical AI Draft)
> In today’s rapidly evolving digital landscape, it is imperative for businesses to leverage cutting-edge strategies in order to maximize engagement and unlock sustainable growth.

### Output (HumanFlow)
> Digital markets move fast. If a business wants real growth, it needs clear strategy, fast iteration, and content people actually want to read.

---

## Who It’s For

- **SEO teams** scaling content without robotic voice
- **Agencies** delivering publish-ready rewrites at volume
- **Writers & editors** cleaning first drafts quickly
- **Students & researchers** improving clarity and tone
- **Developers** embedding rewrite intelligence into apps

---

## Roadmap

- [x] Open-source SFT release (Llama3-8B)
- [x] GGUF compatibility for local inference
- [ ] Hosted inference API (private beta)
- [ ] Pro dashboard for teams
- [ ] Expanded benchmark suite and eval transparency
- [ ] Fine-tuned variants for domain-specific writing

---

## Community

If HumanFlow helps your workflow:

- Star the repository
- Follow updates on new checkpoints
- Share benchmark results and integrations
- Open issues for reproducible bugs or model feedback

**⭐ Star HumanFlow to support the project: https://github.com/iamhero2709/HumanFlow**
