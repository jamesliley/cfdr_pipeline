*****************************************************************
*--  Data and code to reproduce figures and results in paper  --*
*--                                                           --*
*--  'Accurate error control in high dimensional association  --*
*--  testing using conditional false discovery rates'         --*
*--                                                           --*
*--                                                           --*
*--  James Liley and Chris Wallace                            --*
*--  2019                                                     --*
*****************************************************************

This folder contains all relevant material to reproduce plots 
and results in the paper above. We assume that the associated R
package 'cfdr' is loaded. If it is not, use

library(devtools)
install.github("jamesliley/cfdr")

In some areas (mostly large-scale simulations), the complete 
regeneration of all data used in the paper takes a prohibitively 
long time to produce. For this reason, we include a script which
generates a single run of the simulation, and a matrix of results
from previous runs.

In all processes involving random number generation, we set a 
random seed explicitly. For this reason, all results should match
those in the text exactly.

In this guide, we will outline the subdirectories in this folder,
then run through what each script does, and what each data object
contains.

An additional README in ./data explains columns of the matrix of 
simulation results.

*****************************************************************
*--  Directories                                              --*
*****************************************************************

This folder contains four subdirectories
 code: contains R scripts
 outputs: contains figures included in the manuscript (as PDFs) 
   and tables of results
 simulations: would contain simulation output
 data: contains datasets used for analysis


*****************************************************************
*--  Scripts                                                  --*
*****************************************************************

Folder 'code' contains three files:
code/run_simulation.R: runs a single iteration of the simulation,
 given a random seed
code/simulation_analysis.R: given a matrix of simulation results 
 and GWAS data, generates tables and draws plots as pdfs to 
 'outputs' directory
code/twas_analysis.R: runs the analysis of transcriptome-wide
 association study data in the motivating example in the paper.
code/draw_iterated.R: runs the 'iterated' cFDR example, and draws
 corresponding plot.

*****************************************************************
*--  Data objects                                             --*
*****************************************************************

Folder 'data' contains three objects. These are explained in the
README in ./data.
