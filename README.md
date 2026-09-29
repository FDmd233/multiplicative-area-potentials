# Multiplicative Area Potentials for Edge--Point Assignments in Convex Polygons

This repository contains a preprint proving Bui's acyclicity conjecture for edge--point swaps in a strictly convex polygon.

Let the polygon edges be $e_1,\dots,e_m$, and let $h_i(x)$ denote the inward affine height of a point $x$ above $e_i$. For an assignment $\sigma$, define the multiplicative potential

$$
\Phi(\sigma)=\prod_i h_i\bigl(\sigma(i)\bigr).
$$

If two assigned edge--point triangles overlap, then the corresponding points $p,q$ satisfy

$$
h_i(p)h_j(q)>h_i(q)h_j(p),
$$

so swapping the two assigned apices strictly decreases $\Phi$. This proves termination of every legal swap sequence.

The same potential also settles the capacitated variant. In addition, a minimum-potential assignment yields strict pairwise separating lines, giving an alternative proof of Bui's convex-subdivision theorem and a transportation formulation of the construction.

## Manuscript

- [PDF](paper/Multiplicative_Area_Potentials_TCS.pdf)
- [LaTeX source](paper/main.tex)
- [Statement index](docs/content-index.md)

## Build

~~~bash
cd paper
latexmk -pdf -interaction=nonstopmode -halt-on-error main.tex
~~~

## Publication record

- [`v1.0.0-preprint`](https://github.com/FDmd233/multiplicative-area-potentials/releases/tag/v1.0.0-preprint), dated 25 July 2026.

## References

- O. Aichholzer, F. Aurenhammer, F. Hurtado, H. Krasser, *Towards compatible triangulations*, Theoretical Computer Science **296** (2003), 3--13. [DOI](https://doi.org/10.1016/S0304-3975(02)00428-0)
- H. D. Bui, *On existence of a compatible triangulation with the double circle order type*, arXiv:2508.04602 (2025). [DOI](https://doi.org/10.48550/arXiv.2508.04602)
