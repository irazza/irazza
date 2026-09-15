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

## 🎓 PhD thesis

### [On Mining Time Series Data with Random Forest Models: Perspectives from Classification, Anomaly Detection, and Distance Measures](https://tesidottorato.depositolegale.it/bitstream/20.500.14242/364969/1/thesis.pdf)

*Doctoral Program in Artificial Intelligence (38th cycle) — University of Verona & Politecnico di Torino, 2026.*
*Supervisor: Prof. Pietro Sala. Co-supervisors: Prof. Manuele Bicego, Prof. Carlo Combi.*

Random Forests are a cornerstone of tabular data analysis — robust, interpretable, and effective on small datasets — yet their adaptation to the temporal domain is still largely unexplored. The thesis pushes forest-based models into time series along four complementary directions, using **intraoperative motor evoked potentials (MEPs)** recorded during neurosurgery as a demanding real-world case study, while keeping the proposed methods general.

**1. Classification of intraoperative MEPs**
Built a dedicated dataset from intraoperative recordings and systematically evaluated classifiers × signal representations. Random Forest on TSFRESH features reached **93%** accuracy on two-muscle, **83%** on four-muscle, and **78%** on the hardest six-muscle mixed-protocol task — against **47.4 ± 11.9%** for ten expert neurophysiologists on the same signals.
→ *Computers in Biology and Medicine* (2024); oral presentation at EANS.

**2. CISOF — anomaly detection and *early* detection**
Proposed the Canonical Isolation Tree/Forest, the first extension of the Isolation Forest principle to time series where the anomaly affects the whole sequence, plus a formulation for detecting anomalies *before* they fully manifest. Fully unsupervised and patient-specific: it only needs the baseline acquired at the start of the procedure. Mean ROC-AUC **0.844** on detection and **0.667** on early detection, beating every competitor (IForest, OC-SVM, SOD, LOF-cDTW, HBOS, ECOD, MCD) with statistically significant gains (Wilcoxon signed-rank).
→ Submitted to *Journal of Healthcare Informatics Research*; patent application filed.

**3. TSRF-Dist — a novel forest-based time series distance**
A distance derived from **Extremely Randomized Canonical Interval Forests**, transposing Random Forest–based distances (RatioRF, Zhu) to the temporal domain. On the UCR archive it ranks **first overall**, with mean ARI **0.36 / 0.27 / 0.31** across the three dataset groups versus **0.19 / 0.13 / 0.23** for the best classical elastic distances (DTW, cDTW, MSM, TWE, ERP, …) — the gap over the runner-up is statistically significant.
→ *Data Mining and Knowledge Discovery* 39:27 (2025), [doi:10.1007/s10618-025-01098-3](https://doi.org/10.1007/s10618-025-01098-3)

**4. [tsdistances](https://github.com/irazza/tsdistances) — making all of this usable at scale**
A Python library with a Rust backend implementing elastic distances with wavefront (anti-diagonal SIMD) dynamic programming, tiling, and GPU kernels. **5.25×** faster with multi-core CPU and **26.59×** with GPU over the single-threaded baseline; on a single thread it is the fastest CPU implementation on every one of the 23 benchmark datasets, ~**2.3×** faster than `aeon` and **24%** faster than the highly optimized C++ DTAI — with GPU `f32` results deviating at most **0.67%** from the `f64` CPU reference.
→ *ACM Transactions on Mathematical Software*, [doi:10.1145/3802579](https://doi.org/10.1145/3802579)

📄 [Read the thesis (PDF)](https://tesidottorato.depositolegale.it/bitstream/20.500.14242/364969/1/thesis.pdf) · [record page](https://tesidottorato.depositolegale.it/handle/20.500.14242/364969)

## 📚 Selected publications

- **TSRF-Dist: a novel time series distance based on extremely randomized canonical interval forests** — A. Azzari, M. Bicego, C. Combi, et al. *Data Mining and Knowledge Discovery* 39:27 (2025). [doi:10.1007/s10618-025-01098-3](https://doi.org/10.1007/s10618-025-01098-3)
- **tsdistances: a high-performance Python library for time series distances with GPU support** — A. Azzari, et al. *ACM Transactions on Mathematical Software*. [doi:10.1145/3802579](https://doi.org/10.1145/3802579)
- **Machine learning allows expert level classification of intraoperative motor evoked potentials during neurosurgical procedures** — A. Boaro, A. Azzari, F. Basaldella, et al. *Computers in Biology and Medicine* 180:109032 (2024). [doi:10.1016/j.compbiomed.2024.109032](https://doi.org/10.1016/j.compbiomed.2024.109032)
- **Machine learning approaches for the automated classification of intraoperative motor evoked potentials. A pilot study** — A. Boaro, A. Azzari, S. Nunes, et al. *Brain and Spine* 2:101359 (2022).
- **An empirical characterization of the stability of isolation forest results** — A. Azzari, M. Bicego. *IAPR Joint Int. Workshops S+SSPR* (2024), pp. 166–176. Extended with M. Bicego, T. G. Dietterich, S. Liu and A. Mensi into *On the Stability of the Isolation Forest Results* (in preparation for IEEE TKDE) — code: [if_stability](https://github.com/irazza/if_stability).
- CISOF (detection and early detection of pathological MEPs) — under review at *Journal of Healthcare Informatics Research*; patent application filed.

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
