![FARM_LOGO_rgb_black](https://user-images.githubusercontent.com/63424217/178042559-7f4c1b33-cd0f-4bd4-9a31-22e6f0d80dd8.png)
# FARM
Feasible Actuator Range Modifier (FARM) Plugin for RAVEN

# Main developers:
- Haoyu Wang and Roberto Ponciroli, Argonne National Laboratory
- Andrea Alfonsi, Idaho National Laboratory

# Introduction
Feasible Actuator Range Modifier (FARM) is a RAVEN (https://github.com/idaholab/raven) plugin designed to solve the 
supervisory control problem in Integrated Energy System (IES) project. FARM utilizes the linear state-space representation 
(A,B,C matrices) of a model to predict the system state and output in the future time steps, and adjust the actuation variable 
to avoid the violation of implicit thermal mechanical constraints.

# Organization
This plugin folder is organized as follows:
- src folder containing the three officially supported plugin source code:
    - RefGov_parameterized_SIMO.py
    - RefGov_unparameterized_SIMO.py
    - FARMValidatorsForHeron.py
- tests/raven_plugin folder containing the tests that are needed to test the RAVEN plugin:
    - test_RefGov_para_xmlABC.xml
    - test_RefGov_unpara_xmlABC.xml
- tests/heron_validator folder contains the tests/examples to use FARM as a validator for HERON unit dispatcher
    - FARM_SISO_initGuess_noUpdate
    - FARM_SISO_initGuess_fmuUpdate
    - FARM_SISO_selfLearning_noUpdate
    - FARM_SISO_selfLearning_fmuUpdate
    - FARM_SISO_StateVarSelect
    - FARM_MIMO_initGuess_noUpdate
    - FARM_MIMO_initGuess_fmuUpdate
    - FARM_MIMO_selfLearning_noUpdate
    - FARM_MIMO_selfLearning_fmuUpdate
    - FARM_MIMO_StateVarSelect

# User Manual
- For using FARM as a raven plugin:
    - Go to FARM/doc folder
    - run "bibtex user_manual" and then "pdflatex user_manual" to get the latest version of user manual.
- For using FARM as a HERON validator:
    - Go to https://www.osti.gov/biblio/2361134
 
# Cite FARM:
Haoyu Wang, Roberto Ponciroli, Andrea Alfonsi, Paul W. Talbot, Thomas W. Elmer, Aaron S. Epiney, and Richard B. Vilim. 2024. "Feasible Actuator Range Modifier (FARM), a Tool Aiding the Solution of Unit Dispatch Problems for Advanced Energy Systems" Energies 17, no. 12: 2945. https://doi.org/10.3390/en17122945

# Other related technical reports:
- Demonstrate FARM supervisory capabilities for a thermal energy storage problem for the DETAIL facility, https://www.osti.gov/biblio/2284085
- Integrate FARM with PID controllers, https://www.osti.gov/biblio/1995494
- Implementation of a feature selection algorithm in FARM to identify important state variables and time-invariant matrices, https://www.osti.gov/biblio/1962055
- Application of FARM to an IES scenario within the FORCE ecosystem, https://www.osti.gov/biblio/1960777
- Control system for multi-system coordination via a single reference governor, https://www.osti.gov/biblio/1881455
- Time dependent supervisory control update with FARM using rolling window, https://www.osti.gov/biblio/1867368
- Automation of FARM from Alpha Phase to Beta Phase, https://www.osti.gov/biblio/1846200
- Validation and Demonstration of Control System Functional Capabilities within the IES Plug-and-Play Simulation Environment, https://www.osti.gov/biblio/1777477
- Development of Control System Functional Capabilities within the IES Plug-and-Play Simulation Environment, https://www.osti.gov/biblio/1721623
  
# License
FARM itself is licensed as follows:

Copyright 2021 UChicago Argonne, LLC

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

  https://www.apache.org/licenses/LICENSE-2.0.txt

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
