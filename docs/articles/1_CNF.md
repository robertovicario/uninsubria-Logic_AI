---
documentclass: article
lang: "en"
title: "CNF (Conjunctive Normal Form)"
subtitle: "Logic For Artificial Intelligence @ uninsubria"
author: "Roberto Vicario"
date: "2024/2025"

titlepage: true
titlepage-color: "FFFFFF"
titlepage-text-color: "000000"
titlepage-rule-color: "007161"
toc: true
toc-own-page: true
numbersections: true
colorlinks: true
linkcolor: "blue"
urlcolor: "blue"

header-includes:
    - |
      ```{=latex}
      \usepackage{tcolorbox}
      \newtcolorbox{info-box}{colback=cyan!5!white,arc=0pt,outer arc=0pt,colframe=cyan!60!black}
      \newtcolorbox{warning-box}{colback=orange!5!white,arc=0pt,outer arc=0pt,colframe=orange!80!black}
      \newtcolorbox{error-box}{colback=red!5!white,arc=0pt,outer arc=0pt,colframe=red!75!black}
      ```

pandoc-latex-environment:
    info-box: [info]
    warning-box: [warning]
    error-box: [error]
---

# CNF (Conjunctive Normal Form)

_Conjunctive Normal Form (CNF)_ is a standard way of structuring logical formulas in propositional logic. To formulate a CNF, we need to define literals and clauses:

- **Literals**: A literal is either a variable $x$ or its negation $\neg x$. Literals can be combined using logical operators and included in clauses.
- **Clauses**: A clause is a disjunction of literals.

\vspace{0.5cm}

Formalizing well, we can define a _Set Representation_ as follows:

$$
\mathcal{C} = \{l_1, l_2, \ldots, l_n\}
$$
$$
\mathcal{S} = \{C_1, C_2, \ldots, C_m\}
$$

where $\mathcal{C}$ is the set of literals and $\mathcal{S}$ is the set of clauses.

\vspace{0.5cm}

A formula in _CNF_ is a conjunction of clauses, where each clause is a disjunction of literals. A literal is either a variable or its negation:

\begin{equation}
    D = \bigwedge_{i=1}^{n} \left( \bigvee_{j=1}^{m_i} l_{i,j} \right)
\end{equation}

In other words $D = C_1 \land C_2 \land \ldots \land C_n$ where each $C_i$ is a clause $C_i = \bigvee_{j=1}^{m_i} l_{i,j}$

\vspace{0.5cm}

> **Proposition:** For every formula $H$ there exists a formula $D$ in CNF such that $H \equiv D$.

## Satisfiability

...
