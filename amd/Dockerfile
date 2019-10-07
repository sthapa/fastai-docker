FROM rocm/pytorch:rocm2.7_ubuntu18.04_py3.6_pytorch

RUN apt-get update && apt-get install -y --no-install-recommends \
        gfortran \
        git \
        liblapack-dev \
        libopenblas-dev \
        graphviz \
        cmake \
        && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

RUN pip install --no-cache-dir fastai fastai jupyter_contrib_nbextensions 

RUN mkdir /tf && cd /tf && git clone https://github.com/fastai/course-v3

RUN jupyter contrib nbextension install --user && \
    jupyter nbextensions_configurator enable --user

