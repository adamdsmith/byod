FROM rocker/binder:3.6.0
LABEL maintainer='Adam Smith'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}



RUN wget https://github.com/adamdsmith/byod/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2019-09-04/')); devtools::install_deps()"

RUN rm DESCRIPTION.1
