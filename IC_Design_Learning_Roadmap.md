# IC Design Learning Roadmap

> A practical roadmap for learning Digital Logic, Verilog/SystemVerilog, ASIC Design Flow, Design Verification/UVM, Physical Design, and Analog IC Design.

## Roadmap Overview

```text
FOUNDATIONS
  ├─ Mathematics
  ├─ Circuit Fundamentals
  ├─ Semiconductor / MOSFET
  └─ Linux / Git / Python / TCL
          │
          ├──────────── DIGITAL ────────────┐
          │                                 │
          ↓                                 ↓
    Digital Logic                        Verilog
          ↓                                 ↓
   Sequential Logic                    SystemVerilog
          ↓                                 ↓
 Computer Architecture                 RTL Design
                                            │
                              ┌─────────────┴─────────────┐
                              ↓                           ↓
                       Verification                  ASIC Flow
                              ↓                           ↓
                            UVM                    Synthesis / STA
                                                          ↓
                                                   Physical Design
                                                          ↓
                                                        Signoff

          └──────────── ANALOG ─────────────┐
                                             ↓
                                      Analog IC Design
                                             ↓
                                  Amplifiers / Biasing
                                             ↓
                             Differential Pair / OTA
                                             ↓
                                Frequency / Feedback
                                             ↓
                                       Analog Layout
                                             ↓
                                DRC / LVS / PEX / Post-layout
```

---

## Phase 0 — Foundations

### Mathematics
- [ ] Algebra
- [ ] Logarithms
- [ ] Complex numbers
- [ ] Derivatives
- [ ] Integrals
- [ ] Basic differential equations
- [ ] Fourier / Laplace basics
- [ ] Probability basics
- [ ] Decibel calculations

### Circuit Fundamentals
- [x] Ohm's law
- [x] KCL / KVL
- [x] Voltage, current, power
- [x] Thevenin / Norton
- [x] RC / RL / RLC circuits
- [x] Transient analysis
- [x] AC analysis
- [x] Frequency response
- [x] Bode plots

### Semiconductor Fundamentals
- [x] PN junction
- [x] Diode
- [x] BJT basics
- [x] MOS capacitor
- [x] NMOS / PMOS
- [x] CMOS
- [ ] Threshold voltage
- [x] Cutoff / triode / saturation
- [x] Body effect
- [x] Channel-length modulation
- [x] Small-signal model

### Tools
- [ ] Linux terminal / Bash
- [ ] Git / GitHub
- [ ] Python basics
- [ ] TCL basics
- [ ] Makefile basics

---

## Phase 1 — Digital Logic

### Boolean Logic
- [x] Binary / hexadecimal
- [x] Boolean algebra
- [x] Truth tables
- [ ] De Morgan's laws
- [x] Logic gates
- [x] NAND / NOR as universal gates
- [x] XOR / XNOR
- [ ] Karnaugh maps

### Combinational Logic
- [ ] Multiplexer / Demultiplexer
- [ ] Encoder / Decoder
- [ ] Comparator
- [ ] Half adder / Full adder
- [ ] Ripple-carry adder
- [ ] Subtractor
- [ ] ALU

### Sequential Logic
- [ ] Latch
- [ ] D / JK / T flip-flops
- [ ] Register
- [ ] Shift register
- [ ] Counter
- [ ] Clocking
- [ ] Reset strategies

### FSM
- [ ] Moore FSM
- [ ] Mealy FSM
- [ ] State encoding
- [ ] State transition diagrams
- [ ] FSM RTL implementation

### Projects
- [ ] 4-bit ALU
- [ ] Sequence detector
- [ ] Traffic-light controller
- [ ] UART TX/RX

---

## Phase 2 — Computer Architecture Basics

- [ ] Datapath
- [ ] Control unit
- [ ] Register file
- [ ] ALU
- [ ] Program counter
- [ ] Instruction memory
- [ ] Data memory
- [ ] Bus
- [ ] Pipeline basics
- [ ] Hazards basics
- [ ] Cache basics

### Projects
- [ ] Simple 8-bit CPU
- [ ] Single-cycle RISC-V CPU

---

## Phase 3 — Verilog

### Language
- [ ] Modules / ports
- [ ] wire / reg
- [ ] Parameters
- [ ] Continuous assignment
- [ ] Procedural blocks
- [ ] if / case / for
- [ ] Blocking assignment
- [ ] Non-blocking assignment

### RTL
- [ ] Combinational RTL
- [ ] Sequential RTL
- [ ] Registers / counters
- [ ] FSM
- [ ] Parameterized modules
- [ ] Generate blocks

### Projects
- [ ] ALU
- [ ] FIFO
- [ ] UART
- [ ] SPI controller
- [ ] RAM controller

---

## Phase 4 — SystemVerilog

### Language
- [ ] `logic`
- [ ] `always_comb`
- [ ] `always_ff`
- [ ] `always_latch`
- [ ] `enum`
- [ ] `struct`
- [ ] `package`
- [ ] `interface`

### OOP
- [ ] Class
- [ ] Constructor
- [ ] Inheritance
- [ ] Polymorphism
- [ ] Encapsulation
- [ ] Virtual methods

