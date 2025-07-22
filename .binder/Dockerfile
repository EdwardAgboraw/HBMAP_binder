FROM rocker/binder:latest
LABEL maintainer='Edward Agboraw'
COPY --chown=${NB_USER} . ${HOME}
USER ${NB_USER}



RUN wget https://github.com/EdwardAgboraw/HBMAP_binder/raw/main/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2025-07-22/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
