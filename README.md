# 🧠 Quantum Algorithm for Solving Linear Differential Equations

This repository implements a quantum algorithm for solving first-order linear differential equations (LDEs) using Qiskit. It follows the approach described in the paper: **"Quantum Algorithm for Solving Linear Differential Equations"**  
🔗 [arXiv:1807.04553](https://arxiv.org/abs/1807.04553)

---

## 📘 Paper Summary

The paper proposes a quantum algorithm to solve systems of linear differential equations of the form:

  **dx/dt = Mx + b**

The method leverages techniques such as:
- Encoding of the matrix M,
- Taylor series expansion of matrix exponentials,
- Linear Combination of Unitaries (LCU),
to prepare quantum states encoding the solution vector x(t).

---

## ⚙️ Problem Setup (This Repository)

We simulate a Schrödinger-type evolution equation:

  **dψ(t)/dt = -i·H·ψ(t)**

where:
- H = α (X ⊗ I) + β (Z ⊗ Z)
- Initial state: |ψ(0)⟩ = |01⟩
- Parameters: α = 1.0, β = 0.5, t = 1.0

This form matches the homogeneous LDE case (i.e., with b = 0).

---

## 🧮 Implementation Summary

- Hamiltonian evolution implemented via Taylor expansion of the exponential operator.
- Truncated at 4 terms to approximate exp(-iHt).
- Qiskit is used to build and simulate the quantum circuit.
- Results are validated against exact classical solutions (via matrix exponentials).

---

