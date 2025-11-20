+++
title = "Publications"
sort_by = "date"
paginate_by = 5
+++

### Conferences and Workshops

- **(2025) Filling the Gaps of Polarity: Implementing Dependent Data and Codata Types with Implicit Arguments** Bohdan Liesnikov, David Binder and Tim Süberkrüb. *Programming '26* [Published Version](https://doi.org/10.22152/programming-journal.org/2025/10/19)

  The expression problem describes a fundamental tradeoff between two types of extensibility: extending a type with new operations, such as by pattern matching on an algebraic data type in functional programming, and extending a type with new constructors, such as by adding a new object implementing an interface in object-oriented programming. Most dependently typed languages have good support for the former style through inductive types, but support for the latter style through coinductive types is usually much poorer. Polarity is a language that treats both kinds of types symmetrically and allows the developer to switch between type representations.However, it currently lacks several features expected of a state-of-the-art dependently typed language, such as implicit arguments. The central aim of this paper is to provide an algorithmic type system and inference algorithm for implicit arguments that respect the core symmetry of the language. Our work provides two key contributions: a complete algorithmic description of the type system backing Polarity, and a comprehensive description of a unification algorithm that covers arbitrary inductive and coinductive types. We give rules for reduction semantics, conversion checking, and a unification algorithm for pattern-matching, which are essential for a usable implementation. A work-in-progress implementation of the algorithms in this paper is available at polarity-lang.github.io. We expect that the comprehensive account of the unification algorithm and our design decisions can serve as a blueprint for other dependently typed languages that support inductive and coinductive types symmetrically.

- **(2025) The Algebra of Patterns** David Binder and Lean Ermantraut. *ECOOP '25* [Extended Version](https://arxiv.org/abs/2504.18920) [Rocq Proofs](https://zenodo.org/records/15308861) [Official Version (LIPIcs)](https://doi.org/10.4230/LIPIcs.ECOOP.2025.2) [Artifact Description (DARTS)](https://doi.org/10.4230/DARTS.11.2.10)

  Pattern matching is a popular feature in functional, imperative and object-oriented programming languages.
  Language designers should therefore invest effort in a good design for pattern matching.
  Most languages choose a *first-match semantics* for pattern matching; that is, clauses are tried in the order in which they appear in the program until the first one matches.
  As a consequence, the order in which the clauses appear cannot be arbitrarily changed, which results in a less declarative programming model.
  The declarative alternative to this is an *order-independent semantics* for pattern matching, which is not implemented in most programming languages since it requires more verbose patterns.
  The reason for this verbosity is that the syntax of patterns is usually not expressive enough to express the *complement* of a pattern.
  In this paper, we show a principled way to make order-independent pattern matching practical.
  Our solution consists of two parts:
  First, we introduce a *boolean algebra of patterns* which can express the complement of a pattern.
  Second, we introduce *default clauses* to pattern matches.
  These default clauses capture the essential idea of a fallthrough case without sacrificing the property of order-independence.

- **(2024) Grokking the Sequent Calculus (Functional Pearl)** David Binder, Marco Tzschentke, Marius Müller and Klaus Ostermann. *ICFP '24* [Preprint](https://arxiv.org/abs/2406.14719) [https://doi.org/10.1145/3674639](https://doi.org/10.1145/3674639)


  The sequent calculus is a proof system which was designed as a more symmetric alternative to natural deduction.
  The λμμ-calculus is a term assignment system for the sequent calculus and a great foundation for compiler intermediate languages due to its first-class representation of evaluation contexts.
  Unfortunately, only experts of the sequent calculus can appreciate its beauty. To remedy this, we present the first
  introduction to the λμμ-calculus which is not directed at type theorists or logicians but at compiler hackers and programming-language enthusiasts. We do this by writing a compiler from a small but interesting surface language to the λμμ-calculus as a compiler intermediate language.

