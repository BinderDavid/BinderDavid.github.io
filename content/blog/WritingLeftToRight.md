+++
title="Writing Languages From Left to Right"
date="2023-01-24"
+++

The concrete syntax of programming languages is important, but whenever you want to discuss it, you are quickly confronted with the reproach that only semantics are interesting. Cf. Wadler's law.

What I want to write about is a simple principle of language design which only concerns the concrete syntax.
The principle is reasonably simple, but basically no significant language uses it.
In the lingo of type theory it can be expressed as: The concrete syntax for all elimination forms should only add tokens to the right of the expression being eliminated.

- We mold our programming languages to our tools.
- Make a language auto-completion friendly. 
- Hole-based programming.

## Introduction and Elimination Forms

An introduction form has the following form, where the composite formula is in the conclusion of the rule.
{% katex(block=true) %}
\frac{\phi \qquad \psi}{\phi \wedge \psi}
{% end %}

Whereas an elimination form has the following form, where the composite formula is in one of the premisses.

{% katex(block=true) %}
\frac{\phi \wedge \psi}{\phi}
{% end %}

In the case for functions, the introduction and elimination forms look as follows:

{% katex(block=true) %}
\frac{\phi \to \psi \qquad \phi}{\psi}
{% end %}

## Adding Terms

{% katex(block=true) %}
\frac{\Gamma \vdash s : \phi \qquad \Gamma \vdash t : \psi}{\Gamma \vdash (s,t) : \phi \wedge \psi}
{% end %}

Also now on to elim forms:

{% katex(block=true) %}
\frac{\Gamma \vdash t : \phi \wedge \psi}{\Gamma \vdash t.\pi_1 : \phi}
{% end %}

## Some Counterexamples

Certain features in expression based languages go against this principle, so let us look at them and consider alternatives.

### If-then-else Expressions

If-then-else expressions are an elimination form for booleans, but they add a token to the left of the expression that is eliminated.
{% katex(block=true) %}
\frac{\Gamma \vdash b : \mathbb{B} \qquad \Gamma \vdash e_1 : \sigma \qquad \Gamma \vdash e_2 : \sigma}{\Gamma \vdash \mathbf{if}\ b\ \mathbf{then}\ e_1\ \mathbf{else}\ e_2 : \phi \wedge \psi}
{% end %}

### Case Expressions

{% katex(block=true) %}
\frac{\Gamma \vdash b : \mathbb{B} \qquad \Gamma \vdash e_1 : \sigma \qquad \Gamma \vdash e_2 : \sigma}{\Gamma \vdash \mathbf{if}\ b\ \mathbf{then}\ e_1\ \mathbf{else}\ e_2 : \phi \wedge \psi}
{% end %}

### Dereferencing







