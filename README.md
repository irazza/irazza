# Hi, I'm Alberto 👋

**PhD in Artificial Intelligence — Time Series | AI Engineer | Starting Postdoc in Reinforcement Learning**

I'm Alberto ([@irazza](https://github.com/irazza)), PhD in Artificial Intelligence (National PhD Programme in AI, 38th cycle — Politecnico di Torino, research carried out at the University of Verona). I work on time series under different aspects — distances, features, and evaluation — and I build fast, production-ready tools in **Rust + Python**. I spent 6 months at **Accenture as an AI Engineer for banking systems**, and I'm now starting a **postdoc in Reinforcement Learning**.

[![GitHub](https://img.shields.io/badge/GitHub-irazza-black?logo=github)](https://github.com/irazza)
[![ORCID](https://img.shields.io/badge/ORCID-0000--0001--5855--2295-a6ce39?logo=orcid)](https://orcid.org/0000-0001-5855-2295)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/albertoazzari/)
[![Google Scholar](https://img.shields.io/badge/Scholar-Publications-4285F4?logo=googlescholar)](https://scholar.google.com/citations?user=ag2t3wUAAAAJ&hl=it)
[![PhD Thesis](https://img.shields.io/badge/PhD%20Thesis-PDF-red?logo=adobeacrobatreader)](https://tesidottorato.depositolegale.it/bitstream/20.500.14242/364969/1/thesis.pdf)
[![LeetCode](https://img.shields.io/badge/LeetCode-albertoazzari-FFA116?logo=leetcode)](https://leetcode.com/u/albertoazzari/)

## 🔬 About me

- 🎓 **PhD in Artificial Intelligence** — National PhD Programme in AI (38th cycle), Politecnico di Torino / University of Verona
- ⏱️ Worked on time series from multiple angles: elastic distances, feature extraction, anomaly detection, statistical comparison
- 🏦 **AI Engineer @ Accenture (6 months)** — AI for banking systems
- 🚀 **Next: Postdoc in Reinforcement Learning** — scalable RL pipelines + model-based search for real-world problems (see below)
- 🦀 I love Rust for performance, Python for usability, and benchmarking everything against the state of the art

## 🚀 Main project: [tsdistances](https://github.com/irazza/tsdistances)

`tsdistances` is a **Python library with a Rust backend** for fast pairwise distances between sets of time series.

Fast, parallel, and GPU-accelerated — tested against [AEON](https://github.com/aeon-toolkit/aeon) for correctness and benchmarked on [UCR Archive](https://www.cs.ucr.edu/~eamonn/time_series_data_2018/) datasets.

**Features:**
- 13 distances: Euclidean, CATCH22-Euclidean, ERP, LCSS, DTW, DDTW, WDTW, WDDTW, ADTW, MSM, TWE, SBD, MPDist
- Parallel computation with Rayon (multi-core CPU)
- Optional GPU acceleration via Vulkan + [Rust-GPU](https://rust-gpu.github.io/) (`f32` on GPU vs `f64` on CPU)
- Python bindings via PyO3 + MATLAB bindings

```python
import numpy as np
import tsdistances

X = np.random.rand(10, 50)
D = tsdistances.dtw_distance(X, par=True, device='cpu')
```

```bash
pip install tsdistances
```

➡️ Repo: [github.com/irazza/tsdistances](https://github.com/irazza/tsdistances)

## 🧰 More of my work

- **[pycatch22-rs](https://github.com/irazza/pycatch22-rs)** — Blazing-fast Rust implementation of catch22 time-series features with Python bindings.
- **[cddiagram](https://github.com/irazza/cddiagram)** — Critical Difference diagrams for comparing classifiers across datasets (Python).
- **[if_stability](https://github.com/irazza/if_stability)** — Experiments on the stability of Isolation Forest results (S+SSPR paper + TKDE extension).
- **[tsdistances_gpu](https://github.com/irazza/tsdistances_gpu)** (now merged into `tsdistances/crates/tsdistances_gpu`) — SPIR-V / Vulkan compute kernels for elastic distances. Archived as standalone.

## 🧪 Postdoc direction — Reinforcement Learning

I'm starting a postdoc in RL focused on bringing RL to **real problems at scale**. Two main tracks:

**1. Scalability & RL pipelines (hands-on)**
Redesigning the RL stack in **JAX and/or C** to scale to real-world tasks. Key references:
- [JaxMARL](https://jaxmarl.foersterlab.com)
- [PufferLib / Puffer AI](https://puffer.ai)
- Goal: test what these solutions can deliver in terms of throughput/scale, with an eye toward a spin-off/startup.

**2. Model-based search à la AlphaGo (research)**
- [Mastering Go with deep nets + tree search (Nature 2016)](https://www.nature.com/articles/nature16961)
- [Mastering Go without human knowledge (Nature 2017)](https://www.nature.com/articles/nature24270)
- [AlphaGo documentary](https://www.youtube.com/watch?v=WXuK6gekU1Y)
- Despite their age, very few developments of this line exist on real problems. Goal: adapt it and evaluate in **shadow mode on real transmission grids** via collaborations with European TSOs — see e.g. recent work with RTE on power grids: [openreview.net/pdf?id=mpAMH1OyMO](https://openreview.net/pdf?id=mpAMH1OyMO).

Local experiments: see [muzero](https://github.com/irazza/muzero), [rl-exercises](https://github.com/irazza/rl-exercises), [rl-theory](https://github.com/irazza/rl-theory).

## 🛠️ Tech stack

`Rust` `Python` `JAX` `C` `PyTorch` `NumPy` `maturin` `PyO3` `Rayon` `Vulkan` `SPIR-V` `MATLAB`

## 📊 GitHub stats

![GitHub stats](https://github-readme-stats.vercel.app/api?username=irazza&show_icons=true&theme=default)
![Top langs](https://github-readme-stats.vercel.app/api/top-langs/?username=irazza&layout=compact)

## 📫 Contact

- GitHub: [@irazza](https://github.com/irazza)
- ORCID: [0000-0001-5855-2295](https://orcid.org/0000-0001-5855-2295)
- LinkedIn: [albertoazzari](https://www.linkedin.com/in/albertoazzari/)
- Google Scholar: [citations](https://scholar.google.com/citations?user=ag2t3wUAAAAJ&hl=it)
- LeetCode: [albertoazzari](https://leetcode.com/u/albertoazzari/)
