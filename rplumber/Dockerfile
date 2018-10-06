FROM trestletech/plumber

RUN apt-get update && apt-get -y upgrade && apt-get install -y \
  build-essential git-core libssl-dev libffi-dev libcurl4-openssl-dev \
  libxml2-dev g++ \
  libcairo2-dev \
  libsqlite3-dev \
  libmariadbd-dev \
  libmariadb-client-lgpl-dev \
  libpq-dev \
  libssh2-1-dev \
  unixodbc-dev \
  libudunits2-dev libgdal-dev libproj-dev gdal-bin proj-bin \
  && R -e "source('https://bioconductor.org/biocLite.R')" \
  && install2.r --error \
    --deps TRUE \
    Rcpp \
    tidyverse \
    dplyr \
    ggplot2 \
    devtools \
    formatR \
    remotes \
    selectr \
    caTools \
    caret \
    data.table \
    gbm \
    pROC \
    xgboost \
    corrplot \
    dummies \
    pbapply \
    doMC \
    ROCR \
    jsonlite

RUN install2.r --dep TRUE units
