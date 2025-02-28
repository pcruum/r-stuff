FROM rocker/rstudio

# Install system dependencies required for C++ compilation and R package building
RUN apt-get update && apt-get install -y \
    build-essential \
    libcurl4-gnutls-dev \
    libssl-dev \
    libxml2-dev \
    git && \
    rm -rf /var/lib/apt/lists/*

RUN R -e "install.packages('cmdstanr', repos = c('https://stan-dev.r-universe.dev', getOption('repos')))"

RUN R -e "cmdstanr::install_cmdstan(cores = 4);"

RUN R -e "install.packages(c('coda','mvtnorm','devtools','loo','dagitty','shape', 'rmarkdown', 'languageserver', 'knitr', 'ggplot2', 'tidyverse', 'dataframeexplorer'))"

# set the working directory
WORKDIR /home/r-stuff

RUN R -e "install.packages('/home/r-stuff/rethinking_2.42.tar.gz', repos=NULL)"
