# Reading list: Bayesian marketing mix modeling

The papers behind modern Bayesian MMM, in the order I'd read them.

## Foundations (Google, 2017)

1. **[Bayesian Methods for Media Mix Modeling with Carryover and Shape Effects](https://research.google/pubs/bayesian-methods-for-media-mix-modeling-with-carryover-and-shape-effects/)**: Jin, Wang, Sun, Chan, Koehler. The adstock + saturation formulation that most Bayesian MMMs still use.
2. **[Geo-level Bayesian Hierarchical Media Mix Modeling](https://research.google/pubs/geo-level-bayesian-hierarchical-media-mix-modeling/)**: Sun, Wang, Jin, Chan, Koehler. Using regional data to get more variation and tighter estimates than national data allows.
3. **[A Hierarchical Bayesian Approach to Improve Media Mix Models Using Category Data](https://research.google/pubs/a-hierarchical-bayesian-approach-to-improve-media-mix-models-using-category-data/)**: Wang, Jin, Sun, Chan, Koehler. Borrowing strength across brands in a category when one brand's data is too thin.

## Recent work (the ideas behind Google Meridian)

4. **[Bayesian Hierarchical Media Mix Model Incorporating Reach and Frequency Data](https://research.google/pubs/bayesian-hierarchical-media-mix-model-incorporating-reach-and-frequency-data/)** (2023): Zhang et al. Modelling reach and frequency instead of raw impressions.
5. **[Media Mix Model Calibration With Bayesian Priors](https://research.google/pubs/media-mix-model-calibration-with-bayesian-priors/)** (2024): Zhang et al. How to turn experiment results into priors that calibrate the MMM.

## Practitioner guides

- **[A Comprehensive Guide to Bayesian Marketing Mix Modeling](https://1749.io/learn/f/a-comprehensive-guide-to-bayesian-marketing-mix-modeling)**: Niall Oulton (1749.io)
- **[PyMC-Marketing documentation](https://github.com/pymc-labs/pymc-marketing)**: the library used in the MMM notebook