- **(2024) Deriving Dependently-Typed OOP from First Principles** David Binder, Ingo Skupin, Tim Süberkrüb and Klaus Ostermann.*OOPSLA '24* [Extended Version with Additional Appendices](https://arxiv.org/abs/2403.06707) [https://dl.acm.org/doi/10.1145/3649846](https://dl.acm.org/doi/10.1145/3649846)

  🏆 *The artifact for this paper won a distinguished artifact award.*

  The expression problem describes how most types can easily be extended with new ways to produce the type or new ways to consume the type, but not both. When abstract syntax trees are defined as an algebraic data type, for example, they can easily be extended with new consumers, such as print or eval, but adding a new constructor requires the modification of all existing pattern matches. The expression problem is one way to elucidate the difference between functional or data-oriented programs (easily extendable by new consumers) and object-oriented programs (easily extendable by new producers). This difference between programs which are extensible by new producers or new consumers also exists for dependently typed programming, but with one core difference: Dependently-typed programming almost exclusively follows the functional programming model and not the object-oriented model, which leaves an interesting space in the programming language landscape unexplored. In this paper, we explore the field of dependently-typed object-oriented programming by deriving it from first principles using the principle of duality. That is, we do not extend an existing object-oriented formalism with dependent types in an ad-hoc fashion, but instead start from a familiar data-oriented language and derive its dual fragment by the systematic use of defunctionalization and refunctionalization. Our central contribution is a dependently typed calculus which contains two dual language fragments. We provide type- and semantics-preserving transformations between these two language fragments: defunctionalization and refunctionalization. We have implemented this language and these transformations and use this implementation to explain the various ways in which constructions in dependently typed programming can be explained as special instances of the general phenomenon of duality.


- **(2023) Getting Into the Flow: Towards Better Type Error Messages for Constraint-Based Type Inference** Ishan Bhanuka, Lionel Parreaux, David Binder and Jonathan Immanuel Brachthäuser *OOPSLA '23* [Preprint](GettingIntoTheFlow.pdf) [https://dl.acm.org/doi/10.1145/3622812](https://dl.acm.org/doi/10.1145/3622812) [Extended Tech Report](https://arxiv.org/abs/2402.12637)

  Creating good type error messages for constraint-based type inference systems is difficult.
  Typical type error messages reflect implementation details of the underlying constraint-solving algorithms rather than the
  specific factors leading to type mismatches. We propose using subtyping constraints that capture data flow to
  classify and explain type errors. Our algorithm explains type errors as faulty data flows, which programmers
  are already used to reasoning about, and illustrates these data flows as sequences of relevant program locations.
  We show that our ideas and algorithm are not limited to languages with subtyping, as they can be readily
  integrated with Hindley-Milner type inference. In addition to these core contributions, we present the results of
  a user study to evaluate the quality of our messages compared to other implementations. While the quantitative
  evaluation does not show that flow-based messages improve the localization or understanding of the causes
  of type errors, the qualitative evaluation suggests a real need and demand for flow-based messages.

