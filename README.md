# Calibration_damage_mechanics
The repository contains the MATLAB and Python code used to model the examples in "Multi-stage calibration framework for continuum damage mechanics models " 

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% Ref: R.P. Saji, P. Pantidis,L. Svolos, M. Mobasher, Multi-stage calibration framework for continuum damage mechanics models 
% Journal: Engineering Fracture Mechanics
% Author 1: Dr. Roshan Philip Saji
% email: rs7625@nyu.edu
% Author 2: Dr. Panos Pantidis
% email: pp2624@nyu.edu
% Author 3: Prof. Lampros Svolos
% email: Lampros.Svolos@uvm.edu
% Author 4: Prof. Mostafa Mobasher 
% email: mostafa.mobasher@nyu.edu
%
% Computational Solid Mechanics Lab, New York University Abu Dhabi
% Department of Civil and Environmental Engineering, University of Vermont, Burlington, VT, USA
% Date: 03-July-2025 
% Link to manuscript: [https://doi.org/10.1016/j.engfracmech.2025.111341]
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
This is the Read me/License file for the 2D numerical examples presented in the above referenced manuscript.
 
We present a multi-stage calibration framework for determining material parameters in continuum damage models. The framework sequentially minimizes loss functions targeting 
bespoke performance metrics, like peak force and displacement, total work, and L2 norm of experimental vs numerical curves. Incorporating two nonlinear solvers, 
Unified Arc-Length (UAL) and Newton–Raphson (NR), we examine our approach against several benchmark problems with various damage theories, equivalent strain definitions and
evolving length scale regimes. Overall, UAL outperforms NR in computational efficiency and captures snap-backs on the equilibrium path. The proposed framework can be readily
expanded to identify material model parameters for other constitutive model classes. 

This code package contains the following:
• Solvers     			- UAL, NR
  Damage type 			- Local, Non-Local Gradient
  Damage evolution laws - Mazars, Geers
  
We invite you to try out different continuum damage mechanics problems using this package and experience first-hand the benefits of our novel calibration framework.

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%================================================================================================================================================================================%
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

Steps to run the calibration code:

1. Open the folder named "Calibration framework package"
2. From the folders named "Mesh files" and "Reference data" copy the mesh, parameter and reference data of the example you want to test
3. Paste the copied files into the folder named "Calibration code"
4. Open main script file - "Calibration_Mainscript.py"
   • Enter the file path and results storage folder path
   • Enter the model name 
	  ♦ Test slab 
      ♦ Hasanzadeh - (Coarse and Fine)
      ♦ L-shaped panel
      ♦ DNT - Double Notch Tension
   • Enter the following calibration parameters mentioned in Section 4 of the manuscript	
5. Open the file "func_MATLAB_loss_function_UAL.m" and enter solver and model specific parameters mentioned in Section 4 of the manuscript  
5. Run main script file - "Calibration_Mainscript.py"

%================================================================================================================================================================================%
NOTE:
* Ensure that you are using the latest version of MATLAB (R2023b or later versions).
* Rename the variable 'connect' to 'connect_xyz' throughout the code if you don't have access to the latest version of MATLAB.
* Ensure that you've created a folder to save the data files and images at each increment.  
* Ensure that compatible versions of MATLAB and Python are installed on your device.
%================================================================================================================================================================================%


