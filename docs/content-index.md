# Content Index

Statement-level index of the note
*Multiplicative Area Potentials for Edge–Point Assignments in Convex Polygons*
(5 pages). Page numbers refer to the PDF in [`../paper`](../paper).

## Setup and notation

- \(P=Q_1Q_2\cdots Q_h\subset\mathbb{R}^2\): strictly convex polygon, vertices
  counterclockwise; \(A\subset\operatorname{int}(P)\): finite point set.
- \(e_i=[Q_i,Q_{i+1}]\), indices modulo \(h\).
- **Inward affine height** (Eq. 1, p. 1):
  \(h_i(x)=\det(Q_{i+1}-Q_i,\,x-Q_i)\).
  For \(x\in\operatorname{int}(P)\), \(h_i(x)>0\), and \(h_i(x)/2\) is the
  Euclidean area of \(\operatorname{conv}(e_i\cup\{x\})\).
- \(\Delta_i(p)=\operatorname{conv}\{Q_i,Q_{i+1},p\}\) (p. 1).
- **Ratio** (Eq. 3, p. 2): \(\rho_{ij}(x)=h_i(x)/h_j(x)\), with positive
  denominators on \(\operatorname{int}(P)\).
- Two-dimensional sets **overlap** when their interiors intersect (p. 1);
  this excludes the shared endpoint of triangles on adjacent edges.
- **Product potential**: Eq. 6 (p. 2) for bijective assignments,
  Eq. 7 (p. 3) for capacitated assignments.
- \(K_i=\operatorname{conv}(e_i\cup S_i)\) (Eq. 8, p. 3); if \(S_i=\varnothing\)
  then \(K_i=e_i\) and \(\operatorname{int}(K_i)=\varnothing\).

## 1. Introduction (p. 1)

Bui's swap process for \(|A|=h\) ([2, Section 8.2]); the conjecture that every
sequence of legal swaps terminates (state graph acyclic); announcement of the
multiplicative-potential proof, the capacitated extension, and the route via
minimum-potential assignments to Bui's subdivision theorem [2, Theorem 4.1].
All arguments are affine.

## 2. Geometric preliminaries (pp. 1–2)

- **Lemma 2.1** (p. 1). For every \(i\):
  (i) \(h_i=0\) on the supporting line \(\operatorname{aff}(e_i)\);
  (ii) \(h_i>0\) on \(\operatorname{int}(P)\);
  (iii) if \(j\neq i\) and \(y\in\operatorname{relint}(e_i)\), then \(h_j(y)>0\).
  If \(e_i,e_j\) are nonadjacent, then \(h_j>0\) on the whole compact
  segment \(e_i\).
- **Definition 2.2** (p. 2). A finite set \(X\subset\mathbb{R}^2\) is in
  **general-plus position** if no three points of \(X\) are collinear and no
  three lines determined by three disjoint pairs of points of \(X\) are
  concurrent. Used only in Sections 6 and 7.

## 3. The local multiplicative inequality (p. 2)

- **Lemma 3.1 (Local ratio inequality)**. Let \(i\neq j\) and
  \(p,q\in\operatorname{int}(P)\). If
  \(\operatorname{int}(\Delta_i(p))\cap\operatorname{int}(\Delta_j(q))\neq\varnothing\),
  then (Eq. 4) \(\rho_{ij}(p)>\rho_{ij}(q)\); equivalently (Eq. 5)
  \(h_i(p)h_j(q)>h_i(q)h_j(p)\).
  *Proof idea:* for \(x\) in the intersection, write \(x=\alpha p+(1-\alpha)y\)
  with \(y\in\operatorname{relint}(e_i)\); then \(h_i(x)=\alpha h_i(p)\) while
  \(h_j(x)>\alpha h_j(p)\), so \(\rho_{ij}(x)<\rho_{ij}(p)\); symmetrically
  \(\rho_{ij}(x)>\rho_{ij}(q)\).
- **Remark 3.2**. The proof is affine: nonsingular affine transformations
  scale every \(h_i\) by the same determinant, leaving all ratios and
  comparisons unchanged.

## 4. Termination of Bui's swap process (p. 2)

Assume \(|A|=h\); assignments are bijections
\(\sigma:\{1,\dots,h\}\to A\).
**Potential** (Eq. 6): \(\Phi(\sigma)=\prod_{i=1}^h h_i(\sigma(i))>0\).
A **legal swap** exchanges \(\sigma(i),\sigma(j)\) for a pair whose triangle
interiors overlap.

