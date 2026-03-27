# SACD: Mitigating Implicit Semantic-Induced Hallucination via Strategy-Aware Adaptive Contrastive Decoding in Large Language Models 

Code for the CCS 2026 paper ”SACD: Mitigating Implicit Semantic-Induced Hallucination via Strategy-aware Adaptive Contrastive Decoding in Large Language Models“

## Overview
![Overview of SACD](https://github.com/WangMeiquan/SACD/raw/main/Overview%20of%20SACD.png)
  
  Large Language Models (LLMs) frequently exhibit hallucinations, producing outputs that appear plausible but are factually incorrect. Although contrastive decoding has recently been shown to be effective for hallucination mitigation, existing methods rely on fixed decoding parameters to enforce factual consistency, while ignoring the heterogeneous risks posed by implicit semantic strategies embedded in inputs. This critical limitation leads to substantial robustness degradation under specific semantic induction strategies. To tackle this issue, we define Implicit Semantic-Induced Hallucination (ISIH), a novel type of hallucination triggered by implicit semantic manipulation without exposing the inducing intent or disruption of the original task format. We further construct an ISIH benchmark covering three task categories, including reading comprehension, open-domain question answering, and contextual completion. Based on this benchmark, we design six implicit semantic induction strategies and propose a multi-level quantification framework to measure their induction strength and partition their risk levels. Furthermore, we propose Strategy-aware Adaptive Contrastive Decoding (SACD), which adaptively modulates the strength of factual consistency constraints according to the risk level of the input strategy. Experimental results demonstrate that SACD achieves significant performance gains on tasks demanding factual consistency and contextual faithfulness. Across various induction strategies, SACD exhibits more stable and robust decoding behavior, especially under high-risk strategies. Our work highlights the importance of risk-adaptive decoding and presents a general, strategy-aware solution for mitigating hallucinations in LLMs.

## Setup
```
- conda create -n SACD python=3.10
- conda activate SACD
- cd SACD
- pip install -r requirements.txt 
- pip install git+https://github.com/davidbau/baukit
- cd transformers
- pip install -e .
- cd experiments
```


## Requirements
- Python 3.x
- [列出你的依赖库，比如 PyTorch, Transformers 等]
- [其他环境要求]

## Reproduction Steps
1.  Install dependencies: `pip install -r requirements.txt`
2.  Run the main script: `python main.py`
3.  [详细的复现步骤，对应论文中的实验]

## File Structure
- `src/`: Source code
- `data/`: Experimental datasets
- `scripts/`: Reproduction scripts
- `results/`: Experimental results

## Notes
All artifacts are provided for double-blind review only.
