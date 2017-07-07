FROM r-base

RUN apt-get update && apt-get -y upgrade && apt-get install -y python3-pip \
	build-essential libssl-dev libffi-dev python3-dev libcurl4-gnutls-dev

RUN python3 -V

RUN pip3 install rpy2

#setup R configs
RUN echo "r <- getOption('repos'); r['CRAN'] <- 'http://cran.us.r-project.org'; options(repos = r);" > ~/.Rprofile
RUN Rscript -e "install.packages(c('gbm', 'xgboost', 'e1071', 'rpart', 'nnet', 'glmnet', 'randomForest', 'arules', 'tree', 'class', 'tm', 'C50','caret'))"