- **Theorem 4.1 (Bui's acyclicity conjecture)**. Every sequence of legal
  swaps terminates; equivalently, the directed state graph of assignments is
  acyclic.
  *Proof:* \(\Phi(\sigma')/\Phi(\sigma)=
  h_i(q)h_j(p)\,/\,h_i(p)h_j(q)<1\) by Lemma 3.1; with only \(h!\) states, a
  strictly decreasing execution has at most \(h!-1\) swaps.
- **Corollary 4.2**. From any assignment, every selection rule reaches, after
  finitely many swaps, an assignment whose edge–point triangles have pairwise
  disjoint interiors.
- **Remark 4.3**. Under general position, Bui's "intersect" ([2, Conjecture
  8.1]) coincides with interior overlap away from the shared vertex of
  adjacent edges; Theorem 4.1 proves the conjecture in its intended sense.
  The proof needs neither general nor general-plus position.
- **Remark 4.4**. The finite-state bound gives no polynomial upper bound on
  the number of swaps; this remains open.

## 5. Assignments with prescribed capacities (pp. 2–3)

Capacities \(c_1,\dots,c_h\ge 0\) with \(\sum_i c_i=|A|\); a capacitated
assignment is a partition \(A=S_1\sqcup\cdots\sqcup S_h\), \(|S_i|=c_i\).
**Potential** (Eq. 7): \(\Phi(S_1,\dots,S_h)=\prod_i\prod_{p\in S_i}h_i(p)\).
A **conflict** is \(\operatorname{int}(K_i)\cap\operatorname{int}(K_j)\neq\varnothing\).

- **Lemma 5.1 (Extremal ratios in an edge-attached hull)**. Fix \(i\neq j\).
  (i) If \(S_i\neq\varnothing\) and \(M_i=\max_{p\in S_i}\rho_{ij}(p)\), then
  every \(x\in\operatorname{int}(K_i)\) satisfies \(\rho_{ij}(x)<M_i\).
  (ii) If \(S_j\neq\varnothing\) and \(m_j=\min_{q\in S_j}\rho_{ij}(q)\), then
  every \(x\in\operatorname{int}(K_j)\) satisfies \(\rho_{ij}(x)>m_j\).
  *Proof idea:* \(K_i\) lies in the half-plane \(h_i-M_i h_j\le 0\), and an
  interior point of a two-dimensional convex set cannot lie on its boundary
  line.
- **Theorem 5.2 (Capacitated conflict exchange)**. If
  \(\operatorname{int}(K_i)\cap\operatorname{int}(K_j)\neq\varnothing\),
  exchange \(p\in\arg\max_{u\in S_i}\rho_{ij}(u)\) with
  \(q\in\arg\min_{v\in S_j}\rho_{ij}(v)\). This preserves capacities and
  strictly decreases \(\Phi\); every such sequence terminates at an
  assignment with pairwise disjoint hull interiors.
  *Proof:* \(\rho_{ij}(p)>\rho_{ij}(x)>\rho_{ij}(q)\) for \(x\) in the
  intersection; finiteness via the \(|A|!/(c_1!\cdots c_h!)\) states.

## 6. Minimum-potential assignments and strict separators (pp. 3–4)

Fix a capacitated assignment globally minimizing \(\Phi\) (exists by
finiteness).

- **Lemma 6.1 (Pairwise ratio order)**. For distinct \(i,j\) and any
  \(p\in S_i\), \(q\in S_j\): (Eq. 9) \(\rho_{ij}(p)\le\rho_{ij}(q)\). Hence
  (Eq. 10) \(\max_{S_i}\rho_{ij}\le\min_{S_j}\rho_{ij}\) when both classes
  are nonempty. *Proof:* exchange and minimality.
