# Kuramoto Model Simulation

This repository contains a numerical simulation of the Kuramoto model, a paradigmatic model of synchronization. The Kuramoto model illustrates how coupled oscillators evolve towards collective oscillation when the coupling exceeds a critical value. This project explores the fundamental properties of the model through numerical simulations.

## Table of Contents
1. [Introduction](#introduction)
2. [Model Description](#model-description)
3. [Code Implementation](#code-implementation)
4. [Results and Plots](#results-and-plots)
5. [Interpretation](#interpretation)
6. [Usage](#usage)
7. [Dependencies](#dependencies)
8. [License](#license)

## Introduction
The Kuramoto model, introduced by Yoshiki Kuramoto in 1975, is a mathematical model used to study synchronization in systems of coupled oscillators. This project focuses on simulating the model for different coupling strengths and system sizes to observe the onset of synchronization.

## Model Description
The Kuramoto model consists of $N$ one-dimensional rotors on a ring, each with a phase $\theta_i$ and a natural frequency $\omega_i$. The equations of motion are given by:

$$
\frac{d\theta_i}{dt} = \omega_i + \frac{K}{N} \sum_{j=1}^N \sin(\theta_j - \theta_i)
$$

where $K$ is the coupling strength. The complex order parameter $r(t)$ is introduced to measure the degree of synchronization:

$$
r(t) e^{i\psi(t)} = \frac{1}{N} \sum_{j=1}^N e^{i\theta_j(t)}
$$

## Code Implementation
The simulation is implemented in Python using `NumPy` for numerical computations and `SciPy` for solving the differential equations. The code is divided into the following sections:
1. **Parameter Definition**: Define the number of oscillators $N$, coupling strengths $K$, and initial conditions.
2. **Kuramoto Equations**: Implement the Kuramoto equations of motion.
3. **Simulation**: Run simulations for different values of $K$ and $N$.
4. **Order Parameter Calculation**: Compute the order parameter $r(t)$ to measure synchronization.
5. **Plotting**: Visualize the results using `matplotlib`.

## Results and Plots
The repository includes the following plots:
1. **Phase Evolution**: Plots of $\theta_i(t)/t$ for different coupling strengths $K$.
2. **Order Parameter vs. Time**: Evolution of the order parameter $r(t)$ for large $N$.
3. **Stationary Order Parameter**: Mean stationary order parameter $\bar{r}$ as a function of $K$ for different system sizes $N$.

## Interpretation
- As $N$ increases, the transition to synchronization becomes sharper around the critical coupling strength $K_c$.
- The numerical results align with the theoretical prediction of the critical coupling strength in the thermodynamic limit:
  $$
  K_c = \frac{2}{\pi g(0)}
  $$
  where $g(0)$ is the value of the frequency distribution at its center.

## Usage
To run the simulations and generate the plots:
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/kuramoto-model.git

2. Install the required dependencies:
   ```bash
   pip install numpy scipy matplotlib jupyter

