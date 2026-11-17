# SCORE — Open-Source SoC RTL Dataset & Hardware Benchmark Platform

[![Website](https://img.shields.io/badge/Website-score--circuits.github.io-1f6feb?style=flat&logo=githubpages&logoColor=white)](https://score-circuits.github.io)
[![Main Repo](https://img.shields.io/badge/Dataset-SCORE--CIRCUITS%2Fscore-181717?style=flat&logo=github)](https://github.com/SCORE-CIRCUITS/score)
[![Suggest a Repo](https://img.shields.io/badge/Suggest%20a%20Repo-Open%20an%20Issue-2ea44f?style=flat&logo=github)](https://github.com/SCORE-CIRCUITS/score/issues/new?title=Add%20repository%3A%20&body=%23%23%23%20Repository%20Suggestion%0A%0A-%20**GitHub%20%2F%20GitLab%20URL%3A**%20%0A-%20**Category%3A**%20MCU%20%2F%2064-bit%20App%20Core%20%2F%20Vector%20%26%20Coprocessor%20%2F%20Full%20SoC%20%2F%20EDA%20%26%20HDL%20Tooling%0A-%20**Brief%20Description%3A**%20%0A-%20**License%3A**%20)
[![License: CC BY 4.0](https://img.shields.io/badge/SCORE%20Docs%20%26%20Scripts-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

**SCORE** (**S**ystem-on-**C**hip Verilog **R**TL modules dataset f**o**r **E**DA research) is an open-source hardware ecosystem providing **reproducible, versioned Verilog/SystemVerilog RTL snapshots**, **script-driven generation flows**, and **empirical RTL simulation benchmarks** across open-source processors, accelerators, SoC platforms, and hardware construction languages.

> **Why SCORE?** EDA and computer-architecture benchmarks often suffer from ad-hoc builds, drifting upstream commits, and undocumented compile flags. SCORE pins each upstream repository to a known commit, automates installation and RTL generation (`install_*.sh` → `generate_*.sh` → `run_*.sh`), and records real RTL simulation results in standardized JSON schemas so researchers can reproduce and compare results fairly.

---

## 🌐 Explore the SCORE Website

Visit our interactive web platform at **[https://score-circuits.github.io](https://score-circuits.github.io)** to browse microarchitectural profiles, filter architectures by ISA/language/license, inspect empirical benchmark leaderboards, and export LaTeX tables with one click.

| Portal Section | What You'll Find |
|---|---|
| **[Home & Interactive Explorer](https://score-circuits.github.io/)** | Searchable hardware catalog, featured anchor architectures, and benchmark overview |
| **[Architecture Fundamentals](https://score-circuits.github.io/fundamentals/)** | Open-source hardware concepts, ISAs, interconnects, and the 4-level verification ladder |
| **[Category 1 — MCU & Scalar Cores](https://score-circuits.github.io/mcu-scalar/)** | Embedded RV32 in-order cores benchmarked with CoreMark & Dhrystone (`mcu_verilator`) |
| **[Category 2 — 64-bit Application Cores](https://score-circuits.github.io/app-cores/)** | Linux-capable RV64 in-order & OoO cores (`CoreMark`, `Dhrystone`, `memcpy`, `PMP`, `riscv-tests`) |
| **[Category 3 — Vector & Coprocessor Engines](https://score-circuits.github.io/vector-coprocessors/)** | RVV 1.0 vector units, systolic arrays, and SIMT GPGPUs (`fmatmul`, `conv2d`, `fft`, `softmax`, OpenCL) |
| **[Category 4 — Full SoC & Multi-Core Clusters](https://score-circuits.github.io/soc-multicore/)** | Multi-core clusters, NoCs, DMA engines, and heterogeneous SoCs (`soc_verilator`) |

---

## 📦 Core Public Repositories

| Repository | Description |
|---|---|
| **[SCORE-CIRCUITS/score](https://github.com/SCORE-CIRCUITS/score)** | Main SCORE repository containing versioned RTL snapshots (`datasets/`), automation scripts (`scripts/`), benchmark suites (`benchmarks/`), documentation (`docs/`), and pinned tool submodules (`tools/`). |
| **[SCORE-CIRCUITS/score-circuits.github.io](https://github.com/SCORE-CIRCUITS/score-circuits.github.io)** | Source code for the public Astro documentation & interactive benchmark portal deployed at [score-circuits.github.io](https://score-circuits.github.io). |
| **[SCORE-CIRCUITS/.github](https://github.com/SCORE-CIRCUITS/.github)** | Organization profile and community guidelines (also linked inside `score` as `tools/github`). |

---

## 🙋 Missing an Open-Source Hardware Repo? Let Us Know!

We continuously expand **SCORE-CIRCUITS** to track new and noteworthy open-source processors, accelerators, SoC platforms, HDLs, and EDA tools.

If there is a **public open-source hardware or EDA repository** that we have not captured in our organization yet, **please raise an issue and share the GitHub (or GitLab) link with us!**

- 👉 **[Open a New Repository Suggestion Issue](https://github.com/SCORE-CIRCUITS/score/issues/new?title=Add%20repository%3A%20&body=%23%23%23%20Repository%20Suggestion%0A%0A-%20**GitHub%20%2F%20GitLab%20URL%3A**%20%0A-%20**Category%3A**%20MCU%20%2F%2064-bit%20App%20Core%20%2F%20Vector%20%26%20Coprocessor%20%2F%20Full%20SoC%20%2F%20EDA%20%26%20HDL%20Tooling%0A-%20**Brief%20Description%3A**%20%0A-%20**License%3A**%20)**
- 📋 **[Browse Existing Requests & Open Issues](https://github.com/SCORE-CIRCUITS/score/issues)**

When opening an issue, please include:
1. The **repository URL** (e.g., `https://github.com/<owner>/<repo>`),
2. Its **architecture / tooling category** (MCU, 64-bit App Core, Vector/Accelerator, Full SoC, or HDL/EDA Tool), and
3. A **brief note** on what makes it useful for reproducible RTL generation or EDA benchmarking.

---

## 🛠️ Tools & Hardware Repositories in SCORE

All repositories below are **public** and tracked in [`SCORE-CIRCUITS/score`](https://github.com/SCORE-CIRCUITS/score) (pinned under `tools/` as git submodules or maintained as public organization forks for reproducibility).

### 1. MCU & Scalar Embedded Cores (15)

| Architecture | SCORE Mirror | Upstream | ISA | Language | Description |
|---|---|---|---|---|---|
| **CVA5 (Taiga)** | [SCORE-CIRCUITS/cva5](https://github.com/SCORE-CIRCUITS/cva5) | [openhwfoundation/cva5](https://github.com/openhwfoundation/cva5) | RV32IMACB | SystemVerilog | 5-stage decoupled dynamic execution core targeting FPGAs |
| **DarkRISCV** | [SCORE-CIRCUITS/darkriscv](https://github.com/SCORE-CIRCUITS/darkriscv) | [darklife/darkriscv](https://github.com/darklife/darkriscv) | RV32E / RV32I | Verilog | Minimalist 2–3 stage soft RISC-V CPU core |
| **FemtoRV** | [SCORE-CIRCUITS/learn-fpga](https://github.com/SCORE-CIRCUITS/learn-fpga) | [BrunoLevy/learn-fpga](https://github.com/BrunoLevy/learn-fpga) | RV32I / RV32E | Verilog | Compact FPGA-oriented RISC-V core family |
| **Hazard3** | [SCORE-CIRCUITS/Hazard3](https://github.com/SCORE-CIRCUITS/Hazard3) | [Wren6991/Hazard3](https://github.com/Wren6991/Hazard3) | RV32IMACB | Verilog | 3-stage RV32I[M][A][C][B] microcontroller core with debug |
| **Ibex** | [SCORE-CIRCUITS/ibex](https://github.com/SCORE-CIRCUITS/ibex) | [lowRISC/ibex](https://github.com/lowRISC/ibex) | RV32IMC | SystemVerilog | 2-stage embedded core with high verification rigor |
| **NEORV32** | [SCORE-CIRCUITS/neorv32](https://github.com/SCORE-CIRCUITS/neorv32) | [stnolting/neorv32](https://github.com/stnolting/neorv32) | RV32IMACU | VHDL | Customizable 32-bit RISC-V MCU and SoC (VHDL & Verilog flows) |
| **PicoRV32** | [SCORE-CIRCUITS/picorv32](https://github.com/SCORE-CIRCUITS/picorv32) | [YosysHQ/picorv32](https://github.com/YosysHQ/picorv32) | RV32IMC | Verilog | Size-optimized multi-cycle RISC-V CPU |
| **RISC-V VHDL** | [SCORE-CIRCUITS/riscv_vhdl](https://github.com/SCORE-CIRCUITS/riscv_vhdl) | [sergeykhbr/riscv_vhdl](https://github.com/sergeykhbr/riscv_vhdl) | RV32 / RV64 | VHDL | Portable VHDL RISC-V SoC implementation, RTL, and debugger |
| **RV12** | [SCORE-CIRCUITS/RV12](https://github.com/SCORE-CIRCUITS/RV12) | [RoaLogic/RV12](https://github.com/RoaLogic/RV12) | RV32IMC / RV64IMC | SystemVerilog | Configurable single-issue in-order RISC-V CPU core |
| **SCR1** | [SCORE-CIRCUITS/scr1](https://github.com/SCORE-CIRCUITS/scr1) | [syntacore/scr1](https://github.com/syntacore/scr1) | RV32IMC | SystemVerilog | Compact 2–4 stage embedded MCU-class core |
| **SERV** | [SCORE-CIRCUITS/serv](https://github.com/SCORE-CIRCUITS/serv) | [olofk/serv](https://github.com/olofk/serv) | RV32I / RV32E | Verilog | World's smallest bit-serial RISC-V CPU |
| **VeeR EH1** | [SCORE-CIRCUITS/Cores-VeeR-EH1](https://github.com/SCORE-CIRCUITS/Cores-VeeR-EH1) | [chipsalliance/Cores-VeeR-EH1](https://github.com/chipsalliance/Cores-VeeR-EH1) | RV32IMC | SystemVerilog | 9-stage dual-issue superscalar embedded core |
| **VeeR EH2** | [SCORE-CIRCUITS/Cores-VeeR-EH2](https://github.com/SCORE-CIRCUITS/Cores-VeeR-EH2) | [chipsalliance/Cores-VeeR-EH2](https://github.com/chipsalliance/Cores-VeeR-EH2) | RV32IMC | SystemVerilog | 9-stage 2-thread dual-issue superscalar embedded core |
| **VeeR EL2** | [SCORE-CIRCUITS/Cores-VeeR-EL2](https://github.com/SCORE-CIRCUITS/Cores-VeeR-EL2) | [chipsalliance/Cores-VeeR-EL2](https://github.com/chipsalliance/Cores-VeeR-EL2) | RV32IMC | SystemVerilog | 4-stage embedded RISC-V core |
| **VexRiscv** | [SCORE-CIRCUITS/VexRiscv](https://github.com/SCORE-CIRCUITS/VexRiscv) | [SpinalHDL/VexRiscv](https://github.com/SpinalHDL/VexRiscv) | RV32IMAFDC | SpinalHDL (Scala) | FPGA-friendly plugin-based 32-bit RISC-V core |

### 2. 64-bit Application-Class Cores (9)

| Architecture | SCORE Mirror | Upstream | ISA | Language | Description |
|---|---|---|---|---|---|
| **BlackParrot** | [SCORE-CIRCUITS/black-parrot](https://github.com/SCORE-CIRCUITS/black-parrot) | [black-parrot/black-parrot](https://github.com/black-parrot/black-parrot) | RV64GC | SystemVerilog | Modular Linux-capable 64-bit RISC-V multicore |
| **CVA6 (Ariane)** | [SCORE-CIRCUITS/cva6](https://github.com/SCORE-CIRCUITS/cva6) | [pulp-platform/cva6](https://github.com/pulp-platform/cva6) | RV64GC | SystemVerilog | 6-stage in-order application core with MMU |
| **NutShell** | [SCORE-CIRCUITS/NutShell](https://github.com/SCORE-CIRCUITS/NutShell) | [OSCPU/NutShell](https://github.com/OSCPU/NutShell) | RV64GC | Chisel (Scala) | UCAS 6-stage in-order RV64GC core and SoC |
| **Rocket Chip** | [SCORE-CIRCUITS/rocket-chip](https://github.com/SCORE-CIRCUITS/rocket-chip) | [chipsalliance/rocket-chip](https://github.com/chipsalliance/rocket-chip) | RV64GC | Chisel (Scala) | UC Berkeley 5-stage RV64GC processor generator |
| **SHAKTI C-Class** | [SCORE-CIRCUITS/c-class](https://github.com/SCORE-CIRCUITS/c-class) | [shaktiproject/c-class](https://gitlab.com/shaktiproject/cores/c-class) | RV64IMAFD | Bluespec (BSV) | IIT Madras 6-stage in-order application core |
| **SonicBOOM (BOOMv3)** | [SCORE-CIRCUITS/riscv-boom](https://github.com/SCORE-CIRCUITS/riscv-boom) | [riscv-boom/riscv-boom](https://github.com/riscv-boom/riscv-boom) | RV64GC | Chisel (Scala) | UC Berkeley out-of-order superscalar RV64GC core |
| **T-Head OpenC906** | [SCORE-CIRCUITS/openc906](https://github.com/SCORE-CIRCUITS/openc906) | [XUANTIE-RV/openc906](https://github.com/XUANTIE-RV/openc906) | RV64GCV | Verilog | 5-stage RV64GCV application core with vector processing unit |
| **T-Head OpenC910** | [SCORE-CIRCUITS/openc910](https://github.com/SCORE-CIRCUITS/openc910) | [XUANTIE-RV/openc910](https://github.com/XUANTIE-RV/openc910) | RV64GCV | Verilog | 3-issue out-of-order superscalar RV64GCV core |
| **XiangShan (NanHu)** | [SCORE-CIRCUITS/XiangShan](https://github.com/SCORE-CIRCUITS/XiangShan) | [OpenXiangShan/XiangShan](https://github.com/OpenXiangShan/XiangShan) | RV64GCBK | Chisel (Scala) | High-performance 6-issue out-of-order RISC-V processor |

### 3. Vector, Matrix & Coprocessor Engines (10)

| Architecture | SCORE Mirror | Upstream | ISA / Domain | Language | Description |
|---|---|---|---|---|---|
| **Ara** | [SCORE-CIRCUITS/ara](https://github.com/SCORE-CIRCUITS/ara) | [pulp-platform/ara](https://github.com/pulp-platform/ara) | RV64GCV (RVV 1.0) | SystemVerilog | Scalable multi-lane 64-bit vector coprocessor for CVA6 |
| **AraXL** | [SCORE-CIRCUITS/AraXL](https://github.com/SCORE-CIRCUITS/AraXL) | [pulp-platform/AraXL](https://github.com/pulp-platform/AraXL) | RV64GCV (RVV 1.0) | SystemVerilog | Physically scalable ultra-wide clustered vector processor |
| **CV32E40P** | [SCORE-CIRCUITS/cv32e40p](https://github.com/SCORE-CIRCUITS/cv32e40p) | [openhwfoundation/cv32e40p](https://github.com/openhwfoundation/cv32e40p) | RV32IMFCXpulpV2 | SystemVerilog | 4-stage in-order core with XpulpV2 packed SIMD & DSP |
| **Gemmini** | [SCORE-CIRCUITS/gemmini](https://github.com/SCORE-CIRCUITS/gemmini) | [ucb-bar/gemmini](https://github.com/ucb-bar/gemmini) | RoCC Custom | Chisel (Scala) | Berkeley configurable systolic array accelerator generator |
| **Hwacha** | [SCORE-CIRCUITS/hwacha](https://github.com/SCORE-CIRCUITS/hwacha) | [ucb-bar/hwacha](https://github.com/ucb-bar/hwacha) | Hwacha VT (RoCC) | Chisel (Scala) | Decoupled access-execute vector-fetch coprocessor |
| **Matrix Engine (IME)** | [SCORE-CIRCUITS/integrated-matrix-extension](https://github.com/SCORE-CIRCUITS/integrated-matrix-extension) | [riscv/integrated-matrix-extension](https://github.com/riscv/integrated-matrix-extension) | RISC-V IME | Spec / RTL | RISC-V Integrated Matrix Extension development repository |
| **Spatz** | [SCORE-CIRCUITS/spatz](https://github.com/SCORE-CIRCUITS/spatz) | [pulp-platform/spatz](https://github.com/pulp-platform/spatz) | RV32IMFD + Vector | SystemVerilog | Compact vector coprocessor for Snitch compute clusters |
| **TVM VTA** | [SCORE-CIRCUITS/tvm-vta](https://github.com/SCORE-CIRCUITS/tvm-vta) | [apache/tvm-vta](https://github.com/apache/tvm-vta) | Custom Tensor ISA | Chisel / C++ | Open, modular deep learning accelerator & compiler stack |
| **Vicuna** | [SCORE-CIRCUITS/vicuna](https://github.com/SCORE-CIRCUITS/vicuna) | [vproc/vicuna](https://github.com/vproc/vicuna) | RV32 Zve32x (RVV 1.0) | SystemVerilog | Compact embedded 32-bit RVV 1.0 vector coprocessor |
| **Vortex GPGPU** | [SCORE-CIRCUITS/vortex](https://github.com/SCORE-CIRCUITS/vortex) | [vortexgpgpu/vortex](https://github.com/vortexgpgpu/vortex) | RV32/64 SIMT | SystemVerilog | Open-source manycore SIMT GPGPU supporting OpenCL |

### 4. Full SoC Platforms & Multi-Core Clusters (22)

| Platform | SCORE Mirror | Upstream | ISA / Focus | Language | Description |
|---|---|---|---|---|---|
| **Astral** | [SCORE-CIRCUITS/astral](https://github.com/SCORE-CIRCUITS/astral) | [pulp-platform/astral](https://github.com/pulp-platform/astral) | RV64GC | SystemVerilog | Space computing SoC built around Cheshire |
| **Auteur** | [SCORE-CIRCUITS/auteur](https://github.com/SCORE-CIRCUITS/auteur) | [pulp-platform/auteur](https://github.com/pulp-platform/auteur) | RV64GC | SystemVerilog | Tensor unit and system exploration architecture |
| **Carfield** | [SCORE-CIRCUITS/carfield](https://github.com/SCORE-CIRCUITS/carfield) | [pulp-platform/carfield](https://github.com/pulp-platform/carfield) | RV64GC + RV32IMC | SystemVerilog | Mixed-criticality heterogeneous SoC with Safety Island |
| **Cheshire** | [SCORE-CIRCUITS/cheshire](https://github.com/SCORE-CIRCUITS/cheshire) | [pulp-platform/cheshire](https://github.com/pulp-platform/cheshire) | RV64GC (CVA6) | SystemVerilog | Minimal Linux-capable 64-bit RISC-V SoC with DMA |
| **Cheshire (IHP130-O)** | [SCORE-CIRCUITS/cheshire-ihp130-o](https://github.com/SCORE-CIRCUITS/cheshire-ihp130-o) | [pulp-platform/cheshire-ihp130-o](https://github.com/pulp-platform/cheshire-ihp130-o) | RV64GC | SystemVerilog / Tcl | Tapeout-ready 130nm IHP SG13G2 ASIC edition of Cheshire |
| **Chimera** | [SCORE-CIRCUITS/chimera](https://github.com/SCORE-CIRCUITS/chimera) | [pulp-platform/chimera](https://github.com/pulp-platform/chimera) | RV64GC + Snitch | SystemVerilog | Configurable heterogeneous multi-cluster edge AI SoC |
| **Chipyard** | [SCORE-CIRCUITS/chipyard](https://github.com/SCORE-CIRCUITS/chipyard) | [ucb-bar/chipyard](https://github.com/ucb-bar/chipyard) | RV32 / RV64 | Chisel (Scala) | Agile RISC-V SoC design framework (cores, accelerators, flows) |
| **CROC** | [SCORE-CIRCUITS/croc](https://github.com/SCORE-CIRCUITS/croc) | [pulp-platform/croc](https://github.com/pulp-platform/croc) | RV32IMC | SystemVerilog | Compact educational PULP SoC with full physical design flow |
| **HERO** | [SCORE-CIRCUITS/hero](https://github.com/SCORE-CIRCUITS/hero) | [pulp-platform/hero](https://github.com/pulp-platform/hero) | ARMv8 + RV32/64 | SystemVerilog | Heterogeneous research platform (host CPU + manycore cluster) |
| **IOb-SoC** | [SCORE-CIRCUITS/iob-soc](https://github.com/SCORE-CIRCUITS/iob-soc) | [IObundle/iob-soc](https://github.com/IObundle/iob-soc) | RV32IMC | Verilog / Python | Modular Python-generated RISC-V SoC template |
| **MAGIA** | [SCORE-CIRCUITS/MAGIA](https://github.com/SCORE-CIRCUITS/MAGIA) | [pulp-platform/MAGIA](https://github.com/pulp-platform/MAGIA) | RV32IMF | SystemVerilog | Large-scale 2D mesh manycore with GeMM & RDMA accelerators |
| **MemPool** | [SCORE-CIRCUITS/mempool](https://github.com/SCORE-CIRCUITS/mempool) | [pulp-platform/mempool](https://github.com/pulp-platform/mempool) | RV32IMA (Snitch) | SystemVerilog | Scalable 256/1024-core shared-L1 manycore system |
| **Occamy** | [SCORE-CIRCUITS/occamy](https://github.com/SCORE-CIRCUITS/occamy) | [pulp-platform/occamy](https://github.com/pulp-platform/occamy) | RV64GC + Snitch | SystemVerilog | High-efficiency dual-chiplet heterogeneous floating-point SoC |
| **OpenPiton** | [SCORE-CIRCUITS/openpiton](https://github.com/SCORE-CIRCUITS/openpiton) | [PrincetonUniversity/openpiton](https://github.com/PrincetonUniversity/openpiton) | RV64GC / SPARC | Verilog | Princeton scalable manycore research framework with P-Mesh NoC |
| **OpenTitan** | [SCORE-CIRCUITS/opentitan](https://github.com/SCORE-CIRCUITS/opentitan) | [lowRISC/opentitan](https://github.com/lowRISC/opentitan) | RV32IMC (Ibex) | SystemVerilog | Open-source silicon Root of Trust platform |
| **Picobello** | [SCORE-CIRCUITS/picobello](https://github.com/SCORE-CIRCUITS/picobello) | [pulp-platform/picobello](https://github.com/pulp-platform/picobello) | RV64GC + Snitch | SystemVerilog | Multi-cluster FlooNoC mesh SoC platform |
| **PULP Cluster** | [SCORE-CIRCUITS/pulp_cluster](https://github.com/SCORE-CIRCUITS/pulp_cluster) | [pulp-platform/pulp_cluster](https://github.com/pulp-platform/pulp_cluster) | RV32IMFD | SystemVerilog | Multi-core shared-L1 TCDM compute cluster |
| **PULP SoC** | [SCORE-CIRCUITS/pulp_soc](https://github.com/SCORE-CIRCUITS/pulp_soc) | [pulp-platform/pulp_soc](https://github.com/pulp-platform/pulp_soc) | RV32IMFD | SystemVerilog | Core microcontroller SoC subsystem for PULP platforms |
| **PULPissimo** | [SCORE-CIRCUITS/pulpissimo](https://github.com/SCORE-CIRCUITS/pulpissimo) | [pulp-platform/pulpissimo](https://github.com/pulp-platform/pulpissimo) | RV32IMFC | SystemVerilog | Single-core PULP microcontroller SoC with uDMA |
| **RV-Tracer** | [SCORE-CIRCUITS/rv_tracer](https://github.com/SCORE-CIRCUITS/rv_tracer) | [pulp-platform/rv_tracer](https://github.com/pulp-platform/rv_tracer) | RV32 / RV64 Trace | SystemVerilog | RISC-V E-Trace specification RTL implementation |
| **Safety Island** | [SCORE-CIRCUITS/safety_island](https://github.com/SCORE-CIRCUITS/safety_island) | [pulp-platform/safety_island](https://github.com/pulp-platform/safety_island) | RV32IMC Lockstep | SystemVerilog | Reliable real-time lockstep safety subsystem |
| **Snitch Cluster** | [SCORE-CIRCUITS/snitch_cluster](https://github.com/SCORE-CIRCUITS/snitch_cluster) | [pulp-platform/snitch_cluster](https://github.com/pulp-platform/snitch_cluster) | RV32IMA + SSR/FREP | SystemVerilog | Energy-efficient RISC-V floating-point compute cluster |

### 5. HDLs, HLS, Simulators, Verification & EDA Tooling (22)

| Tool | SCORE Mirror / Link | Upstream | Domain | Language | Description |
|---|---|---|---|---|---|
| **AHA Flow** | [SCORE-CIRCUITS/aha](https://github.com/SCORE-CIRCUITS/aha) | [StanfordAHA/aha](https://github.com/StanfordAHA/aha) | Hardware Flow | Python | Stanford Agile Hardware Center generator flow |
| **Amaranth HDL** | [SCORE-CIRCUITS/amaranth](https://github.com/SCORE-CIRCUITS/amaranth) | [amaranth-lang/amaranth](https://github.com/amaranth-lang/amaranth) | HDL | Python | Python-based hardware definition language & toolchain |
| **Bambu (PandA)** | [SCORE-CIRCUITS/PandA-bambu](https://github.com/SCORE-CIRCUITS/PandA-bambu) | [ferrandi/PandA-bambu](https://github.com/ferrandi/PandA-bambu) | HLS | C++ | Open-source C/C++ high-level synthesis framework |
| **Chisel** | [SCORE-CIRCUITS/chisel](https://github.com/SCORE-CIRCUITS/chisel) | [chipsalliance/chisel](https://github.com/chipsalliance/chisel) | HDL | Scala | Scala-embedded hardware construction language |
| **DiffTest** | [SCORE-CIRCUITS/difftest](https://github.com/SCORE-CIRCUITS/difftest) | [OpenXiangShan/difftest](https://github.com/OpenXiangShan/difftest) | Verification | C++ | Differential co-simulation framework for RISC-V CPUs |
| **DRAMSim2** | [SCORE-CIRCUITS/DRAMSim2](https://github.com/SCORE-CIRCUITS/DRAMSim2) | [umd-memsys/DRAMSim2](https://github.com/umd-memsys/DRAMSim2) | Simulator | C++ | Cycle-accurate DDR2/DDR3 memory system simulator |
| **GHDL** | [ghdl/ghdl](https://github.com/ghdl/ghdl) | [ghdl/ghdl](https://github.com/ghdl/ghdl) | Simulator | Ada / C++ | Open-source VHDL analyzer, compiler, simulator & synthesizer |
| **Google XLS** | [SCORE-CIRCUITS/xls](https://github.com/SCORE-CIRCUITS/xls) | [google/xls](https://github.com/google/xls) | HLS | C++ | Accelerated hardware synthesis toolchain |
| **mflowgen** | [SCORE-CIRCUITS/mflowgen](https://github.com/SCORE-CIRCUITS/mflowgen) | [mflowgen/mflowgen](https://github.com/mflowgen/mflowgen) | ASIC/FPGA Flow | Python | Modular ASIC & FPGA physical design flow generator |
| **MyHDL** | [SCORE-CIRCUITS/myhdl](https://github.com/SCORE-CIRCUITS/myhdl) | [myhdl/myhdl](https://github.com/myhdl/myhdl) | HDL | Python | Python hardware modeling, simulation, and RTL conversion |
| **NOCulator** | [SCORE-CIRCUITS/NOCulator](https://github.com/SCORE-CIRCUITS/NOCulator) | [CMU-SAFARI/NOCulator](https://github.com/CMU-SAFARI/NOCulator) | NoC Simulator | C# / C++ | Cycle-accurate network-on-chip simulator |
| **PeakRDL** | [SCORE-CIRCUITS/PeakRDL](https://github.com/SCORE-CIRCUITS/PeakRDL) | [SystemRDL/PeakRDL](https://github.com/SystemRDL/PeakRDL) | CSR Generator | Python | SystemRDL control & status register code generator |
| **PipelineC** | [SCORE-CIRCUITS/PipelineC](https://github.com/SCORE-CIRCUITS/PipelineC) | [JulianKemmerer/PipelineC](https://github.com/JulianKemmerer/PipelineC) | HDL / HLS | C / Python | C-like HDL with automatic pipelining |
| **Py2HWSW** | [SCORE-CIRCUITS/py2hwsw](https://github.com/SCORE-CIRCUITS/py2hwsw) | [IObundle/py2hwsw](https://github.com/IObundle/py2hwsw) | HW/SW Framework | Python | Python framework for managing embedded HW/SW projects |
| **PyMTL3** | [SCORE-CIRCUITS/pymtl3](https://github.com/SCORE-CIRCUITS/pymtl3) | [pymtl/pymtl3](https://github.com/pymtl/pymtl3) | HDL / Verification | Python | Python-based hardware generation, simulation & verification |
| **RgGen** | [SCORE-CIRCUITS/rggen](https://github.com/SCORE-CIRCUITS/rggen) | [rggen/rggen](https://github.com/rggen/rggen) | CSR Generator | Ruby | Control & status register code generator |
| **RISC-V Arch Test** | [SCORE-CIRCUITS/riscv-arch-test](https://github.com/SCORE-CIRCUITS/riscv-arch-test) | [riscv/riscv-arch-test](https://github.com/riscv/riscv-arch-test) | Compliance | Assembly | Official RISC-V architectural certification test suite |
| **RISC-V Matrix Spec** | [SCORE-CIRCUITS/riscv-matrix-extension-spec](https://github.com/SCORE-CIRCUITS/riscv-matrix-extension-spec) | [XUANTIE-RV/riscv-matrix-extension-spec](https://github.com/XUANTIE-RV/riscv-matrix-extension-spec) | Specification | Spec | Matrix extension proposal for AI applications on RISC-V |
| **RISC-V P-Extension Spec** | [SCORE-CIRCUITS/riscv-p-spec](https://github.com/SCORE-CIRCUITS/riscv-p-spec) | [riscv/riscv-p-spec](https://github.com/riscv/riscv-p-spec) | Specification | Spec | RISC-V Packed SIMD (P-Extension) specification |
| **SoC Automation** | [SCORE-CIRCUITS/SoC_Automation](https://github.com/SCORE-CIRCUITS/SoC_Automation) | [habibagamal/SoC_Automation](https://github.com/habibagamal/SoC_Automation) | SoC Generator | Verilog / Python | JSON-driven AMBA AHB/APB SoC-to-GDSII automation flow |
| **SpinalHDL** | [SCORE-CIRCUITS/SpinalHDL](https://github.com/SCORE-CIRCUITS/SpinalHDL) | [SpinalHDL/SpinalHDL](https://github.com/SpinalHDL/SpinalHDL) | HDL | Scala | Scala-based hardware description language |
| **Verilator** | [SCORE-CIRCUITS/verilator](https://github.com/SCORE-CIRCUITS/verilator) | [verilator/verilator](https://github.com/verilator/verilator) | Simulator | C++ / SV | High-speed open-source Verilog/SystemVerilog simulator & linter |

---

## 🚀 Quick Start

Clone the main [`SCORE-CIRCUITS/score`](https://github.com/SCORE-CIRCUITS/score) repository and initialize only the submodules you need (or all public tool submodules):

```bash
git clone https://github.com/SCORE-CIRCUITS/score.git
cd score

# Initialize specific tool submodule(s) (example: Rocket Chip)
git submodule update --init tools/rocket-chip

# 1. Install toolchains & dependencies
./scripts/install_rocket_chip.sh

# 2. Generate versioned RTL into datasets/<arch>/<commit>/
./scripts/generate_rocket_chip.sh

# 3. Run RTL simulation & benchmark checks (when available)
./scripts/run_rocket_chip.sh
```

### Repository Structure (`SCORE-CIRCUITS/score`)

```text
score/
├── benchmarks/   # Standardized benchmark suite definitions & aggregated results
├── datasets/     # Versioned RTL snapshots (datasets/<architecture>/<commit>/) & logs
├── docs/         # Per-architecture technical guides and reference notes
├── scripts/      # Automated install_*, generate_*, run_*, and helper shell scripts
└── tools/        # Pinned open-source hardware & EDA tool git submodules
```

---

## 📊 Benchmarking Principles

- **Real RTL Simulation Only:** All performance numbers are produced by genuine RTL simulation (Verilator / GHDL) — zero synthetic estimates or hardcoded metrics.
- **Versioned Provenance:** Every RTL snapshot and benchmark JSON (`score.benchmark_results.v1`) is stored alongside its exact upstream Git commit, simulator version, and generation log.
- **Four-Tier Taxonomy:** Workloads scale cleanly from single-core scalar microbenchmarks (CoreMark/Dhrystone) to 64-bit OS-capable suites (`riscv-tests`, PMP), vector/matrix kernels, and multi-core SoC/DMA scaling tests.

---

## 📄 Licensing & Citation

- **Upstream Hardware & Tooling:** Each submodule and generated RTL snapshot remains governed by its **upstream project's open-source license** (Apache-2.0, BSD, Solderpad Hardware License, ISC, MIT, GPL, etc.). Please consult the `LICENSE` file in each repository.
- **SCORE Automation, Catalog Metadata & Documentation:** Released under **[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)**.

If you use SCORE in your research, please cite both SCORE and the upstream hardware projects whose RTL you evaluate:

```bibtex
@misc{score,
  title        = {SCORE: Reproducible SoC RTL Snapshots for EDA Research},
  howpublished = {\url{https://github.com/SCORE-CIRCUITS/score}},
  note         = {Portal: \url{https://score-circuits.github.io}}
}
```

---

## 🙏 Acknowledgments

SCORE builds upon the tremendous work of the global open-source silicon and EDA communities — including the **PULP Platform**, **CHIPS Alliance**, **UC Berkeley BAR**, **OpenHW Foundation**, **lowRISC**, **OpenXiangShan**, **IObundle**, **Princeton OpenPiton**, **NEORV32**, **YosysHQ**, **Verilator**, and all upstream contributors listed above.
