# Simulation Suite: First-Principles Quantum Hydrodynamics, Chiral Spin-2 Gravitons, Non-Linear Cyclic Nucleosynthesis, and Multi-Scale Empirical Calibration of \(\chi_{\text{crit}}\)

[![ORCID](https://shields.io)](https://orcid.org)
[![Python 3.10+](https://shields.io)](https://python.org)
[![License: MIT](https://shields.io)](https://opensource.org)

**Author:** Ehab Mohamed Abdel Gwad Manse  
**Affiliation:** Independent Researcher, Cairo, Egypt  
**Contact:** `ehabmanse2@gmail.com`  

---

## Overview

This repository hosts the **five reproducible Python/Jupyter numerical simulation and Bayesian Markov Chain Monte Carlo (MCMC) validation notebooks** supporting the Unified Quantum Superfluid cosmological study:

> **First-Principles Quantum Hydrodynamics, Chiral Spin-2 Gravitons, Non-Linear Cyclic Nucleosynthesis, and Multi-Scale Empirical Calibration of the Cosmic Superfluid Crystallization Threshold (\(\chi_{\text{crit}}\))**

The codebase implements first-principles partial differential equation (PDE) and stiff ordinary/integro-differential equation (ODE/IDE) solvers modeling space-time as a topologically closed, zero-viscosity chiral \(p\)-wave quantum superfluid (\(^3\text{He-A}\) analogy). All statistical verifications strictly enforce a **zero-proxy, zero-tuning protocol** evaluated across **\(N = 414\) exclusively direct astronomical measurements** spanning \(0.0001 \le z \le 14.18\).

---

## Interactive Google Colab Notebooks & Simulation Suite

All five numerical simulations can be executed directly in the cloud via Google Colab with a single click, or run locally using the archived `.ipynb` notebooks in this repository:

| Simulation | Physics & Numerical Solver | Direct Observational MCMC Dataset (\(N = 414\)) | Key Benchmark Output | Cloud Execution |
| :--- | :--- | :--- | :--- | :--- |
| **Sim 1** (`Sim1_CMB_Cyclic_BBN_117MCMC.ipynb`) | Coupled baryon–photon sound horizon (\(r_s = 144.29\,\mathrm{Mpc}\)), closed-cavity \(C_\ell\) power spectrum, & 12-reaction stiff **LSODA** cyclic nucleosynthesis | **\(N = 117\) direct systems** (\(52\) VLT/Keck/LBT \(^7\mathrm{Li}\), \(\mathrm{D}\), \(^4\mathrm{He}\) spectra + \(65\) HST/ALMA/JWST \(M_{\text{gal}}\text{--}M_{\text{BH}}\) galaxies) | \(\ell_1 = 212\), \(D_2 = 212.6\,\mu\mathrm{K}^2\), \(^7\mathrm{Li/H} = 1.89 \times 10^{-10}\), \(\mathcal{I}_0 = 0.4599 \pm 0.0015\) | [![Open In Colab](https://google.com)](https://google.com) |
| **Sim 2** (`Sim2_3D_Soliton_GPE_Poisson_65MCMC.ipynb`) | 3D time-dependent **GPE–Poisson** solver via 2nd-order Strang Split-Step Fourier Method (\(48^3\) grid, \(g_{\text{nl}}/G_{\text{grav}} = 22.67\)) | **\(N = 65\) direct galaxies** (\(55\) SPARC rotation curves + \(10\) high-\(z\) JWST galaxies) | Unitarity \(\vert{}\Delta N/N\vert{} = 5.74 \times 10^{-16}\), \(\chi_{\text{crit}} = (4.12 \pm 0.05) \times 10^4\), \(\xi = 4.14 \pm 0.04\,\mathrm{kpc}\) | [![Open In Colab](https://google.com)](https://google.com) |
| **Sim 3** (`Sim3_3D_BH_PhaseShear_Bounce_64MCMC.ipynb`) | 3D **Landau–Ginzburg** Higgs phase-shear collapse & non-singular Quantum Bohm bounce solver | **\(N = 64\) direct black holes** (EHT M87*/Sgr A* + Fundamental Plane jet catalog) | Bounce peak \(\chi_{\text{peak}} = 5.30 \times 10^6\), \(\vert{}\Delta N/N\vert{} = 4.24 \times 10^{-16}\), \(\chi_{\text{shear}} = (2.513 \pm 0.008) \times 10^5\) | [![Open In Colab](https://google.com)](https://google.com) |
| **Sim 4** (`Sim4_Freeman_Madelung_Edge_120MCMC.ipynb`) | Radial **Euler–Madelung** hydrodynamics coupled to exact analytical Freeman exponential disk Bessel potential | **\(N = 120\) direct galaxies** (THINGS-VLA HI velocity dispersions & SPARC disks) | Acoustic floor \(\sigma_{\text{edge}} = 7.28 \pm 0.11\,\mathrm{km/s}\), flat outer \(V_{\text{rot}} = 185.6\,\mathrm{km/s}\) | [![Open In Colab](https://google.com)](https://google.com) |
| **Sim 5** (`Sim5_BAO_Anisotropy_Dipole_48MCMC.ipynb`) | Inhomogeneous superfluid BAO sound-horizon integral \(r_d(\delta_m, \theta)\) & Mollweide dipole projection | **\(N = 48\) direct measurements** (\(28\) DESI DR1/SDSS void–cluster BAO splits + \(20\) Planck/CatWISE dipoles) | Void–cluster split \(\Delta r_d/r_d = 1.52\% \pm 0.05\%\), dipole \(A_{\text{res}} = 0.0720 \pm 0.0041\) | [![Open In Colab](https://google.com)](https://google.com) |

---

## Repository Structure

```text
├── notebooks/
│   ├── Sim1_CMB_Cyclic_BBN_117MCMC.ipynb
│   ├── Sim2_3D_Soliton_GPE_Poisson_65MCMC.ipynb
│   ├── Sim3_3D_BH_PhaseShear_Bounce_64MCMC.ipynb
│   ├── Sim4_Freeman_Madelung_Edge_120MCMC.ipynb
│   └── Sim5_BAO_Anisotropy_Dipole_48MCMC.ipynb
├── figures/
│   ├── cmb_simulation.png
│   ├── sim2_3d_crystallization.png
│   ├── sim3_bh_recycling.png
│   ├── sim4_galaxy_edge.png
│   └── sim5_bao_anisotropy.png
├── requirements.txt
├── CITATION.cff
└── README.md
```

---

## Local Installation & Reproducibility

To run the five simulation notebooks locally:

```bash
pip install -r requirements.txt
jupyter notebook
```

*(All Metropolis–Hastings MCMC chains use fixed random seeds `np.random.seed(42)` to guarantee bit-for-bit reproducibility of posterior means, $1\sigma$ uncertainties, reduced $\chi^2_\nu$, and high-resolution figures.)*

---

## Citation

If you use these simulation codes or compiled observational datasets, please cite this software release via its Zenodo DOI or the accompanying research article:

```bibtex
@software{Manse2026_SuperfluidSimulations,
  author       = {Manse, Ehab Mohamed Abdel Gwad},
  title        = {{Simulation Suite: First-Principles Quantum Hydrodynamics, Chiral Spin-2 Gravitons, Non-Linear Cyclic Nucleosynthesis, and Multi-Scale Empirical Calibration of \(\chi_{\text{crit}}\)}},
  year         = {2026},
  month        = {nov},
  publisher    = {Zenodo}
}
```
