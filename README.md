# PennylaneHamiltonian
Variational Quantum Learning of Hidden Symmetries in Quantum Hamiltonians: Enabling Improved Ansatz Design and Error Robustness in Near-Term Quantum Systems.
Quantum Symmetry Classifier – 2-Qubit VQC (Pennylane)
This project implements a Variational Quantum Classifier (VQC) using Pennylane to identify symmetry properties of quantum Hamiltonians. It serves as a proof-of-concept for symmetry detection via quantum machine learning and will be submitted to IEEE QCE25.

What We’ve Done (So Far)
📦 Environment Setup

Created and isolated a pennylane_env using Anaconda

Installed pennylane, scikit-learn, matplotlib, and Qiskit simulators

⚙️ Model Architecture

Built a 2-qubit classifier circuit using a basic ansatz:

RY(x) encoding for features

RY(weights) for trainable parameters

CNOT entanglement between qubits

Output: ⟨Z⟩ expectation on qubit 0

Training Loop

Implemented custom loss with soft labels (0.9/0.1)

Added L2 regularization

Integrated validation loss tracking

Saved loss history to loss_log.csv

Added live plotting of training vs validation loss

Generalization Measures

Introduced noise via default.mixed device

Tuned for generalization using early stopping

Logged best-performing weights during training

 Evaluation

Used accuracy_score and roc_auc_score on a holdout set

Visualized raw circuit predictions

Simulated final model on qiskit.aer for a hardware-matching backend

Outcome

Stable loss convergence

Clear separation of output expectations across symmetry classes

Tested Google Cirq with and without Gradient
 Variational Quantum Classifier for Z₂ Symmetry Detection (Cirq Implementation)
This notebook implements a Variational Quantum Classifier (VQC) using Google’s Cirq framework to detect Z₂ parity symmetry in synthetic Hamiltonian feature encodings. The same classifier architecture is adapted from the PennyLane version for comparative benchmarking.

📌 Project Highlights
Quantum Framework: Cirq (1.5.0)

Symmetry Target: Z₂ parity (detect if qubit rotations are symmetric across features)

Backend: Cirq Simulator (state vector)

Optimization Strategies:

Gradient-Free: Nelder-Mead

Gradient-Based: Manual Finite-Difference

"Tested on real IBM Quantum hardware (ibm_sherbrooke) with 10,000 shots. Results exhibited uniform probability distribution across Z₂ symmetry pairs — confirming our handcrafted VQC circuit preserves parity."

AUC = 1.0 on test data with only 2-qubit model

Ready for real-hardware execution

