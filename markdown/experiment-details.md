# Experiment Details

---

## Efficiency Evaluation

We provide a comparison between **WebNorm** and **AgenticNorm** in efficiency. AgenticNorm incurs much longer training and iteration time (about 19.2 minutes per round) than WebNorm (about 5 minutes), and its throughput is slightly lower because it learns a larger and more comprehensive set of invariants. We acknowledge this difference. However, both the training cost and runtime verification speed remain well within a practical range, and AgenticNorm still sustains **1.2 × 10³ logs/s**, which is sufficient for real-world deployment and remains faster than neural model-based detectors.

---

### Performance Comparison Table

| Item | WebNorm | Ours (AgenticNorm) |
|------|---------|-------------------|
| **Invariant Generation Time** | 4.3 min | 5.8 min |
| **One Round Iteration Time** | - | 19.4 min |
| **Total Training Time** | 4.3 min | 199.8 min |
| **Throughput** | 3.2 × 10³ logs/s | 1.2 × 10³ logs/s |


---

## 💡 Design Philosophy

Importantly, our **lightweight design** refers to **reduced dependencies** (no source code, no proprietary LLMs, no long-context prompts, no high reasoning requirements), **not** reduced computation time. Even with slightly higher verification cost, AgenticNorm becomes easy to deploy locally, privacy-preserving, and independent of heavy external infrastructure.

---


## 🔗 Related Pages

- [🏠 Home](index.md)
- [⚔️ Generated Attacks and Constraints](generated-attacks-and-constraints.md)
- [💾 Source Code and Dataset](source-code-and-dataset.md)
- [💡 Motivating Example](motivating-example.md)
- [📋 Detailed Prompts](detailed-prompts.md)

---

*For more details about the experimental methodology and complete results, please refer to our paper.*
