# EPICS
Extracting Physical-Characteristics from Images of Chromatin Structures (EPICS) is a machine-learning based computational method for processing high-resolution chromatin 3D image data. 

## Repository Organization

Each of the experiments associated with EPICS is provided in respective branches.  Specifically, experiments were done on 3D-EMISH and 3D-SIM data.  Those experiments (code, associated data, and output) are all provided in their respective branches.  The .py files in each branch collect the features from the raw data.  The .r files build the models for classifying open and closed chromatin domains (CDs).   

## Data

Raw 3D-EMISH data was obtained from Trzaskoma et.al.'s GitHub (https://github.com/3DEMISH/3D-EMISH).  Raw 3D-SIM images were obtained from Cremer et.al.'s 2020 paper (https://datadryad.org/stash/dataset/doi:10.5061/dryad.vt4b8gtqb).   

## System Information

The computation was performed on a Ubuntu 18.04.5 system with 64 GB of RAM and an Intel® Xeon(R) W-2245 CPU @ 3.90GHz with 8 cores and 16 threads.  Python and R were used to implement EPICS and many visualizations.  ImageJ was used to create some of the 3D .gifs.

Below is a list of the installed versions of the Python libraries (as of Janurary 2021):

apt-clone==0.2.1
apturl==0.5.2
asn1crypto==0.24.0
Brlapi==0.6.6
certifi==2018.1.18
chardet==3.0.4
command-not-found==0.3
cryptography==2.1.4
cupshelpers==1.0
cycler==0.10.0
cykhash==1.0.2
Cython==0.29.24
decorator==4.4.2
defer==1.0.6
dell-recovery==0.0.0
distro-info===0.18ubuntu0.18.04.1
hdbscan==0.8.27
httplib2==0.9.2
idna==2.6
imagecodecs==2020.5.30
imageio==2.9.0
imglyb==1.0.0
jgo==1.0.1
joblib==1.0.1
JPype1==1.2.1
keyring==10.6.0
keyrings.alt==3.0
kiwisolver==1.3.1
kneed==0.7.0
language-selector==0.1
launchpadlib==1.10.6
lazr.restfulclient==0.13.5
lazr.uri==1.0.3
libtiff==0.4.2
louis==3.5.0
macaroonbakery==1.1.3
MACS3==3.0.0a6
Mako==1.0.7
MarkupSafe==1.0
matplotlib==3.3.4
netifaces==0.10.4
networkx==2.5.1
numpy==1.19.5
oauth==1.0.1
olefile==0.45.1
PAM==0.4.2
pandas==1.1.5
pexpect==4.2.1
Pillow==8.2.0
progressbar==2.3
protobuf==3.0.0
psutil==5.8.0
pycairo==1.16.2
pycrypto==2.6.1
pycups==1.9.73
pygobject==3.26.1
PyICU==1.9.8
pyimagej==1.0.0
pymacaroons==0.13.0
PyNaCl==1.1.2
pyparsing==2.4.7
pyRFC3339==1.0
python-apt==1.6.5+ubuntu0.5
python-dateutil==2.8.1
python-debian==0.1.32
pytz==2021.1
PyWavelets==1.1.1
pyxdg==0.25
PyYAML==3.12
reportlab==3.4.0
requests==2.18.4
requests-unixsocket==0.1.5
ripleyk==0.0.3
scikit-image==0.15.0
scikit-learn==0.24.2
scipy==1.5.4
scour==0.36
screen-resolution-extra==0.0.0
scyjava==1.1.0
SecretStorage==2.3.1
SELMA==1.0
simplejson==3.13.2
six==1.16.0
system-service==0.3
systemd-python==234
threadpoolctl==2.2.0
tifffile==2020.9.3
typing-extensions==3.10.0.0
ubuntu-drivers-common==0.0.0
ufw==0.36
unattended-upgrades==0.1
urllib3==1.22
usb-creator==0.3.3
wadllib==1.3.2
xarray==0.16.2
xkit==0.0.0
zope.interface==4.3.2

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
