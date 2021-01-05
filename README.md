# Turbulent-Modelling-using-Machine-Learning-Techniques
Jie Bao, MASc. Thesis

**Short summary**: Recent improvement in GPUs allows for research in fundamental turbulence using Machine
Learning. Current research area concerns the application of a neural network for the canonical
turbulent channel case. Strategy includes building a loss function for the production and
dissipation variables and feature pruning techniques. In turn improving the accuracy and
efficiency of turbulent-viscosity models. The research objective is achieved using Deviate from CAL 
and also Graham from Compute Canada. The high-order DNS data solution is solved using open-source solver PyFR (Discontinuous Galerkin Method).

The simulation below is a direct numerical simulation (DNS) of the canonical wall bounded turbulent channel case. In which the whole spatial and temporal spectrum are solved for accurate turbulence prediction. The showcased simulation is from the dimensionless shear Reynolds of 180. The bulk Reynolds is found using the relationship from [Dean(1978)](https://ui.adsabs.harvard.edu/abs/1974STIN...7522638D/abstract).

![Alt Text](https://github.com/DiscoBroccoli/Turbulent-Modelling-using-Machine-Learning-Techniques/blob/main/latex_equation/re_bulk.gif)

The flow field starts laminar and will transition into turbulent regime. However, this transition process can be very slow. Therefore, we can accelerate the transition by adding perturbation in the initial condition:

![Alt Text](https://github.com/DiscoBroccoli/Turbulent-Modelling-using-Machine-Learning-Techniques/blob/main/latex_equation/transition_u.gif)

![Alt Text](https://github.com/DiscoBroccoli/Turbulent-Modelling-using-Machine-Learning-Techniques/blob/main/latex_equation/transition_vv.gif)

![Alt Text](https://github.com/DiscoBroccoli/Turbulent-Modelling-using-Machine-Learning-Techniques/blob/main/latex_equation/transition_w.gif)

![Alt Text](https://github.com/DiscoBroccoli/Turbulent-Modelling-using-Machine-Learning-Techniques/blob/main/iso.gif)

![Alt Text](https://github.com/DiscoBroccoli/Turbulent-Modelling-using-Machine-Learning-Techniques/blob/main/latex_equation/Dimension.gif)

![Alt Text](https://github.com/DiscoBroccoli/Turbulent-Modelling-using-Machine-Learning-Techniques/blob/main/latex_equation/Values.gif)

The goal of the research project is to gather a database of high fidelity data ranging from Re = 180, 285, 395, 450, 590.
Then build a neural network to predict the Production and Dissipation terms in the turbulent kinetic energy PDE.

![Alt Text](https://github.com/DiscoBroccoli/Turbulent-Modelling-using-Machine-Learning-Techniques/blob/main/latex_equation/Production.gif)

![Alt Text](https://github.com/DiscoBroccoli/Turbulent-Modelling-using-Machine-Learning-Techniques/blob/main/latex_equation/Dissipation.gif)

The current industry standard fluid solver uses a Reynolds-Averaged-Navier-Stokes solver (RANS). Unlike DNS, the meshes are usually coarse and does not solve all the way down to the smallest scale. This reduces the computation cost but decreases the accuracy. Furthermore, the solver is using a time-averaged Navier-Stokes equation, giving rise to an extra unknown term called the Reynolds stress. To overcome this challenge many eddy-viscosity based model are created, some like the k-e model computes the turbulent kinetic energy field to estimate the Reynolds stress (Boussinesq approximation).

**To be continued**
