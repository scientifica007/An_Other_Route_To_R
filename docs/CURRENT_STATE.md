# CURRENT STATE

_Last updated: 2026-08-30_

## Current phase

**Foundational literature review and route comparison.**

The project has not yet adopted a new construction of \(\mathbb{R}\). A first broad literature search has now been completed and documented in [`LITERATURE_REVIEW_2026-08-30.md`](LITERATURE_REVIEW_2026-08-30.md).

## Governing question

How can one construct the real numbers from \(\mathbb{N}\), \(\mathbb{Z}\), or \(\mathbb{Q}\) through mechanisms whose primitive object is not a Dedekind cut or a Cauchy sequence?

## Current working observations

1. A finite algebraic closure of \(\mathbb{Q}\) cannot by itself produce all of \(\mathbb{R}\); some source of infinite information/completion is unavoidable if the target is the full continuum.
2. Infinite processes need not be represented specifically by Cauchy sequences.
3. The literature contains numerous constructions beyond the textbook pair Dedekind/Cauchy, but their foundational independence varies substantially.
4. The strongest currently identified family for this project is the Eudoxus/Schanuel/Street construction using near-endomorphisms or almost homomorphisms \(\mathbb{Z}\to\mathbb{Z}\) modulo bounded error.
5. Continued fractions, de Bruijn additive expansions, and the Faltin–Metropolis–Ross–Rota string/wreath construction are also high-value alternatives.
6. Shiu, Pintilie, Engel/Sylvester, alternating-series, and infinite-product constructions form an important family of expansion-based models, but many recover operations/completeness through approximation, null sequences, or suprema.
7. Nested rational intervals and Cauchy filters should not be counted as strong alternatives: they are close variants of completion. Maier–Maier is essentially Dedekind without canonical representatives.
8. Arthan's 2001 “irrational construction” changes the intermediate algebraic ring but still explicitly uses Dedekind cuts, so it does not satisfy the strict project criterion.
9. A targeted first search did not locate an established **integration-first construction** of \(\mathbb{R}\) in which integration/Riemann accumulation is the primitive bridge from \(\mathbb{N}\), \(\mathbb{Z}\), or \(\mathbb{Q}\). This is a provisional negative search result, not a nonexistence theorem.
10. A central distinction must always be maintained between representation, model construction, completion mechanism, and genuinely distinct foundational mechanism.

## Priority routes after literature review

### Priority 1 — Eudoxus / near-endomorphisms / quasimorphisms

Primitive object: a map
\[
f:\mathbb{Z}\to\mathbb{Z}
\]
with bounded additive defect, modulo bounded difference.

Why first: it starts directly from integers; no rational intermediate stage is needed; the real number is encoded in global large-scale behavior rather than as a cut or Cauchy limit object. Later work also generalizes the mechanism to field completions.

### Priority 2 — Rieger continued fractions

Primitive data: finite/infinite continued-fraction expansions built from integers/natural numbers.

Key issue: determine exactly where completeness/suprema enter, so that representation novelty is not confused with foundational novelty.

### Priority 3 — de Bruijn additive expansions

Primitive data: digit/additive expansions directly from integer data, explicitly avoiding a prior rational construction.

### Priority 4 — Faltin–Metropolis–Ross–Rota

Primitive data: integer-coefficient strings/formal Laurent-type series modulo carrying relations.

## Secondary comparison families

- Engel and Sylvester series constructions.
- Alternating Engel/Sylvester constructions.
- Infinite-product constructions.
- Shiu/Pintilie subseries constructions.
- Domain-theoretic interval-domain reals.
- Nonstandard/ultrafilter quotient constructions.
- Reals by abstraction / ratios of magnitudes.
- Decimal/binary/bicimal constructions, including recent work by Klazar and Panza.

## Immediate next research task

Produce a rigorous **foundational decomposition** of the Eudoxus/near-endomorphism construction covering:

- exact primitive structure required from \(\mathbb{Z}\);
- definition of slope/near-endomorphism;
- bounded-error equivalence;
- construction of addition and multiplication;
- order;
- embedding of \(\mathbb{Z}\) and emergence of \(\mathbb{Q}\);
- multiplicative inverses;
- Archimedean property;
- proof of completeness;
- exact point at which infinity enters;
- whether the construction is best interpreted as a fundamentally new mechanism or as a disguised/generalized completion;
- which pieces could be reused in a genuinely new route.

Only after that should the same decomposition be applied to Rieger and de Bruijn/FMRR.
