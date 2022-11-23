+++
title = "Publications"
sort_by = "date"
paginate_by = 5
+++

### Conferences and Workshops

- **(2022) Introduction and Elimination, Left and Right** Klaus Ostermann, David Binder, Ingo Skupin, Tim Süberkrüb and Paul Downen. *International Conference on Functional Programming (ICFP).* [https://dl.acm.org/doi/10.1145/3547637](https://dl.acm.org/doi/10.1145/3547637)
  
  Functional programming language design has been shaped by the framework of natural deduction, in which language constructs are divided into introduction and elimination rules for producers of values.
  In sequent calculus-based languages, left introduction rules replace (right) elimination rules and provide a dedicated sublanguage for consumers of values.
  In this paper, we present and analyze a wider design space of programming languages which encompasses four kinds of rules: Introduction and elimination, both left and right. 
  We analyze the influence of rule choice on program structure and argue that having all kinds of rules enriches a programmer’s modularity arsenal.
  In particular, we identify four ways of adhering to the principle that "the structure of the program follows the structure of the data" and show that they correspond to the four possible choices of rules.
  We also propose the principle of bi-expressibility to guide and validate the design of rules for a connective.
  Finally, we deepen the well-known dualities between different connectives by means of the proof/refutation duality.

- **(2022) Structural Refinement Types** David Binder, Ingo Skupin, David Läwen, Klaus Ostermann *Full paper at the workshop for Typedriven development (TYDE)* [https://dl.acm.org/doi/10.1145/3546196.3550163](https://dl.acm.org/doi/10.1145/3546196.3550163)

  Static types are a great form of lightweight static analysis.
  But sometimes a type like List is too coarse -- we would also like to work with its *refinements* like non-empty lists, or lists containing exactly 42 elements.
  Dependent types allow for this, but they impose a heavy proof burden on the programmer.
  We want the checking and inference of refinements to be fully automatic.
  
  In this article we present a simple refinement type system and inference algorithm which uses only variants of familiar concepts from constraint-based type inference.
  Concretely, we build on the algebraic subtyping approach and extend it with typing rules which combine properties of nominal and structural type systems in a novel way.
  Despite the simplicity of our approach, the resulting type system is very expressive and allows to specify and infer non-trivial properties of programs.

- **(2021) Popper on Quantification** David Binder and Thomas Piecha. *Chapter in the book "Karl Popper's Science and Philosophy, Zuzana Parusniková and David Merrit (Eds.)* [https://doi.org/10.1007/978-3-030-67036-8_8](https://doi.org/10.1007/978-3-030-67036-8_8)
(A draft of the published paper is available [here](Binder-Piecha-Quantification.pdf))

  Karl Popper developed a new approach to mathematical logic with foundational aspirations in the 1940s, which was published in a series of articles between 1946 and 1949.
  This new system of logic did not have the influence that he had hoped for, despite being original, and despite anticipating problems which were discussed in the logic community only much later.
  In a previous article we explored in technical detail his approach to propositional logic, modal logic and various sub-classical systems like intuitionistic, dual-intuitionistic and minimal logic.
  A detailed discussion of his theory of quantification (i.e., of first-order logic) has been lacking so far.
  We first present the main ideas of Popper’s approach and the core of the propositional system.
  We then provide a concise introduction to his theory of quantification and identity, accessible to non-specialists.
  Popper’s theory of quantification underwent significant modifications over the course of his published articles, subsequent corrections to those articles, and in unpublished correspondence with other logicians.
  We present what we consider to be his most mature view on these matters, taking unpublished material into account.

- **(2020) Decomposition Diversity with Symmetric Data and Codata** Klaus Ostermann, Julian Jabs, David Binder and Ingo Skupin. *Principles of Programming Languages (POPL).* [https://doi.org/10.1145/3371098](https://doi.org/10.1145/3371098)
  
  The expression problem describes a fundamental trade-off in program design: Should a program’s primary decomposition be determined by the way its domain objects are constructed (“functional” decomposition), or by the way they are destructed (“object-oriented” decomposition)? We argue that programming languages should not force one of these decompositions on the programmer; rather, a programming language should support both ways of decomposing a program in a symmetric way, with an easy translation between these decompositions. However, current programming languages are usually not symmetric and hence make it unnecessarily hard to switch the decomposition. We propose a language that is symmetric in this regard and allows a fully automatic translation between “functional” and “object-oriented” decomposition. We present a language with algebraic data types and pattern matching for “functional” decomposition and codata types and copattern matching for “object-oriented” decomposition, together with a bijective translation that turns a data type into a codata type (“destructorization”) or vice versa (“constructorization”). We present the first symmetric programming language with support for local (co)pattern matching, which includes local anonymous function or object definitions, that allows an automatic translation as described above. We also present the first mechanical formalization of such a language and prove i) that the type system is sound, that the translations between data and codata types are ii) type-preserving, iii) behavior-preserving and iv) inverses of each other. We also extract a mechanically verified implementation from our formalization and have implemented an IDE with direct support for these translations. 

