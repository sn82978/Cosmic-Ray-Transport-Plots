# Cosmic Ray Transport Plots

This repository contains the Python code I developed to generate a central figure for my **second-author publication**:

> *Constraining cosmic ray transport with observations of the circumgalactic medium*
> (Caltech TAPIR)

The code integrates galaxy observational data with theoretical halo models to estimate **cosmic-ray diffusivity** in the circumgalactic medium (CGM). The resulting plots were used directly in the publication.

---

## 📄 Research Context

* **Scientific Goal:** Understand how cosmic rays propagate through the CGM by comparing modeled galaxy halo velocities with observed circumgalactic absorption features.
* **Key Idea:** By modeling **circular velocity profiles** with both **Navarro-Frenk-White (NFW) halos** and the **Tully-Fisher relation**, we can connect galaxy properties (stellar mass, halo mass, SFR, HI column density) to **cosmic-ray diffusivity constraints**.
* **Contribution:** I built the analysis pipeline and figure-generation code, providing the quantitative link between **galaxy dynamics** and **diffusion coefficients**.

---

## 🧮 What the Code Does

The script performs:

1. **Data ingestion** — stellar mass, halo mass, redshift, star formation rates (SFR), and HI column densities.
2. **Abundance matching** — predict halo mass from stellar mass.
3. **Velocity modeling**:

   * **NFW profile** circular velocities via `astropy.modeling.models.NFW`.
   * **Tully-Fisher relation**–based velocity estimates.
4. **Diffusivity estimation** — compute cosmic-ray diffusion coefficients under different assumptions.
5. **Plot generation** — produce side-by-side comparisons of:

   * NFW vs. Tully-Fisher velocity predictions.
   * Diffusivity coefficients vs. stellar mass and SFR.
   * Error bars reflecting astrophysical uncertainties.

---

## 📊 Example Output

* Velocity profile plots (NFW vs. Tully-Fisher).
* Diffusivity vs. stellar mass scatter plots.
* SFR-dependent diffusivity scaling.

Each figure is exportable in both **PNG** and **PDF** for direct use in publications.

---

## ⚙️ Requirements

* Python 3.9+
* `numpy`
* `pandas`
* `matplotlib`
* `astropy`
* `sympy`

---

## 📂 Repository Structure

* `CorrectOrderNotebook.ipynb` contains the working code

---

## 📚 Citation

If you use this code or adapt methods, please cite:

> *\[Authors including Shreya Nakum]*. “Constraining cosmic ray transport with observations of the circumgalactic medium.” *\[MNRAS, 2023, [DOI](https://doi.org/10.1093/mnras/stad671)]*.

---

## 👩🏽‍💻 Author

Developed by **Shreya Nakum** (UC Irvine) in collaboration with **Caltech**.
For questions or collaboration, please reach out via [LinkedIn](https://www.linkedin.com/in/shreyanakum/) or GitHub.
