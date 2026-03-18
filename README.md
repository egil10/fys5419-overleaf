# FYS5419 — A VQE Study of the Lipkin Interaction

LaTeX source for the project report submitted for **FYS5419: Quantum Computing and Quantum Machine Learning** at the University of Oslo, Spring 2026.

**Author:** Egil Furnes (`egilsf@uio.no`)

---

## Repositories

| Purpose | URL |
|---|---|
| This report (LaTeX source) | https://github.com/egil10/fys5419-overleaf |
| Code & experiments | https://github.com/egil10/fys5419 |

The Overleaf project is synced to this repository. All `.tex` files are edited on Overleaf and mirrored here for version control and AI-assisted review.

---

## Report structure

| File | Contents |
|---|---|
| `00-MAIN.tex` | Root document — packages, layout, input chain |
| `01-FRONTMATTER.tex` | Title, author, abstract |
| `10-INTRO.tex` | Introduction |
| `11-METHOD.tex` | Methods — circuits, VQE, Lipkin Hamiltonian, implementation |
| `12-RESULT.tex` | Results |
| `13-NUMERICAL-STABILITY.tex` | Numerical stability analysis |
| `14-CONCLUSION.tex` | Conclusion and future work |
| `99-APPENDIX.tex` | Appendix — VQE algorithm, figures, Python environment |
| `bib.bib` | Bibliography |
| `figures/` | All figures used in the report |
| `article/` | Supporting article material |
| `project/` | Project description |

---

## Abstract

This project studies the Lipkin–Meshkov–Glick model using the Variational Quantum Eigensolver (VQE) algorithm on a sequence of increasingly complex quantum systems. Starting from single-qubit operations and Bell state entanglement, the work progresses through a two-level Hamiltonian with an avoided crossing, a two-qubit interacting system, and finally the *J* = 1 and *J* = 2 Lipkin Hamiltonians mapped onto two and four qubits respectively.

Classical diagonalization achieves machine-precision accuracy (~10⁻¹⁵) throughout and serves as the reference. Hardware-efficient VQE circuits based on *R*_y rotations and entangling gates reproduce exact ground state energies to ~10⁻¹¹ for the two-level Hamiltonian and the Lipkin *J* = 1 system. For the two-qubit Hamiltonian the VQE achieves machine precision for λ ≲ 0.4 but undergoes a branch-tracking failure at the avoided crossing. For the *J* = 2 Lipkin model the residual error is ~10⁻², reflecting optimization in a high-dimensional symmetry-mixed landscape.

---

## Building the PDF

The report is compiled on Overleaf. To build locally:

```bash
pdflatex 00-MAIN.tex
biber 00-MAIN
pdflatex 00-MAIN.tex
pdflatex 00-MAIN.tex
```

Requires a standard LaTeX distribution (TeX Live / MiKTeX) with `biblatex` and `biber`.

---

## Course

**FYS5419 — Quantum Computing and Quantum Machine Learning**
Department of Physics, University of Oslo
https://github.com/CompPhysics/QuantumComputingMachineLearning
