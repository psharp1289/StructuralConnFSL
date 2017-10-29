# StructuralConnFSL: A pipeline for structural connectome reconstruction from diffusion-weighted data. 

This set of scripts is designed to reconstruct structural connectomes from diffusion-weighted data in a user-friendly fashion.

The higher-level pipeline file which calls all sub-scripts is called "proc_fsl_connectome.sh" After changing the variables in the appropriate .cfg files, you can run this pipeline by typing "./proc_fsl_connectom.sh" in your bash terminal. 

REQUIRED PACKAGES:

1. Nipype (to get, execute in bash: pip install nipype)
2. FSL (https://fsl.fmrib.ox.ac.uk/fsl/fslwiki)
3. Freesurfer (http://freesurfer.net/fswiki/FreeSurferWiki)

*ALL* that needs to be changed in order to run this pipeline on your data is to amend the .cfg and subjects.txt files.

1. Subjects.txt includes one subject per line.
2. Connectome_variables.cfg: this allows you to parse the brain in any way, as long as you have the correct total parcellation number, labels file, and accompanying freesurfer .mgz parcellated file. Future versions of this pipeline will expand usage to other parcellation schemes, such as (1) AAL or (2) the Human Connectome Project multimodal map. Currently, this can be worked in with few changes (really just amending the registration of the atlas-space to native diffuson space steps which are currently specific to freesurfer). 


This scripts ASSUMES you have run freesurfer recon-all on your subjects T1 images.
 
IF YOU HAVEN'T RUN FREESURFER:
There are 2 Files in this set of scripts to run freesurfer on T1 data: 
1. freesurfer_recon_all.py
2. freesurfer_variables.cfg

NOTE the freesurfer python file requires subject folders to be within the T1 location directory. 


  
