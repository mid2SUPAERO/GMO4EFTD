# Basic Information

The databases are inside the folder "data"

The figures are saved inside the folders "figures*"

The trained VAE is stored at the folder "results"

The folder "src" contains some python packages codes such as the material encoder or the Finite Element Solver


## VAE_2D_Visual
It trains the VAE and displays a series of results such as the decoding error, the latent space (2D) considering 2 coordinates or the gradients of the properties.

## VAE_3D_Visual
It trains the VAE and displays a series of results such as the decoding error, the latent space (3D) considering 3 coordinates or the gradients of the properties.

## Integer_Optimizer
Perform a multiple optimization of material and topology using the pymoo tool Multi-objective Optimization With Mixed Variables https://pymoo.org/customization/mixed.html

You simply need to edit the constraints / objectives you want to search for in block [4] and everything runs automatically.
