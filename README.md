# EPICS
Extracting Physical-Characteristics from Images of Chromatin Structures (EPICS) is a machine-learning based computational method for processing high-resolution chromatin 3D image data. 

## Repository Organization

Each of the experiments associated with EPICS is provided in respective branches.  Specifically, experiments were done on 3D-EMISH and 3D-SIM data.  Those experiments (code, associated data, and output) are all provided in their respective branches.  The .py files in each branch collect the features from the raw data.  The .r files build the models for classifying open and closed chromatin domains (CDs).   Each branch is also given it's own .zip file in the main branch with the same files.  Each .zip is explained herein.

### EPICS_guide.pdf

A guide and overview of EPICS applied to 3D-EMISH and 3D-SIM.  EPICs is detailed with step-by-step examples for 3D-EMISH and 3D-SIM.  

### EPICS_guide.pdf

A guide and overview of EPICS applied to 3D-EMISH and 3D-SIM.  EPICs is detailed with step-by-step examples for 3D-EMISH and 3D-SIM.  

### epics-3D-EMISH.zip

The ultima_cds_open_closed.py file collects the shape and intensity metrics for each chromatin domains (CDs). It uses custom functions from md_tif.py. 3d_emish_cds_open_closed_lr.r builds the models to classify the open and closed CDs from one another. It requires the data from 3d_emish_data.zip.

Raw 3D-EMISH data was obtained from Trzaskoma et.al.'s GitHub (https://github.com/3DEMISH/3D-EMISH). Our intensity and shape metrics are provided in 3d_emish_data.zip.

Thus, the steps to run the code are:

0. Ensure that your files are in useful locations.  Define these locations in the subsquent files. 
1. Run ultima_cds_open_closed.py using Python. 
2. Run 3d_emish_cds_open_closed_lr.r using R.

### epics-3D-SIM.zip

The 3d_sim.py file collects the shape and intensity metrics for each chromatin domains (CDs). It uses custom functions from md_tif.py. tri_open_closed_lr.r builds the models to classify the open and closed CDs from one another. It requires the data from 3d_sim_data.zip.

Raw 3D-SIM images were obtained from Cremer et.al.'s 2020 paper (https://datadryad.org/stash/dataset/doi:10.5061/dryad.vt4b8gtqb). Our intensity and shape metrics are provided in 3d_sim_data.zip.

Thus, the steps to run the code are:

0. Ensure that your files are in useful locations.  Define these locations in the subsquent files. 
1. Run 3d_sim.py using Python. 
2. Run tri_open_closed_lr.r using R.

## 3D .gif Files

3D .gif files of some of Figure 1's panels are provided in the main branch under the folder '3d_gifs'.  

## Data