- **(2022) Introduction and Elimination, Left and Right** Klaus Ostermann, David Binder, Ingo Skupin, Tim Süberkrüb and Paul Downen. *International Conference on Functional Programming (ICFP).* [https://dl.acm.org/doi/10.1145/3547637](https://dl.acm.org/doi/10.1145/3547637)

  Functional programming language design has been shaped by the framework of natural deduction, in which language constructs are divided into introduction and elimination rules for producers of values.
  In sequent calculus-based languages, left introduction rules replace (right) elimination rules and provide a dedicated sublanguage for consumers of values.
  In this paper, we present and analyze a wider design space of programming languages which encompasses four kinds of rules: Introduction and elimination, both left and right.
  We analyze the influence of rule choice on program structure and argue that having all kinds of rules enriches a programmer’s modularity arsenal.
  In particular, we identify four ways of adhering to the principle that "the structure of the program follows the structure of the data" and show that they correspond to the four possible choices of rules.
  We also propose the principle of bi-expressibility to guide and validate the design of rules for a connective.
  Finally, we deepen the well-known dualities between different connectives by means of the proof/refutation duality.

- **(2022) Structural Refinement Types** David Binder, Ingo Skupin, David Läwen, Klaus Ostermann *Full paper at the workshop for Typedriven development (TYDE)* [https://dl.acm.org/doi/10.1145/3546196.3550163](https://dl.acm.org/doi/10.1145/3546196.3550163) [Preprint](structural-refinement-types.pdf)

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

- **(2024) Programming with Symmetric Data and Codata Types** David Binder. Thesis submitted for the degree of Dr. rer. nat. at the University of Tübingen. [Link to published version](http://dx.doi.org/10.15496/publikation-100270).

- **(2022) Data-Codata Symmetry and its Interaction with Evaluation Order** David Binder, Julian Jabs, Ingo Skupin and Klaus Ostermann. Tech report published on arXiv: [https://doi.org/10.48550/arXiv.2211.13004](https://doi.org/10.48550/arXiv.2211.13004)

  Data types and codata types are, as the names suggest, often seen as duals of each other. However, most programming languages do not support both of them in their full generality, or if they do, they are still seen as distinct constructs with separately defined type-checking, compilation, etc. Rendel et al. were the first to propose variants of two standard program transformations, de- and refunctionalization, as a test to gauge and improve the symmetry between data and codata types. However, in previous works, codata and data were still seen as separately defined language constructs, with de- and refunctionalization being defined as similar but separate algorithms. These works also glossed over interactions between the aforementioned transformations and evaluation order, which leads to a loss of desirable η expansion equalities. We argue that the failure of complete symmetry is due to the inherent asymmetry of natural deduction as the logical foundation of the language design. Natural deduction is asymmetric in that its focus is on producers (proofs) of types, whereas consumers (contexts, continuations, refutations) have a second-class status. Inspired by existing sequent-calculus-based language designs, we present the first language design that is fully symmetric in that the issues of polarity (data type vs codata types) and evaluation order (call-by-value vs call-by-name) are untangled and become independent attributes of a single form of type declaration. Both attributes, polarity and evaluation order, can be changed independently by one algorithm each. In particular, defunctionalization and refunctionalization are now one algorithm. Evaluation order can be defined and changed individually for each type, independently from polarity. By allowing only certain combinations of evaluation order and polarity, the aforementioned η laws can be restored.


- **(2022) Administrative Normal Forms and Focusing for Lambda Calculi** David Binder and Thomas Piecha. In *Logically Speaking. A Festschrift for Marie Duží.* Pavel Materna and Bjørn Jespersen (Eds.) College Publications. [Link to publisher](https://www.collegepublications.co.uk/tributes/?00049). [PDF Draft](Binder-Piecha-ANF-Focusing.pdf).

  The Curry-Howard correspondence between deductive systems and computational calculi is one of the great unifying ideas.
  It links purely logical investigations to practical problems in computer science, in particular the design and implementation of programming languages.
  Many aspects of this correspondence are widely known, such as the correspondence between natural deduction for intuitionistic logic and the simply typed lambda-calculus.
  On the other hand, the importance of the sequent calculus in proof-theoretic investigations is not yet reflected in the study of programming languages, where languages based on the lambda-calculus dominate.
  One of the principal reasons for this is, we think, the lack of introductory material that could serve in helping to translate between logicians and programming language theorists.

  Our small contribution in this respect is to introduce and expose the correspondence between two normal forms and their respective normalization procedures: administrative normal form and ANF-transformation on the one hand, and focused normal form and static focusing on the other.
  Though invented for different purposes, compiler optimizations in the case of the ANF-transformation and proof search in the case of focusing, they are structurally very similar.
  Both transformations bring proofs into a normal form where functions and constructors are only applied to values and where computations are sequentialized.
  In this paper we make this similarity explicit.

- **(2018) Review of "Gentzen's Centenary: The Quest for Consistency** David Binder. *Journal for General Philosophy of Science, 49* [https://doi.org/10.1007/s10838-018-9411-6](https://doi.org/10.1007/s10838-018-9411-6)

  Review of the book "Gentzen's Centenary: The Quest for Consistency".
