# Turbulent-Modelling-using-Machine-Learning-Techniques
Jie Bao, MASc. Thesis

**Short summary**: Recent improvement in GPUs allows for research in fundamental turbulence using Machine
Learning. Current research area concerns the application of a neural network for the canonical
turbulent channel case. Strategy includes building a loss function for the production and
dissipation variables and feature pruning techniques. In turn improving the accuracy and
efficiency of turbulent-viscosity models. The research objective is achieved using Deviate from CAL 
and also Graham from Compute Canada. The high-order DNS data solution is solved using open-source solver PyFR (Discontinuous Galerkin Method).

The simulation below is a direct numerical simulation of the canonical wall bounded turbulent channel case. In which the whole spatial and temporal spectrum are solved for accurate turbulence prediction. The showcased simulation is from the dimensionless shear Reynolds of 180. The bulk Reynolds is found using the relationship from [Dean(1978)](https://ui.adsabs.harvard.edu/abs/1974STIN...7522638D/abstract).

![Alt Text](https://github.com/DiscoBroccoli/Turbulent-Modelling-using-Machine-Learning-Techniques/blob/main/latex_equation/re_bulk.gif)

![Alt Text](https://github.com/DiscoBroccoli/Turbulent-Modelling-using-Machine-Learning-Techniques/blob/main/TC-180.gif)

![Alt Text](https://github.com/DiscoBroccoli/Turbulent-Modelling-using-Machine-Learning-Techniques/blob/main/latex_equation/Dimension.gif)

![Alt Text](https://github.com/DiscoBroccoli/Turbulent-Modelling-using-Machine-Learning-Techniques/blob/main/latex_equation/Values.gif)

The goal of the research project is to predict to gather a database of high fidelity data ranging from Re = 180, 285, 395, 450, 590.
Then build a neural network to predict the Production and Dissipation terms in the turbulent kinetic energy PDE.

![Alt Text](https://github.com/DiscoBroccoli/Turbulent-Modelling-using-Machine-Learning-Techniques/blob/main/latex_equation/Production.gif)

![Alt Text](https://github.com/DiscoBroccoli/Turbulent-Modelling-using-Machine-Learning-Techniques/blob/main/latex_equation/Dissipation.gif)
