FROM rocker/tidyverse:3.6.3

RUN apt-get update -qq && apt-get -y --no-install-recommends install libhdf5-dev

RUN R -e "install.packages('ids')"
RUN R -e "install.packages('askpass')"
RUN R -e "BiocManager::install('DropletUtils')"
RUN R -e "BiocManager::install('biomaRt')"
RUN installGithub.r -d TRUE \
  NathanSkene/One2One \
  hhoeflin/hdf5r \
  mojaveazure/loomR@develop \
  neurogenomics/scFlowExample

#RUN R -e "devtools::install_github('NathanSkene/One2One')"
#RUN R -e "devtools::install_github('hhoeflin/hdf5r')"
#RUN R -e "devtools::install_github('mojaveazure/loomR', ref = 'develop')"
#RUN R -e "devtools::install_github('neurogenomics/scFlowExample')"
