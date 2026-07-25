# Multiplicative Area Potentials for Edge–Point Assignments in Convex Polygons

Preprint and LaTeX source.

The note proves Bui's acyclicity conjecture: for a strictly convex polygon
with a finite set of interior points, the process that swaps the apices of
overlapping edge–point triangles terminates along every execution. The proof
uses the multiplicative potential
\(\Phi(\sigma)=\prod_i h_i(\sigma(i))\), where \(h_i(x)\) is the inward affine
height of \(x\) over edge \(e_i\). An overlap between two assigned triangles
forces \(h_i(p)h_j(q)>h_i(q)h_j(p)\), so each legal swap strictly decreases
\(\Phi\). The same potential settles the capacitated version of the process,
and a minimum-potential assignment yields strict pairwise separating lines,
giving an alternative proof of Bui's convex-subdivision theorem and a
transportation formulation of the construction.

## Files

- `paper/Multiplicative_Area_Potentials_TCS.pdf` -- compiled note.
- `paper/main.tex` -- LaTeX source.
- `docs/content-index.md` -- statement-level index of all definitions,
  lemmas, and theorems, with page references.

## Reproduction

```text
latexmk -pdf -interaction=nonstopmode -halt-on-error main.tex
```

## Publication record

- [v1.0.0-preprint](https://github.com/FDmd233/multiplicative-area-potentials/releases/tag/v1.0.0-preprint), dated 25 July 2026.

## References

- O. Aichholzer, F. Aurenhammer, F. Hurtado, H. Krasser, *Towards compatible
  triangulations*, Theoretical Computer Science 296 (2003) 3–13.
  [doi:10.1016/S0304-3975(02)00428-0](https://doi.org/10.1016/S0304-3975(02)00428-0)
- H. D. Bui, *On existence of a compatible triangulation with the double
  circle order type*, arXiv:2508.04602 (2025).
  [doi:10.48550/arXiv.2508.04602](https://doi.org/10.48550/arXiv.2508.04602)
