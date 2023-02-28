# Geometry-and-Material-Optimization-for-Environmentally-Friendly-Truss-Design

*Link to the paper*

ICA, Universit ́e de Toulouse, ISAE-SUPAERO, MINES ALBI, UPS, INSA, CNRS, Toulouse, France.

## Dependencies

PyTorch, scipy, numpy, matplotlib, pymoo


## Abstract

The optimization of topology and material selection is a crucial factor in structural design, as it helps meet structural objectives while reducing weight or cost. In simple structures with a small number of materials, these two problems can be separated, enabling the selection of the optimal material followed by topology optimization. However, for more complex structures, this approach is computationally infeasible.

The main challenge in coupling these problems is the discrete nature of materials, which does not align with gradient-based geometry optimization. To address this, a continuous space of material properties is created, called the latent space, using a variational autoencoder (VAE) to enable simultaneous gradient optimization of material and geometry selection.

We demonstrate the effectiveness of the proposed method using trusses and a database of materials with their properties. Our objective is to select one material from the list and determine the areas of each truss member to minimize a particular property, while adhering to imposed constraints.

This work has significant applications in optimizing structures based on environmental criteria, such as reducing carbon dioxide, water, or energy consumption associated with truss member production, while considering costs or weight. Therefore one of the key results of this tool is to be able to obtain a Pareto front that balances multiple properties to facilitate an appropriate selection of material.




# Basic Information

The database is inside the folder "data"

The figures are saved inside the folders "figures*"

The VAE is stored at the folder "results"

The folder "src" contains some python packages codes such as the material encoder, truss examples or the Finite Element Solver


## VAE_2D_Visual
It trains the VAE and displays a series of results such as the decoding error, the latent space (2D) considering 2 coordinates or the gradients of the properties.

## VAE_3D_Visual
It trains the VAE and displays a series of results such as the decoding error, the latent space (3D) considering 3 coordinates or the gradients of the properties.

## VAE_Single_pymoo
Solves the single-objective problem with NSGAII algorithm making use of the VAE

## VAE_Multi_pymoo
Solves the multi-objective problem with NSGAII algorithm making use of the VAE

## Pareto_Bruteforce
Gets a solution by brute-force of a set of objectives and plots the Pareto front from the solution

## Integer_Optimizer
Perform a multiple optimization of material and geometry using the pymoo tool Multi-objective Optimization With Mixed Variables https://pymoo.org/customization/mixed.html

## VAE_Mixed_Multi_pymoo
Runs a program similar to **VAE_Multi_pymoo** and then applies **Integer_Optimizer** to the reduced database
