FROM ubuntu:18.04
LABEL version="0.4.1"

RUN apt update \
    && apt install -y \
        wget \
        git \
        python3 \
        python3-pip \
        libbz2-dev \
        liblzma-dev \
        libcurl4-gnutls-dev \
        zlib1g-dev

RUN pip3 install --quiet \
    cython \
    setuptools

RUN pip3 install --quiet \
    pysam \
    bx-python \
    pyBigWig \
    numpy

RUN pip3 install --quiet \
    git+https://github.com/liguowang/CrossMap.git@618492c16c83f1366af3429795617554018e5315#egg=CrossMap

WORKDIR /chain_files/human/

RUN wget -nv ftp://ftp.ensembl.org/pub/assembly_mapping/homo_sapiens/*.chain.gz
