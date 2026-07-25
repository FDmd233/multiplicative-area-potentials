# Multiplicative Area Potentials for Edge–Point Assignments in Convex Polygons

This repository contains the note
*Multiplicative Area Potentials for Edge–Point Assignments in Convex Polygons*.

The note proves Bui's acyclicity conjecture: for a strictly convex polygon
\(P=Q_1\cdots Q_h\) with a finite point set \(A\subset\operatorname{int}(P)\),
the local process that swaps the apices of overlapping edge–point triangles
always terminates. The proof introduces the multiplicative potential

\[
\Phi(\sigma)=\prod_{i=1}^{h} h_i(\sigma(i)),
\qquad
h_i(x)=\det(Q_{i+1}-Q_i,\,x-Q_i),
\]

the product of the inward affine heights of the assigned points over their
assigned edges (equivalently, the product of twice the triangle areas). A
single two-by-two inequality does all the work: if the triangles based on
edges \(e_i,e_j\) with apices \(p,q\) overlap in their interiors, then
\(h_i(p)h_j(q)>h_i(q)h_j(p)\), so every legal swap strictly decreases
\(\Phi\).

The same potential extends to prescribed edge capacities \(c_1,\dots,c_h\),
where an extremal-ratio exchange again strictly decreases \(\Phi\) and
terminates. At a global minimum of \(\Phi\), the induced pairwise ratio
orderings yield strict separating lines under Bui's general-plus position
hypothesis; intersecting the resulting half-planes gives a short alternative
proof of Bui's convex-subdivision theorem. Taking logarithms turns the
construction into a minimum-cost transportation problem followed by
\(O(h^2)\) separator computations.

## Read

- [Note (PDF)](paper/Multiplicative_Area_Potentials_TCS.pdf) — 5 pages, two-column format

## Repository layout

```text
paper/
  Multiplicative_Area_Potentials_TCS.pdf   the note
docs/
  content-index.md                         section-by-section index of all
                                           definitions, lemmas, theorems,
                                           and displayed equations, with
                                           page references
```

## Contents at a glance

1. Introduction
2. Geometric preliminaries — affine heights (Lemma 2.1), general-plus position (Definition 2.2)
3. The local multiplicative inequality — Lemma 3.1
4. Termination of Bui's swap process — Theorem 4.1, Corollary 4.2
5. Assignments with prescribed capacities — Lemma 5.1, Theorem 5.2
6. Minimum-potential assignments and strict separators — Lemmas 6.1, 6.2
7. Edge-attached convex regions — Theorem 7.1, Corollary 7.2
8. Optimization formulation
9. Concluding remarks

A full statement-level index is in [`docs/content-index.md`](docs/content-index.md).

## Typographical notes

Three rendering glitches in the current PDF do not affect the mathematical
content:

- p. 2, §4, definition of a legal swap: the overlap condition is printed as
  `...)eq∅`; the intended reading is
  \(\operatorname{int}(\Delta_i(\sigma(i)))\cap\operatorname{int}(\Delta_j(\sigma(j)))\neq\varnothing\).
- `relint(()` appears in place of `relint(` in Lemma 2.1(iii), the proof of
  Lemma 3.1, Lemma 6.2(ii)–(iii), and the proof of Theorem 7.1.
- Lemmas are cross-referenced as "Theorem" (e.g. "Theorem 2.1" refers to
  Lemma 2.1); the numbering itself is consistent.

## References

- O. Aichholzer, F. Aurenhammer, F. Hurtado, H. Krasser, *Towards compatible
  triangulations*, Theoretical Computer Science 296 (2003) 3–13.
  [doi:10.1016/S0304-3975(02)00428-0](https://doi.org/10.1016/S0304-3975(02)00428-0)
- H. D. Bui, *On existence of a compatible triangulation with the double
  circle order type*, arXiv:2508.04602 (2025).
  [doi:10.48550/arXiv.2508.04602](https://doi.org/10.48550/arXiv.2508.04602)
