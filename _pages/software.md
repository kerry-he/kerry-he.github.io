---
layout: archive
title: "Software"
permalink: /software/
author_profile: true
---

{% include base_path %}

Below, I list some open-source software projects that I have worked on.

# Quantum Information Conic Solver

QICS is a primal-dual interior point solver fully implemented in Python, and is specialized towards problems arising in quantum information theory. Features of QICS include

- **Efficient quantum relative entropy programming**
  
  We support optimizing over the quantum relative entropy cone, as well as related cones including the quantum conditional entropy cone, as well as slices of the quantum relative entropy cone that 
arise when solving quantum key rates of quantum cryptographic protocols. Numerical results show that QICS solves problems much faster than existing quantum relative entropy programming solvers, such as Hypatia, DDS, and CVXQUAD.

- **Efficient semidefinite programming**

  We implement an efficient semidefinite programming solver which utilizes state-of-the-art techniques for symmetric cone programming, including using Nesterov-Todd scalings and exploiting sparsity in the problem structure. Numerical results show that QICS has comparable performance to state-of-the-art semidefinite programming software, such as MOSEK, SDPA, SDPT3 and SeDuMi.

- **Complex-valued matrices**

  Users can specify whether cones involving symmetric matrices, such as the positive semidefinite cone or quantum relative entropy cone, are real-valued or complex-valued (i.e., Hermitian). Support for Hermitian matrices is embedded directly in the definition of the cone, which can be more computationally efficient than lifting into the real-valued symmetric cone.

See the links below for further information.

[Source code](https://github.com/kerry-he/qics){: .btn--research}
[Documentation](https://qics.readthedocs.io/en/stable/){: .btn--research}