Raw 3D-EMISH data was obtained from Trzaskoma et.al.'s GitHub (https://github.com/3DEMISH/3D-EMISH).  Raw 3D-SIM images were obtained from Cremer et.al.'s 2020 paper (https://datadryad.org/stash/dataset/doi:10.5061/dryad.vt4b8gtqb).   

## System Information

The computation was performed on a Ubuntu 18.04.5 system with 64 GB of RAM and an Intel® Xeon(R) W-2245 CPU @ 3.90GHz with 8 cores and 16 threads.  Python and R were used to implement EPICS and many visualizations.  ImageJ was used to create some of the 3D .gifs.

Below is a list of the installed versions of the Python libraries (as of Janurary 2021):

apt-clone==0.2.1<br />
apturl==0.5.2<br />
asn1crypto==0.24.0<br />
Brlapi==0.6.6<br />
certifi==2018.1.18<br />
chardet==3.0.4<br />
command-not-found==0.3<br />
cryptography==2.1.4<br />
cupshelpers==1.0<br />
cycler==0.10.0<br />
cykhash==1.0.2<br />
Cython==0.29.24<br />
decorator==4.4.2<br />
defer==1.0.6<br />
dell-recovery==0.0.0<br />
distro-info===0.18ubuntu0.18.04.1<br />
hdbscan==0.8.27<br />
httplib2==0.9.2<br />
idna==2.6<br />
imagecodecs==2020.5.30<br />
imageio==2.9.0<br />
imglyb==1.0.0<br />
jgo==1.0.1<br />
joblib==1.0.1<br />
JPype1==1.2.1<br />
keyring==10.6.0<br />
keyrings.alt==3.0<br />
kiwisolver==1.3.1<br />
kneed==0.7.0<br />
language-selector==0.1<br />
launchpadlib==1.10.6<br />
lazr.restfulclient==0.13.5<br />
lazr.uri==1.0.3<br />
libtiff==0.4.2<br />
louis==3.5.0<br />
macaroonbakery==1.1.3<br />
MACS3==3.0.0a6<br />
Mako==1.0.7<br />
MarkupSafe==1.0<br />
matplotlib==3.3.4<br />
netifaces==0.10.4<br />
networkx==2.5.1<br />
numpy==1.19.5<br />
oauth==1.0.1<br />
olefile==0.45.1<br />
PAM==0.4.2<br />
pandas==1.1.5<br />
pexpect==4.2.1<br />
Pillow==8.2.0<br />
progressbar==2.3<br />
protobuf==3.0.0<br />
psutil==5.8.0<br />
pycairo==1.16.2<br />
pycrypto==2.6.1<br />
pycups==1.9.73<br />
pygobject==3.26.1<br />
PyICU==1.9.8<br />
pyimagej==1.0.0<br />
pymacaroons==0.13.0<br />
PyNaCl==1.1.2<br />
pyparsing==2.4.7<br />
pyRFC3339==1.0<br />
python-apt==1.6.5+ubuntu0.5<br />
python-dateutil==2.8.1<br />
python-debian==0.1.32<br />
pytz==2021.1<br />
PyWavelets==1.1.1<br />
pyxdg==0.25<br />
PyYAML==3.12<br />
reportlab==3.4.0<br />
requests==2.18.4<br />
requests-unixsocket==0.1.5<br />
ripleyk==0.0.3<br />
scikit-image==0.15.0<br />
scikit-learn==0.24.2<br />
scipy==1.5.4<br />
scour==0.36<br />
screen-resolution-extra==0.0.0<br />
scyjava==1.1.0<br />
SecretStorage==2.3.1<br />
SELMA==1.0<br />
simplejson==3.13.2<br />
six==1.16.0<br />
system-service==0.3<br />
systemd-python==234<br />
threadpoolctl==2.2.0<br />
tifffile==2020.9.3<br />
typing-extensions==3.10.0.0<br />
ubuntu-drivers-common==0.0.0<br />
ufw==0.36<br />
unattended-upgrades==0.1<br />
urllib3==1.22<br />
usb-creator==0.3.3<br />
wadllib==1.3.2<br />
xarray==0.16.2<br />
xkit==0.0.0<br />
zope.interface==4.3.2<br />

Here is the system info associated with the R sessions:

R version 3.4.4 (2018-03-15)
Platform: x86_64-pc-linux-gnu (64-bit)
Running under: Ubuntu 18.04.5 LTS

Matrix products: default
BLAS: /usr/lib/x86_64-linux-gnu/blas/libblas.so.3.7.1
LAPACK: /usr/lib/x86_64-linux-gnu/lapack/liblapack.so.3.7.1

locale:
 [1] LC_CTYPE=en_US.UTF-8       LC_NUMERIC=C              
 [3] LC_TIME=en_US.UTF-8        LC_COLLATE=en_US.UTF-8    
 [5] LC_MONETARY=en_US.UTF-8    LC_MESSAGES=en_US.UTF-8   
 [7] LC_PAPER=en_US.UTF-8       LC_NAME=C                 
 [9] LC_ADDRESS=C               LC_TELEPHONE=C            
[11] LC_MEASUREMENT=en_US.UTF-8 LC_IDENTIFICATION=C       

attached base packages:
[1] stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:
 [1] pROC_1.17.0.1        Hmisc_4.5-0          Formula_1.2-4       
 [4] survival_3.2-7       scatterplot3d_0.3-41 clue_0.3-59         
 [7] glmnet_2.0-16        foreach_1.5.1        Matrix_1.2-12       
[10] caret_6.0-86         ggplot2_3.3.5        lattice_0.20-41     
[13] xtable_1.8-4        

loaded via a namespace (and not attached):
 [1] Rcpp_1.0.6           lubridate_1.7.10     class_7.3-18        
 [4] digest_0.6.27        ipred_0.9-11         R6_2.5.0            
 [7] plyr_1.8.6           backports_1.2.1      stats4_3.4.4        
[10] pillar_1.4.7         rlang_0.4.10         rstudioapi_0.13     
[13] data.table_1.13.6    rpart_4.1-15         checkmate_2.0.0     
[16] splines_3.4.4        gower_0.2.2          stringr_1.4.0       
[19] foreign_0.8-69       htmlwidgets_1.5.3    munsell_0.5.0       
[22] compiler_3.4.4       xfun_0.21            pkgconfig_2.0.3     
[25] base64enc_0.1-3      htmltools_0.5.1.1    nnet_7.3-15         
[28] tidyselect_1.1.0     tibble_3.0.6         gridExtra_2.3       
[31] htmlTable_2.1.0      prodlim_2019.11.13   codetools_0.2-18    
[34] crayon_1.4.1         dplyr_1.0.4          withr_2.4.1         
[37] MASS_7.3-53.1        recipes_0.1.15       ModelMetrics_1.2.2.2
[40] grid_3.4.4           nlme_3.1-152         gtable_0.3.0        
[43] lifecycle_0.2.0      magrittr_2.0.1       scales_1.1.1        
[46] stringi_1.5.3        reshape2_1.4.4       latticeExtra_0.6-28 
[49] timeDate_3043.102    ellipsis_0.3.1       generics_0.1.0      
[52] vctrs_0.3.6          lava_1.6.9           RColorBrewer_1.1-2  
[55] iterators_1.0.13     tools_3.4.4          glue_1.4.2          
[58] purrr_0.3.4          colorspace_2.0-0     cluster_2.1.0       
[61] knitr_1.31   
