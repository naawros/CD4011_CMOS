# CMOS NAND / CD4011 Design – TSMC 180nm

This project presents the design and verification of a CMOS NAND gate used as a building block of the CD4011 quad NAND logic IC.

The project includes transistor-level design, SPICE simulations, layout implementation using Magic VLSI and comparison between pre-layout and post-layout simulations.

Technology: TSMC 180nm  
Supply voltage: 1.8V  

---

# Design flow

1. Transistor-level NAND gate design in SPICE
2. Functional verification and operating point analysis
3. Output buffer design using a tapered CMOS buffer chain
4. Layout implementation in Magic VLSI
5. Parasitic extraction
6. Post-layout simulation and comparison with schematic results

---

# Circuit structure

The circuit consists of:

- CMOS NAND logic core
- multi-stage output buffer
- bonding pads
- ESD protection structures

The output stage uses a tapered CMOS buffer chain with scaling factor = 3 in order to increase drive strength.

---

# Layout

## Single NAND gate layout

![nand layout](images/nand_layout.png)

## Full CD4011 block layout

![cd4011 layout](images/cd4011_layout.png)

---

# Simulations

Both pre-layout and post-layout simulations were performed.

Simulation conditions:

- Supply voltage: 1.8V
- Temperature sweep: -30°C, 27°C, 125°C
- SPICE transistor models for TSMC 180nm

---

# Performed tests

The following circuit tests were performed:

### Maximum switching frequency

Simulation file:

results/f_bufora_MAX_510MHz

This test estimates the maximum operating frequency of the output buffer.

---

### Output drive capability – logic low

Simulation file:

results/wydajnosc_pradowa_stan_niski

This test evaluates the current drive capability of the circuit when the output is in the LOW state.

---

### Output drive capability – logic high

Simulation file:

results/wydajnosc_pradowa_stan_wysoki

This test evaluates the current drive capability when the output is in the HIGH state.

---

### Buffer operation test

Simulation file:

results/f_bufora_30MHz

This simulation verifies correct buffer operation for a typical switching frequency.

---

# Tools used

- SPICE
- Magic VLSI

---

# Repository structure
