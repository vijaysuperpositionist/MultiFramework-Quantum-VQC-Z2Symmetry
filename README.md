This repository implements and compares Variational Quantum Classifier (VQC) architectures for detecting Z₂ parity symmetry in toy Hamiltonians across three major quantum frameworks:

PennyLane (IBM backend) — full classical simulation and circuit cost convergence analysis
Cirq (Google backend) — implemented with both gradient-free and gradient-based optimization
Qiskit (IBM Composer + Aer simulator + real device) — results from real IBM Quantum backends

Key Features:

Dataset builder for Z₂-symmetric and asymmetric Hamiltonians

Angle encoding of features via RY gates

Cost function convergence plots and ROC curves

Threshold tuning for classifier outputs

Cirq implementation using both gradient-based and gradient-free methods

Real quantum hardware job run via IBM Composer (Sherbrooke backend)

📂 File Overview

vq_classifier_symmetry_pennylane.ipynb: PennyLane simulation for VQC Z₂ classifier

vq_classifier_symmetry_pennylane--ibm.ipynb: PennyLane version adapted for IBM Simulator

vq_classifier_symmetry_cirq.ipynb: Cirq implementation using both optimization strategies

job_VQC-Z2-IBM_Qiskit_results_c.pdf: Output from IBM Composer run

📉 Sample Results

PennyLane: AUC = 0.65 (post-threshold tuning), Accuracy = 0.60

Cirq (Gradient-Free): AUC = 0.75, Accuracy = 0.70

Cirq (Gradient-Based): AUC = 0.95, Accuracy = 0.80

Qiskit Composer: Real hardware histogram output included

🧭 Next Steps

Feel free to explore each notebook and PDF result to trace the performance across frameworks. This repo is part of an IEEE QCE25 submission effort.
