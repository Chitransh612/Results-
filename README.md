rTMS-Enhanced Glioblastoma Treatment Simulation

Mechanistic PK/PD and Systems Neuro-Oncology Model

Overview

This repository presents results and model documentation from an ongoing computational oncology project investigating rTMS-enhanced glioblastoma (GBM) therapy. The simulation integrates tumor growth dynamics, hypoxia, chemotherapy pharmacokinetics/pharmacodynamics, Tumor Treating Fields (TTF), and rTMS-driven neurovascular effects within a unified mechanistic framework.

The full simulation codebase is under active development and remains private.
This repository is intended to demonstrate scientific modeling depth, system structure, and key outcomes.

Scientific Motivation

Glioblastoma exhibits profound treatment resistance driven by hypoxia, limited drug delivery, and proliferative heterogeneity. Recent evidence suggests that rTMS may modulate perfusion, oxygenation, and blood–brain barrier permeability, potentially enhancing standard therapies.

This project explores:

How rTMS-induced perfusion changes alter intratumoral hypoxia

How hypoxia dynamically modulates TTF efficacy and chemotherapy response

Whether mechanistic synergy emerges from combining rTMS, TMZ, and TTF

Model Architecture (High-Level)
Core Components

Tumor Growth

Logistic growth with apoptosis

Age-dependent and inter-patient variability

High-precision RK45 ODE solver

Hypoxia Dynamics

ODE-based hypoxic fraction model

Tumor growth–driven hypoxia vs perfusion-driven reoxygenation

Explicit oxygen effect ratio (OER) modeling

Chemotherapy (Temozolomide)

Two-compartment PK model (plasma ↔ tumor)

DNA adduct–based PD

MGMT-dependent resistance and acquired resistance dynamics

rTMS-enhanced BBB permeability

Tumor Treating Fields (TTF)

Field attenuation with tumor depth

Cell-cycle–dependent mitotic disruption

Hypoxia-modulated efficacy

rTMS Effects

Session-based cumulative perfusion enhancement

Neurovascular coupling and decay dynamics

Indirect treatment synergy via oxygenation and delivery

Biomarkers (Reporting Layer)

Tumor pO₂

HIF-1α, VEGF

BDNF

Pro-inflammatory cytokines (IL-1β, TNF-α)

Results Included

This repository contains representative output figures demonstrating:

Tumor volume trajectories under different treatment arms

Dynamic hypoxia and perfusion modulation

rTMS-dependent enhancement of chemotherapy exposure

Biomarker evolution reflecting microenvironmental changes

Emergent synergy between rTMS, TTF, and chemotherapy

Figures are generated from multi-patient Monte Carlo simulations with biologically constrained parameter sampling.

Numerical Methods

ODE integration: scipy.solve_ivp (RK45)

Separate solver tolerances for:

Tumor growth

Hypoxia dynamics

Pharmacokinetics

Explicit parameter validation against literature ranges to prevent non-physical solutions

Code Availability

The full simulation codebase is currently private while:

Model validation is ongoing

Manuscript preparation is in progress

Code access can be provided upon request for academic review or collaboration.

