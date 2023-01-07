 # syntax=docker/dockerfile:1
FROM rocker/r-base:4.2.2

# external depencencies as deb packages
# each apt call absoluterly positively must be on a single line (so that update & install end up in the same Docker cache)
RUN apt-get update && apt-get -y install libgdal-dev=3.6.1+dfsg-1+b1
RUN apt-get update && apt-get -y install libgeos-dev=3.11.1-1
RUN apt-get update && apt-get -y install libproj-dev=9.1.1-1
RUN apt-get update && apt-get -y install libudunits2-dev
RUN apt-get update && apt-get -y install libxml2-dev
RUN apt-get update && apt-get -y install libv8-dev
RUN apt-get update && apt-get -y install libjq-dev
RUN apt-get update && apt-get -y install libprotobuf-dev
RUN apt-get update && apt-get -y install protobuf-compiler
RUN apt-get update && apt-get -y install libxtst6
RUN apt-get update && apt-get -y install libfontconfig1-dev
RUN apt-get update && apt-get -y install libharfbuzz-dev
RUN apt-get update && apt-get -y install libfribidi-dev
RUN apt-get update && apt-get -y install libfreetype6-dev
RUN apt-get update && apt-get -y install libpng-dev
RUN apt-get update && apt-get -y install libtiff5-dev
RUN apt-get update && apt-get -y install libjpeg-dev
RUN ldconfig


# R packagoptions(warn=2); es from POSIT; R 4.2.2 image is based on ubuntu:jammy
RUN R -e "options(warn=2); install.packages('czso', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('dplyr', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('ggplot2', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('giscoR', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('gtools', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('hereR', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('htmltools', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('knitr', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('leaflet', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('lwgeom', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('mapview', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('exactextractr', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('nngeo', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('osmdata', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('raster', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('RCzechia', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('readr', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('remotes', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('rgeoda', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('rmapshaper', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('rmarkdown', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('scales', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('sf', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('spdep', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('tidygeocoder', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('tidyr', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('tidyverse', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); install.packages('languageserver', repos = 'https://packagemanager.rstudio.com/cran/__linux__/jammy/2022-12-01')"
RUN R -e "options(warn=2); remotes::install_github('ManuelHentschel/vscDebugger@v0.5.2')"