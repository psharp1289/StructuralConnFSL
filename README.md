# StructuralConnFSL: A pipeline for structural connectome reconstruction from diffusion-weighted data. 

These set of scripts comprise a structural connecotme pipeline.

The higher-level pipeline file which calls all sub-scripts is called "proc_fsl_connectome.sh"

REQUIRED PACKAGES:
1. Nipype
2. FSL
3. Freesurfer

*ALL* that needs to be changed in order to run this pipeline in your data is to amend the config and subjects.txt files appropriately.
1. Subjects.txt includes one subject per line, which should be 


This scripts ASSUMES you have run freesurfer recon-all on your subjects T1 images.
 
IF YOU HAVEN'T RUN FREESURFER:
There are 2 Files in this set of scripts to run freesurfer on T1 data: 
1. freesurfer_recon_all.py
2. freesurfer_variables.cfg

NOTE the freesurfer python file requires subject folders to be within the T1 location directory. 


  
