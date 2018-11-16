# CSL with model-based reasoning
This repository hosts soundness proofs for CSL (Concurrent Separation Logic) with model-based reasoning. This is a program logic that extends on classical/standard CSL by having inference rules to verify whether a program adheres to an abstract model. Process algebra terms are used as the abstract models. The program logic can be used to reason about concurrent and distributed, possibly non-terminating, software. The soundness proof is mechanised in the Coq proof assistant (version 8.6).

## Structure
- **Statics.v** defines the syntax of the language (expressions and statements), together with related operations, e.g. substitution, free variables, etc.
- **Dynamics.v** defines the denotational semantics of expressions and the operational semantics of language statements. In particular, three different operational semantics are defined for statements, and we show how they relate.
- **Assertions.v** defines the syntax and semantics of the assertion language of our program logic. Also contains substitution, logical entailment, and soundness of the laws of bunched implications.
- **Process.v** defines a theory on process algebras with data. This file contains a syntax and operational semantics for process algebras, a definition of bisimulation, a proof that bisimulation is a congruence, and a soundness proof for our axiomatisation.
- **Permissions.v** contains lemmas and theories on fractional permissions, process permissions, and other related variants.
- **Heap.v** contains definitions and theories on heaps, heap masks, and permission heaps.
- **ProcessMap.v** contains definitions and theories regarding process maps, process masks, and permission process maps.
- **Soundness.v** defines the meaning of Hoare triples and contains the actual soundness proof.

## Contact
For any questions and support, contact [Wytse Oortwijn](http://wwwhome.ewi.utwente.nl/~oortwijnwhm/) by emailing to `w.h.m.oortwijn at utwente dot nl`.