- **Lemma 6.2 (Pairwise strict separator)**. Assume \(V(P)\cup A\) is in
  general-plus position. For every \(i\neq j\) there is a line \(L_{ij}\)
  with complementary closed half-planes \(H^i_{ij},H^j_{ij}\) such that
  (i) \(e_i\subset H^i_{ij}\), \(e_j\subset H^j_{ij}\);
  (ii) \(\operatorname{relint}(e_i)\cup S_i\subset\operatorname{int}(H^i_{ij})\);
  (iii) \(\operatorname{relint}(e_j)\cup S_j\subset\operatorname{int}(H^j_{ij})\).
  Adjacent edges may share an endpoint on \(L_{ij}\).
  *Proof:* if \(a=\max_{S_i}\rho_{ij}<b=\min_{S_j}\rho_{ij}\), take
  \(\{h_i=t h_j\}\) for \(t\in(a,b)\). If \(a=b=t\), the line \(L_0=\{h_i=t
  h_j\}\) contains exactly one point of each class (general position); its
  two edge supporting lines must be parallel (general-plus excludes both the
  adjacent and nonadjacent concurrency alternatives), so the compact edges
  lie strictly on their sides, and a small rotation of \(L_0\) about the
  midpoint of the two equality points yields the strict separator. Empty
  classes are handled by one-sided choices of \(t\).
- **Remark 6.3**. The separator is strictly stronger than disjoint hulls:
  every assigned point lies strictly on its class side of every pairwise
  separator, keeping all points off the final region boundaries.

## 7. Edge-attached convex regions (pp. 4–5)

- **Theorem 7.1 (Capacitated convex subdivision)**. Let
  \(P=Q_1\cdots Q_h\) be strictly convex, \(A\subset\operatorname{int}(P)\),
  \(V(P)\cup A\) in general-plus position, and \(c_1,\dots,c_h\ge 0\) with
  \(\sum_i c_i=|A|\). Then there exist two-dimensional convex polygons
  \(R_1,\dots,R_h\subset P\) such that
  (i) \(e_i\) is an edge of \(R_i\);
  (ii) no point of \(A\) lies on \(\partial R_i\);
  (iii) exactly \(c_i\) points of \(A\) lie in \(\operatorname{int}(R_i)\);
  (iv) \(\operatorname{int}(R_i)\cap\operatorname{int}(R_j)=\varnothing\) for
  \(i\neq j\).
  *Construction* (Eq. 11): take a minimum-potential assignment and set
  \(R_i=P\cap\bigcap_{j\neq i}H^i_{ij}\), with the symmetric convention
  \(H^i_{ij}=H^i_{ji}\). Then \(S_i\subset\operatorname{int}(R_i)\), points
  of other classes are strictly outside, the pairwise interiors are disjoint
  by complementarity, and a one-sided neighborhood of any midpoint of
  \(e_i\) makes \(R_i\) two-dimensional with \(R_i\cap\operatorname{aff}(e_i)
  =e_i\). The case \(c_i=0\) is unchanged.
- **Corollary 7.2**. This gives an alternative proof of Bui's
  convex-subdivision theorem [2, Theorem 4.1]. (Bui's "subdivision" need not
  cover \(P\); a central portion may remain unassigned.)

## 8. Optimization formulation (p. 5)

- Logarithms linearize the objective (Eq. 12):
  \(\log\Phi=\sum_i\sum_{p\in S_i}\log h_i(p)\).
- Transportation instance: unit supply at each \(p\in A\), demand \(c_i\) at
  each edge \(e_i\), cost (Eq. 13) \(w(p,i)=\log h_i(p)\). The
  transportation polytope is integral, so an integral minimum-cost flow is
  exactly a minimum-potential capacitated assignment (no rounding needed).
- Overall computation: one minimum-cost transportation problem, then the
  \(O(h^2)\) pairwise separators of Lemma 6.2 and the intersections (11).
  Polynomial in the comparison model (or a real-arithmetic model); no
  bit-complexity claim is made for rational coordinates, which does not
  affect the existence or termination theorems.

## 9. Concluding remarks (p. 5)

The product of edge heights is a complete descent certificate for Bui's
process; the same two-by-two multiplicative inequality also controls
capacitated exchanges and, at a global minimum, encodes the orderings behind
the strict separators. Two open questions:
(a) a polynomial upper bound on the length of every legal execution of the
swap process;
(b) extensions where polygon edges are replaced by short chains, which would
require affine or piecewise-affine gauges whose strict ratio ordering
survives overlap.

## References (p. 5)

- [1] O. Aichholzer, F. Aurenhammer, F. Hurtado, H. Krasser, *Towards
  compatible triangulations*, Theoretical Computer Science 296 (2003) 3–13.
- [2] H. D. Bui, *On existence of a compatible triangulation with the double
  circle order type*, arXiv:2508.04602v1 (2025).
