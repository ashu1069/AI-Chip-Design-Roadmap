# AI Chip Design Roadmap

A curated collection of resources for anyone looking to break into AI accelerator and chip design, from foundational digital logic to production architectures and open-source tapeouts.

The roadmap is organized as a progression: start with the foundations, build up through GPU programming and hardware description languages, then dive into AI-specific accelerator design, ML compilers, and real company architectures.

---

## Table of Contents

- [Foundations](#foundations)
- [Intermediate: Hardware and GPU Programming](#intermediate-hardware-and-gpu-programming)
- [AI Accelerator Design and Co-Design](#ai-accelerator-design-and-co-design)
- [Key Papers](#key-papers)
- [ML Compilers](#ml-compilers)
- [Accelerator Modeling and Simulation](#accelerator-modeling-and-simulation)
- [Company Architecture Deep Dives](#company-architecture-deep-dives)
- [Research and Preparation](#research-and-preparation)
- [Additional Books](#additional-books)
- [Newsletters and Blogs](#newsletters-and-blogs)
- [Key Takeaways](#key-takeaways)

---

## Foundations

| Resource | Type | Link |
|----------|------|------|
| **Nand2Tetris**: Build a computer from first principles | Book / Course | [PDF](https://github.com/jherskow/nand2tetris/blob/master/nand2tetris%20BOOK.pdf) |
| **Digital Design and Computer Architecture**: Onur Mutlu, ETH Zurich | Video Lectures | [YouTube Playlist](https://youtube.com/playlist?list=PL5Q2soXY2Zi-yo9kK-BKrq11ykNKkVEpd&si=mMpCVd2lY4JV_MLm) |
| **Harris & Harris: DDCA RISC-V** | Textbook | [Book Site](https://pages.hmc.edu/harris/ddca/ddcarv.html) |
| **MIT 6.004: Computation Structures** | Video Lectures | [YouTube Playlist](https://youtube.com/playlist?list=PLUl4u3cNGP62WVs95MNq3dQBqY2vGOtQ2&si=4dUBEJTA0bZXk4IU) |

---

## Intermediate: Hardware and GPU Programming

| Resource | Type | Link |
|----------|------|------|
| **Programming Massively Parallel Processors** | Textbook | [PDF](https://www.cse.iitd.ac.in/~rijurekha/col730_2022/cudabook.pdf) |
| **Caltech CS179: GPU Programming** | Course | [Course Page](https://courses.cms.caltech.edu/cs179/) |
| **Stanford CS149: Parallel Computing** | Video Lectures + Labs | [YouTube Playlist](https://youtube.com/playlist?list=PLoROMvodv4rMp7MTFr4hQsDEcX7Bx6Odp&si=QFD31ERg-BIpmBqE) / [GitHub](https://github.com/PKUFlyingPig/CS149-parallel-computing) |
| **Chisel** — Hardware construction language (UC Berkeley) | HDL / Tool | [chisel-lang.org](https://www.chisel-lang.org/) |
| **Computer Architecture: A Quantitative Approach** - Chapter 7: Domain-Specific Architectures | Textbook | [PDF](https://dn790008.ca.archive.org/0/items/computerarchitectureaquantitativeapproach6thedition/Computer%20Architecture%3A%20A%20Quantitative%20Approach%206th%20Edition.pdf) |

---

## AI Accelerator Design and Co-Design

| Resource | Type | Link |
|----------|------|------|
| **Efficient Processing of DNNs**: Sze et al. | Paper + Book | [Paper](https://arxiv.org/pdf/1703.09039) / [Book](https://link.springer.com/book/10.1007/978-3-031-01766-7) |
| **Stanford CS217: Hardware Accelerators for Machine Learning** | Course | [cs217.stanford.edu](https://cs217.stanford.edu/) |
| **MIT: TinyML and Efficient Deep Learning Computing** | Video Lectures | [YouTube Playlist](https://youtube.com/playlist?list=PL80kAHvQbh-pT4lCkDT53zT8DKmhE0idB&si=DBDpd2N0Mr9EaAyM) |

---

## Key Papers

### Foundational Architectures

| Paper | Topic | Link |
|-------|-------|------|
| **TPU v1** (Google, 2017) | Google's first Tensor Processing Unit | [arXiv](https://arxiv.org/pdf/1704.04760) |
| **Eyeriss** (MIT, 2016) | Energy-efficient DNN accelerator | [Project](https://eyeriss.mit.edu/) / [Paper](https://eems.mit.edu/wp-content/uploads/2016/04/eyeriss_isca_2016.pdf) |
| **Systolic Arrays** (Kung & Leiserson, 1978) | The original systolic array paper | [PDF](https://www.eecs.harvard.edu/htk/static/files/1978-cmu-cs-report-kung-leiserson.pdf) |

### Attention and Memory Optimization

| Paper | Topic | Link |
|-------|-------|------|
| **FlashAttention** (Dao et al., 2022) | IO-aware exact attention | [arXiv](https://arxiv.org/pdf/2205.14135) |
| **FlashAttention-2** (Dao, 2023) | Better parallelism and work partitioning | [arXiv](https://arxiv.org/pdf/2307.08691) |
| **FlashAttention-3** (2024) | Further optimizations | [arXiv](https://arxiv.org/pdf/2407.08608) |

### Performance Modeling

| Paper | Topic | Link |
|-------|-------|------|
| **Roofline Model** (Williams et al.) | Visual performance model for multicore architectures | [PDF](https://people.eecs.berkeley.edu/~kubitron/cs252/handouts/papers/RooflineVyNoYellow.pdf) |

### Surveys and Overviews

| Paper | Topic | Link |
|-------|-------|------|
| **Survey on DL Hardware Accelerators** (2024) | Comprehensive accelerator survey | [ACM](https://dl.acm.org/doi/full/10.1145/3729215) |
| **A Domain-Specific Supercomputer for Training DNNs** | Training-focused supercomputer design | [Summary](https://singularitykchen.github.io/blog/2020/06/28/Read-Paper-A-domain-specific-supercomputer-for-training-DNN/) |
| **AI Accelerators for LLM Inference** (2025) | LLM inference accelerator landscape | [arXiv](https://arxiv.org/pdf/2506.00008) |
| **LLMCompass** (ISCA 2024) | LLM hardware evaluation framework | [PDF](https://augustning.com/assets/papers/llmcompass-isca-2024.pdf) |
| **A Review on Proprietary Accelerators for LLMs** (2025) | Cross-company accelerator comparison | [arXiv](https://arxiv.org/html/2503.09650v1) |
| **ISCA 2025 Relevant Papers** | Curated reading list | [Reading Notes](https://paper.lingyunyang.com/reading-notes/conference/isca-2025) |

### NVIDIA Architecture Evolution

| Resource | Link |
|----------|------|
| NVIDIA GPU Architecture Overview | [Wolf Advanced Technology](https://wolfadvancedtechnology.com/nvidia-gpu-architecture/) |
| NVIDIA Architecture Roadmap: CUDA to Blackwell | [PatSnap](https://www.patsnap.com/resources/blog/articles/nvidia-gpu-architecture-roadmap-cuda-to-blackwell/) |
| Evolution of NVIDIA Data Center GPUs | [ServerSimply](https://www.serversimply.com/blog/evolution-of-nvidia-data-center-gpus) |
| Blackwell Microarchitecture | [Wikipedia](https://en.wikipedia.org/wiki/Blackwell_(microarchitecture)) |
| H100 / Hopper Architecture Whitepaper | [NVIDIA](https://resources.nvidia.com/en-us-hopper-architecture/nvidia-h100-tensor-c) |

---

## ML Compilers

| Tool | Description | Link |
|------|-------------|------|
| **MLIR** | Multi-Level Intermediate Representation (LLVM project) | [Tutorials](https://mlir.llvm.org/docs/Tutorials/) |
| **Apache TVM** | Open-source ML compiler framework | [tvm.apache.org](https://tvm.apache.org/) |
| **Triton** | Language and compiler for writing GPU kernels | [Tutorials](https://triton-lang.org/main/getting-started/tutorials/) |
| **XLA** | Accelerated Linear Algebra compiler (OpenXLA) | [openxla.org](https://openxla.org/) |

---

## Accelerator Modeling and Simulation

| Tool | Description | Link |
|------|-------------|------|
| **Timeloop / Accelergy** | Accelerator architecture evaluation | [timeloop.csail.mit.edu](https://timeloop.csail.mit.edu/) |
| **Gemmini** (UC Berkeley) | Open-source systolic array generator | [GitHub](https://github.com/ucb-bar/gemmini) |

---

## Company Architecture Deep Dives

These companies represent different points on the specialization spectrum, from transformer-only ASICs to general-purpose GPUs, and make fundamentally different bets on memory hierarchy, execution models, and workload evolution.

### Specialization Spectrum

```
Most Specialized ◄──────────────────────────────────────────► Most General
Etched          Groq          Cerebras/MatX    Tenstorrent/SambaNova    GPUs
(transformer    (inference     (LLM             (broader AI              (general
 only)           focused)      optimized)        workloads)              purpose)
```

### Memory Hierarchy Bets

| Approach | Companies |
|----------|-----------|
| **All-SRAM** | Groq, Cerebras |
| **Hybrid (SRAM + HBM)** | MatX |
| **Three-tier memory** | SambaNova |
| **HBM-primary** | GPUs (NVIDIA) |

### Execution Model Choices

| Approach | Companies |
|----------|-----------|
| **Deterministic / compiler-scheduled** | Groq, Tenstorrent |
| **Dynamic scheduling** | GPUs (NVIDIA) |
| **Compiler-driven spatial mapping** | Cerebras, SambaNova |

---

### Groq (LPU — Language Processing Unit)

- [Groq LPU Design Deep Dive](https://blog.codingconfessions.com/p/groq-lpu-design)
- [Think Fast: A Tensor Streaming Processor (TSP) for Accelerating DNN Workloads (ISCA 2020)](https://groq.humain.ai/wp-content/uploads/2024/02/2020-Isca.pdf)
- [A Software-defined Tensor Streaming Multiprocessor (ISCA 2022)](https://dl.acm.org/doi/pdf/10.1145/3470496.3527405)
- [Groq TSP Whitepapers Summary](https://www.zellic.io/blog/groq-tsp-whitepapers/)

### Cerebras (Wafer-Scale Engine)

- [Review of Proprietary Accelerators for LLMs](https://arxiv.org/html/2503.09650v1)
- [Cerebras Architecture Analysis](https://arxiv.org/html/2503.11698v1)
- [Cerebras WSE-2 at Hot Chips 33](https://www.servethehome.com/cerebras-wafer-scale-engine-2-wse-2-at-hot-chips-33/)
- [Cerebras Whitepapers](https://www.cerebras.ai/whitepapers)

### Tenstorrent

- [Jim Keller on RISC-V and AI Processing at Tenstorrent](https://www.allaboutcircuits.com/news/cpu-designer-jim-keller-rethinks-risc-v-ai-processing-at-tenstorrent/)
- [Tenstorrent and the State of AI Hardware](https://irrationalanalysis.substack.com/p/tenstorrent-and-the-state-of-ai-hardware)

### MatX

- [MatX Research](https://matx.com/research)

### SambaNova (RDU: Reconfigurable Dataflow Unit)

- [SambaNova RDU: Reconfigurable Architectures for Inference, Training, and Agentic AI](https://medium.com/@leosorge/sambanova-rdu-reconfigurable-architectures-for-inferencefor-inference-training-and-agentic-ai-5088b5ca400b)
- [SambaNova Architecture Paper](https://arxiv.org/html/2405.07518v1)

### Graphcore (IPU: Intelligence Processing Unit)

- [SoftBank Acquires Graphcore](https://www.trendforce.com/news/2024/07/16/news-softbank-acquired-graphcore-hinting-at-a-battle-between-ipu-and-gpu/)
- [IPU Programmer's Guide](https://docs.graphcore.ai/projects/ipu-programmers-guide/en/latest/about_ipu.html)
- [Graphcore — Wikipedia](https://en.wikipedia.org/wiki/Graphcore)

### Intel Gaudi (Habana Labs)

- [Gaudi Architecture Overview](https://docs.habana.ai/en/latest/Gaudi_Overview/Gaudi_Architecture.html)
- [Intel Merges Habana with Xe GPUs](https://www.techinsights.com/blog/intel-merges-habana-xe-gpus)

### Etched (Sohu: Transformer ASIC)

- [etched.com](https://www.etched.com/)
- [Etched — Wikipedia](https://en.wikipedia.org/wiki/Etched_(company))

---

## Research and Preparation

- **Read company architecture papers**: Groq TSP, Cerebras WSE, NVIDIA whitepapers (linked above)
- **Follow top conferences** — ISCA, MICRO, ASPLOS, Hot Chips, MLSys
- **Try open-source ASIC flows**: Experiment with [OpenLane](https://github.com/The-OpenROAD-Project/OpenLane) + [SKY130 PDK](https://github.com/google/skywater-pdk) for open-source tapeouts
- **Contribute to open-source accelerator projects**: Gemmini, Chisel ecosystem, TT-Metalium
- **Study the business side**: [Acquired podcast (NVIDIA episodes)](https://www.acquired.fm/), SemiAnalysis deep dives, Fabricated Knowledge
- **Build something real**: Even a small systolic array taped out through [Tiny Tapeout](https://tinytapeout.com/) (~$50) demonstrates real capability

---

## Additional Books

| Book | Link |
|------|------|
| **MLSys Handbook** | [mlsysbook.ai](https://mlsysbook.ai/book/) |
| **Engineering a Compiler** (Cooper & Torczon) | [PDF](http://www.r-5.org/files/books/computers/compilers/writing/Keith_Cooper_Linda_Torczon-Engineering_a_Compiler-EN.pdf) |

---

## Newsletters and Blogs

| Resource | Link |
|----------|------|
| **SemiAnalysis** | [Newsletter](https://newsletter.semianalysis.com/) / [Site](https://semianalysis.com/) |
| **Fabricated Knowledge** | [fabricatedknowledge.com](https://www.fabricatedknowledge.com/) |
| **Chip Huyen** | [huyenchip.com](https://huyenchip.com/start/) |

---

## Key Takeaways

> The most important insight from surveying this entire landscape is that AI chip design is increasingly accessible. Open-source tools (OpenLane, SKY130, Chisel, Gemmini) have demolished the barrier that once required millions in EDA licenses. The real scarce resource is not tools or knowledge but the **integration skill**: understanding how transistor-level choices propagate through RTL, architecture, compiler, and ML framework to determine real-world tokens-per-second-per-watt.

**Three non-obvious recommendations:**

1. **Spend disproportionate time on FlashAttention and the Roofline Model**: Hardware-aware algorithm design increasingly determines whether new silicon succeeds or fails.

2. **Build something real early**: Even a tiny systolic array taped out through Tiny Tapeout teaches more about the ASIC flow than months of reading.

3. **Study company deep dives for strategy, not just architecture**: Groq's bet on determinism, Cerebras's wafer-scale gamble, Etched's transformer-only ASIC, and MatX's hybrid memory all represent different theories about where the memory wall, workload evolution, and economics will land. The best chip companies are built on a correct thesis about the future of AI workloads, not just superior circuits.

---

## Contributing

Found a broken link or want to suggest a resource? Open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
