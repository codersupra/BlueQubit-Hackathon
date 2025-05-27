# BlueQubit-Hackathon
## Project Description
This project implements solutions to the "Peaked Circuits" challenge - a novel approach for verifiable quantum advantage introduced by Scott Aaronson. Peaked circuits are specially designed quantum circuits that produce a non-uniform output distribution with one dominant bitstring (probability O(1)), unlike random circuits where outputs have exponentially small amplitudes.

This implementation demonstrates two distinct approaches to efficiently identify the hidden high-probability bitstring in given peaked circuits (provided in .qasm format), while maintaining the verifiability advantage over classical simulation methods.

### Technical Approaches
1. State Vector Simulation
Implementation:

  - Full quantum state evolution using state vector representation

  - Exact amplitude calculation for all possible bitstrings

  - Direct probability measurement of the peaked output

Significance:

  - Provides ground truth results for verification

  - Demonstrates the theoretical peaked distribution

  - Limited to small qubit counts (~30 qubits) due to exponential memory requirements

2. Matrix Product State (MPS) Simulation
Implementation:

  - Tensor network representation of quantum state

  - Controlled truncation of bond dimensions

  - Approximate sampling of output distribution

Significance:

  - Enables simulation of larger circuits (~50-100 qubits)

  - Maintains high accuracy for peaked circuits due to localized entanglement

  - Demonstrates classical simulability limits of peaked circuits

### Key Features
  - QASM circuit parser for peaked circuit input

  - Cross-verification across all three methods

  - Performance benchmarking tools

  - Visualization of output distributions

### Applications
  1. Quantum advantage verification

  2. Quantum hardware benchmarking

  3. Random circuit sampling validation

Quantum algorithm testing

### Requirements
  - Python 3.8+

  - Qiskit

  - NumPy
