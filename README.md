# BRIEFnet
Code for MICCAI 2017 paper
please see mpheinrich.de for PDF and more details

## Prerequisites to run example

### 1) Create free synapse.org account and download pancreas dataset
"Beyond the Cranial Vault" MICCAI workshop (https://www.synapse.org/#!Synapse:syn3193805/wiki/89480)
Log in, click on 'Files' and select 'Abdomen' (or go to https://www.synapse.org/#!Synapse:syn3376386)
you will only need RawData.zip (which has a size of 1.53 GBytes), extract the files.

### 2) Download and install the c3d of ITK-Snap
http://www.itksnap.org/pmwiki/pmwiki.php?n=Downloads.C3D
Open a terminal window and navigate into the BRIEFnet source folder
run the following script to crop the scans (edit path if needed)
./crop_scans.sh ~/Downloads/RawData/

### 3) Open a MATLAB instance and install matconvnet
https://github.com/vlfeat/matconvnet
Follow the guide to compile the toolbox at http://www.vlfeat.org/matconvnet/install/
for applying the trained models the CPU is sufficient, otherwise a GPU is recommended

### 4) Load a trained BRIEFnet model and a apply it to a scan