### Verification Features
- [ ] Randomization
- [ ] Constraints
- [ ] Assertions
- [ ] Functional coverage
- [ ] Mailboxes / events

---

## Phase 5 — Design Verification

```text
Stimulus → Driver → DUT → Monitor → Checker / Scoreboard → Pass/Fail → Coverage
```

- [ ] Testbench architecture
- [ ] Directed tests
- [ ] Constrained-random testing
- [ ] Reference model
- [ ] Scoreboard
- [ ] Monitor
- [ ] Functional coverage
- [ ] Code coverage
- [ ] Assertions
- [ ] Regression testing
- [ ] Waveform debugging

### Projects
- [ ] Verify FIFO
- [ ] Verify UART
- [ ] Verify AXI-Lite slave

---

## Phase 6 — UVM

```text
Test
 └── Environment
      ├── Agent
      │    ├── Sequencer
      │    ├── Driver
      │    └── Monitor
      └── Scoreboard
```

- [ ] `uvm_test`
- [ ] `uvm_env`
- [ ] `uvm_agent`
- [ ] `uvm_driver`
- [ ] `uvm_monitor`
- [ ] `uvm_sequencer`
- [ ] `uvm_sequence`
- [ ] `uvm_sequence_item`
- [ ] Factory
- [ ] Config DB
- [ ] TLM
- [ ] Analysis ports
- [ ] Phases / objections
- [ ] Virtual sequencer
- [ ] Register model basics

### Project
- [ ] Complete UVM environment for FIFO or UART
- [ ] Functional coverage
- [ ] Assertions
- [ ] Scoreboard
- [ ] Regression

---

## Phase 7 — ASIC Design Flow

```text
Specification
  ↓
Architecture
  ↓
RTL
  ↓
Simulation / Verification
  ↓
Synthesis
  ↓
Gate-level Netlist
  ↓
Floorplan
  ↓
Placement
  ↓
CTS
  ↓
Routing
  ↓
STA
  ↓
DRC / LVS
  ↓
GDSII
```

- [ ] RTL design
- [ ] Lint
- [ ] CDC basics
- [ ] Simulation
- [ ] Logic synthesis
- [ ] Standard-cell library
- [ ] Netlist
- [ ] SDC constraints
- [ ] STA
- [ ] Power estimation
- [ ] DFT basics
- [ ] Physical implementation
- [ ] Signoff

---

## Phase 8 — Physical Design

### Floorplanning
- [ ] Die / core area
- [ ] Aspect ratio
- [ ] Utilization
- [ ] IO placement
- [ ] Macro placement
- [ ] Power grid / rings / straps

### Placement
- [ ] Standard-cell placement
- [ ] Congestion
- [ ] Density
- [ ] Optimization

### CTS
- [ ] Clock tree
- [ ] Clock latency
- [ ] Clock skew
- [ ] Clock uncertainty
- [ ] Clock buffers

### Routing
- [ ] Global routing
- [ ] Detailed routing
- [ ] Congestion
- [ ] Antenna effects

### Timing
- [ ] Setup / hold time
- [ ] Clock-to-Q
- [ ] Propagation delay
- [ ] Slack
- [ ] Critical path
- [ ] Setup / hold violations
- [ ] OCV basics
- [ ] MCMM basics

### Signoff
- [ ] STA
- [ ] DRC
- [ ] LVS
- [ ] IR drop
- [ ] Electromigration
- [ ] Power analysis

### Project
- [ ] RTL → synthesis
- [ ] Netlist → floorplan
- [ ] Placement
- [ ] CTS
- [ ] Routing
- [ ] STA
- [ ] DRC/LVS
- [ ] GDS generation

---

## Phase 9 — Analog IC Design

### MOSFET / Biasing
- [ ] DC operating point
- [ ] Q-point
- [ ] Biasing
- [ ] Small-signal model
- [ ] `gm`
- [ ] `ro`
- [ ] `gmb`
- [ ] Channel-length modulation
- [ ] Body effect

### Basic Amplifiers
- [ ] Common Source
- [ ] Common Gate
- [ ] Common Drain
- [ ] Source degeneration
- [ ] Active load
- [ ] Cascode

Key small-signal relation for a basic CS stage:

\[
A_v \approx -g_m R_D
\]

### Current Sources
- [ ] Current mirror
- [ ] Cascode current mirror
- [ ] Wilson current mirror
- [ ] Bias generation

### Differential Pair
- [ ] Differential input
- [ ] Common-mode input
- [ ] Differential gain
- [ ] Common-mode gain
- [ ] CMRR
- [ ] Tail current
- [ ] Active load

### OTA / Op-Amp
- [ ] Single-stage OTA
- [ ] Two-stage OTA
- [ ] Folded cascode
- [ ] Telescopic cascode
- [ ] Gain
- [ ] GBW
- [ ] Slew rate
- [ ] Output swing
- [ ] Input common-mode range

