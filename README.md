# Thermal Stability of Nuclear Reactors

**A 101-page technical monograph** on coupled neutronic–thermal reactor dynamics,
stability theory, and the historical lessons of the Chernobyl accident.

📄 **[Read the PDF »](thermal-stability-of-nuclear-reactors.pdf)**

---

## About

This monograph develops the theory of reactor thermal stability from first
principles and uses it to dissect the Chernobyl Unit 4 accident (26 April 1986).
The central thesis: *a reactor is thermally stable when rising temperature removes
reactivity faster than rising power can add it* — and Chernobyl is the story of a
machine in which that inequality was reversed.

It is written for advanced undergraduates, graduate students, and engineers, at
roughly graduate-textbook depth, with derivations, worked numerical examples,
figures, and end-of-chapter exercises.

## Contents

The book is organised into five parts plus appendices:

- **I — Foundations:** reactor physics, point reactor kinetics, the inhour
  equation, delayed neutrons, decay heat.
- **II — Heat transport & feedback:** fuel/coolant thermal models, and the
  Doppler, moderator, and void reactivity coefficients.
- **III — Stability theory:** linearisation, transfer functions and the Nyquist
  criterion, the Nordheim–Fuchs power excursion, xenon spatial oscillations,
  control & protection systems, and measurement of feedback coefficients.
- **IV — Historical lessons:** earlier stability incidents, the RBMK-1000 design,
  the Chernobyl accident, its root-cause analysis (INSAG-1 → INSAG-7), and the
  decay-heat accidents at Three Mile Island and Fukushima.
- **V — Modern practice:** inherent and passive safety, computational modelling,
  and synthesis.
- **Appendices:** delayed-neutron data, derivations, a detailed Chernobyl
  timeline, worked numerical examples, and a glossary.

## Repository structure

```
.
├── thermal-stability-of-nuclear-reactors.pdf   # the compiled book (read this)
├── src/
│   ├── main.tex            # master file (preamble, structure)
│   ├── chapters/           # one .tex per chapter / appendix
│   └── figures/            # figures (PNG)
├── README.md
└── LICENSE
```

## Building from source

Requires a LaTeX distribution (TeX Live or MiKTeX). From `src/`:

```bash
pdflatex main.tex
pdflatex main.tex   # run 2–3 times to resolve the TOC and cross-references
pdflatex main.tex
```

No bibliography tool is needed; references are embedded.

## Companion code

Several figures (the transient gallery and the inhour-equation validation) were
produced with the author's open-source point-kinetics toolkit,
[**reactor-kinetics**](https://github.com/amir-koutahi/reactor-kinetics).

## License

The text and figures are released under
**[Creative Commons Attribution 4.0 (CC BY 4.0)](LICENSE)**. You may share and
adapt the material with attribution.

> **Disclaimer.** This is an educational and historical treatment of reactor
> dynamics and safety. It is *not* a design specification, operating procedure, or
> safety-analysis document, and must not be used as one.
