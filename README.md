# Epistasis-detection-and-fitness-valleys-in-SARS-CoV-2-evolution-Code
Code for the "Epistasis detection and fitness valleys in SARS-CoV-2 evolution" project

Minimal reqiurements:

PC with Windows system (10 or newer) - Linux and Mac builds are not present at the moment, you can build them from source files, note that for now (October 2026) Mac doesn't support CUDA

MATLAB (recommended version is 2023A or newer) - needed only for mock sequences generation

NVIDIA GPU with CUDA support (Highly recommended) - Processing tool doesn't need GPU and Calculation tool can be used with CPU alone, but in that case calculation speed is very low. Use the CPU mode only for small data samples

Folders description

CodeOnly - only the source code without enviroment (you will need to install Python and all libraries)

CodePlusEnviroment - code with enviroment (you can open folders from there in IDE as projects, enviroment inside should have all libraries needed to run)

Files description:

ShortTest.m - MATLAB program that initiates mock sequence generation

recomb_2023_epi.m - MATLAB program function that generates mock sequences

DataProcessing - folder with enviroment and python script for data processing

EpistasisCalculation - folder with enviroment and python script for Epistasis calculation

How to use:

0) Decide whether you want to build code with your enviroment, provided enviroment or download the builded code in release section (currently only Windows build is available)
1) If using mock sequences - open ShortTest.m and set needed parameters. After the end of calculations remeber the path to saved data files
or transfer them to the EpistasisCalculation folder, skip step 2
2) Process your data (use the compiled script located in the relese folder or run raw script via IDE like PyCharm)
3) Transfer processed data to the EpistasisCalculation folder and use the compiled script or run raw script via IDE
4) Work with images of clusters and .txt files with links in each cluster (you can combine .txt for better look. Circular diagrams in paper were done via Circos software using .txt output files) (note that nucleotide positions in images start with 0 and not with 1, same applies to the positions inside .txt files)