### Journals

- **(2017) Popper’s Notion of Duality and His Theory of Negations** David Binder and Thomas Piecha. *History and Philosophy of Logic 38(2).* [https://doi.org/10.1080/01445340.2016.1278517](https://doi.org/10.1080/01445340.2016.1278517)
  (A draft of the published paper is available [here](popper-hpl.pdf))
  
  Karl Popper developed a theory of deductive logic in the late 1940s. In his approach, logic is a metalinguistic theory
  of deducibility relations that are based on certain purely structural rules. Logical constants are then characterized in
  terms of deducibility relations. Characterizations of this kind are also called inferential definitions by Popper. In this
  paper, we expound his theory and elaborate some of his ideas and results that in some cases were only sketched by him.
  Our focus is on Popper’s notion of duality, his theory of modalities, and his treatment of different kinds of negation.
  This allows us to show how his works on logic anticipate some later developments and discussions in philosophical
  logic, pertaining to trivializing (tonk-like) connectives, the duality of logical constants, dual-intuitionistic logic, the
  (non-)conservativeness of language extensions, the existence of a bi-intuitionistic logic, the non-logicality of minimal
  negation, and to the problem of logicality in general.

### Monographs

- **(2022) The Logical Writings of Karl Popper** David Binder, Thomas Piecha and Peter Schroeder-Heister (Eds.) *Volume 58 of the series "Trends in Logic".* Available as an open-access book directly via [Springer](https://link.springer.com/book/10.1007/978-3-030-94926-6).
  
  This book is the first ever collection of Karl Popper's writings on deductive logic.
  Karl R. Popper (1902-1994) was one of the most influential philosophers of the 20th century. His philosophy of science ("falsificationism") and his social and political philosophy ("open society") have been widely discussed way beyond academic philosophy. What is not so well known is that Popper also produced a considerable work on the foundations of deductive logic, most of it published at the end of the 1940s as articles at scattered places. This little-known work deserves to be known better, as it is highly significant for modern proof-theoretic semantics.
  This collection assembles Popper's published writings on deductive logic in a single volume, together with all reviews of these papers. It also contains a large amount of unpublished material from the Popper Archives, including Popper's correspondence related to deductive logic and manuscripts that were (almost) finished, but did not reach the publication stage. All of these items are critically edited with additional comments by the editors. A general introduction puts Popper's work into the context of current discussions on the foundations of logic. This book should be of interest to logicians, philosophers, and anybody concerned with Popper's work.

### Miscellanea

- **(2022) Administrative Normal Forms and Focusing for Lambda Calculi** David Binder and Thomas Piecha. *Festschrift for Marie Duzi.* (Forthcoming)
- **(2018) Review of "Gentzen's Centenary: The Quest for Consistency** David Binder. *Journal for General Philosophy of Science, 49* [https://doi.org/10.1007/s10838-018-9411-6](https://doi.org/10.1007/s10838-018-9411-6)

  Review of the book "Gentzen's Centenary: The Quest for Consistency".