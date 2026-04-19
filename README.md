<div align="center">
  <img src="assets/logo.png" alt="HumanFlow Logo" width="400"/>

  <h1>🌊 HumanFlow-Llama3-8B</h1>
  <p><b>The Antidote to Robotic AI Text.</b></p>

  <a href="https://huggingface.co/[YOUR_USERNAME]/HumanFlow-Llama3-8B-GGUF"><img src="https://img.shields.io/badge/🤗%20Hugging%20Face-Models-orange"/></a>
  <a href="https://colab.research.google.com/drive/[YOUR_COLAB_LINK]"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-Apache%202.0-blue.svg"/></a>
</div>

<br/>

Standard LLMs are exhausted. They use words like *"delve"*, *"tapestry"*, and *"imperative"* while maintaining a highly predictable, mechanical sentence structure. Prompt engineering isn't enough to bypass advanced AI detectors or make the text readable for actual humans.

**HumanFlow** is a custom-trained Llama-3 8B model engineered specifically to strip out RLHF alignment artifacts and rewrite AI-generated drafts with human-like burstiness, perplexity, and natural cognitive flow.

---

## 🚀 The 99% Bypass Benchmark

We don't just swap synonyms. HumanFlow manipulates structural perplexity to achieve passing scores on enterprise AI detectors. 

| Detector | Base Llama-3 | HumanFlow SFT |
| :--- | :--- | :--- |
| **GPTZero** | 18% Human | **99% Human** |
| **Turnitin** | 10% Human | **92%+ Human** |

*(Note: These benchmarks require the specific inference parameters outlined below).*

---

## 🏢 Enterprise DPO API & Web SaaS (Waitlist)

**This repository contains the Open-Source SFT (Supervised Fine-Tuning) weights.** While the SFT model is excellent for local execution, we have built a **Private DPO (Direct Preference Optimization) Engine** that is significantly stronger, understands complex domain context, and operates at blistering speeds via our dedicated inference API.

If you are an agency, SEO team, or developer tired of robotic output, get access to the HumanFlow Web App and API:

👉 **[Join the HumanFlow Pro Waitlist Here](https://[YOUR_WAITLIST_LINK].com)**

---

## 💻 Quickstart (Local Inference)

We highly recommend using the GGUF quantized models for efficient CPU/GPU inference.

### 1. Install Dependencies
```bash
pip install llama-cpp-python