### Feedback / Stability
- [ ] Negative feedback
- [ ] Loop gain
- [ ] Poles / zeros
- [ ] Dominant pole
- [ ] Miller effect
- [ ] Compensation
- [ ] Phase margin
- [ ] Gain margin

---

## Phase 10 — Analog Simulation

Using Cadence Virtuoso / Spectre:

- [ ] DC analysis
- [ ] AC analysis
- [ ] Transient analysis
- [ ] Noise analysis
- [ ] Parametric sweep
- [ ] Monte Carlo basics
- [ ] Corner analysis
- [ ] Gain measurement
- [ ] Phase measurement
- [ ] Bandwidth / `f-3dB`
- [ ] Operating point
- [ ] Device parameters

### Projects
- [ ] Common-source amplifier
- [ ] Current mirror
- [ ] Differential pair
- [ ] Two-stage OTA
- [ ] Frequency compensation
- [ ] Post-layout simulation

---

## Phase 11 — Analog Layout

### Layout Fundamentals
- [ ] Transistor layout
- [ ] Contacts
- [ ] Metal layers
- [ ] Via
- [ ] Well
- [ ] Well taps
- [ ] Guard rings

### Matching
- [ ] Device matching
- [ ] Common-centroid
- [ ] Interdigitation
- [ ] Dummy devices
- [ ] Symmetry

### Parasitics
- [ ] Parasitic capacitance
- [ ] Parasitic resistance
- [ ] Coupling
- [ ] Shielding

### Signoff

```text
Schematic
  ↓
Layout
  ↓
DRC
  ↓
LVS
  ↓
PEX
  ↓
Post-layout simulation
```

### Project
- [ ] Layout a current mirror
- [ ] Layout a differential pair
- [ ] Layout a two-stage OTA
- [ ] Run DRC
- [ ] Run LVS
- [ ] Run PEX
- [ ] Compare pre-layout vs post-layout

---

## Recommended Tool Stack

### Digital / RTL
- Verilog / SystemVerilog
- Icarus Verilog
- Verilator
- GTKWave
- cocotb

### ASIC
- Yosys
- OpenROAD
- OpenLane
- Design Compiler
- Innovus
- PrimeTime

### Analog
- Cadence Virtuoso
- Spectre
- ADE
- ViVA

### Productivity
- Linux
- Git / GitHub
- Bash
- Python
- TCL
- Make

---

## Project Ladder

### Beginner
- [ ] 4-bit adder
- [ ] 4-bit ALU
- [ ] Counter
- [ ] FSM

### Intermediate
- [ ] UART TX/RX
- [ ] SPI
- [ ] FIFO
- [ ] RAM controller
- [ ] RISC-V single-cycle CPU

### Verification
- [ ] SystemVerilog testbench
- [ ] Assertions
- [ ] Functional coverage
- [ ] UVM FIFO verification
- [ ] UVM UART verification

### ASIC
- [ ] RTL synthesis
- [ ] STA
- [ ] Floorplan
- [ ] Placement
- [ ] CTS
- [ ] Routing
- [ ] DRC/LVS
- [ ] GDS generation

### Analog
- [ ] Common-source amplifier
- [ ] Current mirror
- [ ] Differential pair
- [ ] OTA
- [ ] Two-stage op-amp
- [ ] Analog layout
- [ ] Post-layout simulation

---

## Suggested 12-Month Plan

| Month | Main Focus |
|---|---|
| 1 | Circuits + Semiconductor |
| 2 | MOSFET + CMOS |
| 3 | Digital Logic |
| 4 | Sequential Logic + FSM |
| 5 | Verilog |
| 6 | SystemVerilog + RTL |
| 7 | Verification |
| 8 | UVM |
| 9 | ASIC Flow + Synthesis |
| 10 | Physical Design |
| 11 | Analog IC Design |
| 12 | Analog Layout + Final Project |

> 18–24 months is a more realistic pace for deep understanding across all tracks.

---

## GitHub Portfolio Structure

```text
ic-design-journey/
├── digital/
│   ├── logic-gates/
│   ├── alu/
│   ├── uart/
│   ├── fifo/
│   └── riscv/
├── rtl/
│   ├── verilog/
│   └── systemverilog/
├── verification/
│   ├── sv-testbenches/
│   └── uvm/
├── asic/
│   ├── synthesis/
│   ├── sta/
│   └── physical-design/
├── analog/
│   ├── common-source/
│   ├── current-mirror/
│   ├── differential-pair/
│   └── ota/
├── analog-layout/
│   ├── drc/
│   ├── lvs/
│   ├── pex/
│   └── post-layout/
└── README.md
```

For each project, keep:

- schematic / RTL
- simulation
- testbench
- waveform / plots
- design notes
- results
- README
- lessons learned

---

## Core Principle

Do not study the topics as isolated subjects.

### Digital

```text
Specification
→ RTL
→ Verification
→ Synthesis
→ Physical Design
→ Signoff
```

### Analog

```text
Specification
→ Architecture
→ Schematic
→ Simulation
→ Layout
→ DRC/LVS
→ PEX
→ Post-layout
```

The long-term goal is to understand how an IC moves from an idea to a verified physical chip.
