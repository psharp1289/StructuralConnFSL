# StructuralConnFSL: A pipeline for structural connectome reconstruction from diffusion-weighted data. 

These set of scripts comprise a structural connecotme pipeline.

The higher-level pipeline file which calls all sub-scripts is called "proc_fsl_connectome.sh"

REQUIRED PACKAGES:

1. Nipype
2. FSL
3. Freesurfer

*ALL* that needs to be changed in order to run this pipeline in your data is to amend the config and subjects.txt files appropriately.

1. Subjects.txt includes one subject per line.
2. Connectome_variables.cfg: this allows you to parse the brain in any way, as long as you have the appropriate parcellation numbers, labels file, and accompanying freesurfer .mgz parcellated file. Future versions of this pipeline will expand usage to AAL labelling, which can be worked in with few changes (really just amending the registration of the atlas-space to native diffuson space steps which are currently specific to freesurfer). 


This scripts ASSUMES you have run freesurfer recon-all on your subjects T1 images.
 
IF YOU HAVEN'T RUN FREESURFER:
There are 2 Files in this set of scripts to run freesurfer on T1 data: 
1. freesurfer_recon_all.py
2. freesurfer_variables.cfg

NOTE the freesurfer python file requires subject folders to be within the T1 location directory. 


  
