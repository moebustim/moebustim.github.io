---
layout: talks
title: Talks
permalink: /talks/
last_updated: January 2026
description: This page presents a selected list of talks I have given in recent years. Similar talks are summarized in a single entry for readability.

talks:
    - title: "Heisenberg-limited Hamiltonian learning CV systems"
      meta:
        - text: "QIP 2026"
          url: "https://qip2026.lu.lv/"
        - "Riga"
        - "01.26"
        - "|"
        - "CQIF Group Meeting"
        - "Cambridge"
        - "10.25"
        - "|"
        - text: "QMATH16"
          url: "https://sites.google.com/view/qmath16/home"
        - "Munich"
        - "09.25"
      description: "These talks addressed the fundamental task in quantum learning theory of identifying the Hamiltonian governing a quantum time evolution. Previous research has focused on discrete quantum spin systems, while comparatively little is known about continuous‑variable systems. Focusing on the latter, infinite‑dimensional Hilbert spaces and unbounded operators introduce significant technical challenges. We introduce an analytic framework to study the effects of strong dissipation in such systems, enabling a rigorous analysis of cat‑qubit stabilization via engineered dissipation. Building on this, we develop Heisenberg‑limited algorithms for learning general bosonic Hamiltonians with higher‑order terms in the creation and annihilation operators. Our approach ensures efficient scaling with both the number of modes and the precision of the reconstructed coefficients. Additionally, we derive a new adiabatic approximation for Lindbladian evolutions and explore potential experimental implementations."

    - title: "Dissipation-enabled bosonic Hamiltonian learning via new information-propagation bounds"
      meta:
        - text: "TQC 2024"
          url: "https://groups.oist.jp/ocqt/event/conference-theory-quantum-computation-communication-and-cryptography-tqc2024"
        - "Okinawa"
        - "09.24"
        - "|"
        - text: "QMATH Masterclass"
          url: "https://qmath.ku.dk/events/quantum-learning-theory/"
        - "Copenhagen"
        - "08.23"
      youtube_id: "XnyQFTr7pqE"
      description: "Reliable quantum technologies require understanding the dynamics of the underlying system, a task known as Hamiltonian learning. While well studied for multi‑qubit systems, learning guarantees for bosonic dynamics remain largely unexplored. For m-mode Hamiltonians given as polynomials in creation and annihilation operators, we establish a simple moment criterion—formulated via the particle‑number operator—that allows finite‑dimensional learning strategies to extend to the bosonic setting using only coherent states and heterodyne detection. We further introduce a dissipation‑assisted procedure that succeeds even when this criterion is violated, learning all Hamiltonian coefficients to accuracy $\\varepsilon$  in total evolution time $\\mathcal{O}(\\varepsilon ^{-2}\\log m)$. The protocol uses experimentally accessible ingredients such as projected coherent states, photon‑driven dissipative regularization inspired by cat‑qubit stabilization, and heterodyne measurements. A key technical contribution is a new bosonic Lieb–Robinson‑type bound for Hamiltonians of bounded degree combined with driven dissipation. Overall, our results show that a broad class of bosonic Hamiltonians can be efficiently learned from simple continuous‑variable experiments."
    
    - title: "Energy preserving evolutions of Bosonic systems"
      meta:
        - text: QMATH QLunch Seminar
          url: "https://qmath.ku.dk/events/quantum-lunch/?event_type=&fromdate=20.11.2023&todate=04.01.2027&year_month="
        - "Copenhagen"
        - "11.23"
      description: The exponential convergence to invariant subspaces of quantum Markov semigroups plays a crucial role in quantum information theory. One such example is in bosonic error correction schemes, where dissipation is used to drive states back to the codespace - an invariant subspace protected against certain types of errors. In this paper, we investigate perturbations of quantum dynamical semigroups that operate on continuous variable (CV) systems and admit an invariant subspace. First, we prove a generation theorem for quantum Markov semigroups on CV systems under the physical assumptions that (i) the generator has GKSL form with corresponding jump operators defined as polynomials of annihilation and creation operators; and (ii) the (possibly unbounded) generator increases all moments in a controlled manner. Additionally, we show that the level sets of operators with bounded first moments are admissible subspaces of the evolution, providing the foundations for a perturbative analysis. Our results also extend to time-dependent semigroups. We apply our general framework to two settings of interest in continuous variables quantum information processing. First, we provide a new scheme for deriving continuity bounds on the energy-constrained capacities of Markovian perturbations of Quantum dynamical semigroups. Second, we provide a quantitative analysis of the dampening of continuous-time evolutions generating a universal gate set for cat-qubits outside their code-space.

    - title: "Fermionic Entropic Inequalities"
      meta:
        - text: "BIID in Information Theory 11"
          url: "https://sites.google.com/view/beyondiid11"
        - "Tübingen"
        - "07.23"
      description: Entropic inequalities play an important role in the establishment of the optimal transmission rates of classical and quantum information. Motivated by the key role of the constrained minimum output entropy in the study of the capacity region of bonsonic Gaussian broadcast channel, we study similar inequalities in the Fermionic case. In this paper, we prove the fermionic, multi-mode version of the Entropy Power Inequality, the Entropy Photon-Number Inequality, constrained minimum output entropy, and Young's inequality for even Gaussian input states satisfying the parity super selection rule. We also prove hypercontractivity for states satisfying the SSR given that the 2-log-Sobolev constant is known in 1-mode. Finally, we establish the generalized subadditivity of the conditional entropy, and gradient estimate of even Gaussian channels on fermionic systems.

    - title: "Optimal convergence rate in the quantum Zeno effect for open quantum systems in infinite dimensions"
      meta:
        - text: "QMATH 15"
          url: "https://www.math.ucdavis.edu/~qmath/"
        - "Davis"
        - "09.22"
        - "|"
        - text: "IAMP Summer School"
          url: "https://collab.dvb.bayern/spaces/TUMqimp20/pages/67808645/IAMP+%E2%80%93+EMS+Summer+School+in+Mathematical+Physics+2022"
        - "Munich"
        - "09.22"
        - "|"
        - text: "Quantum Alliance PhD Conference"
          url: "https://www.quantum-alliance.de/news-and-events/events/phd-conference-2022.html"
        - "Munich"
        - "04.22"
        - "|"
        - text: "DPG Meeting 2022"
          url: "https://www.dpg-physik.de/aktivitaeten-und-programme/tagungen/fruehjahrstagungen/2022"
        - "Regensburg"
        - "02.22"
      description: "In open quantum systems, the quantum Zeno effect consists in frequent applications of a given quantum operation, e.g. a measurement, used to restrict the time evolution (due e.g. to decoherence) to states that are invariant under the quantum operation. In an abstract setting, the Zeno sequence is an alternating concatenation of a contraction operator (quantum operation) and a $C_0$-contraction semigroup (time evolution) on a Banach space. In this paper, we prove the optimal convergence rate of order $1/n$of the Zeno sequence by proving explicit error bounds. For that, we derive a new Chernoff-type $\\sqrt{n}$-Lemma, which we believe to be of independent interest. Moreover, we generalize the convergence result for the Zeno effect in two directions: We weaken the assumptions on the generator, inducing the Zeno dynamics generated by an unbounded generator and we improve the convergence to the uniform topology. Finally, we provide a large class of examples arising from our assumptions."
---

