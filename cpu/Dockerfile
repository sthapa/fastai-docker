FROM tensorflow/tensorflow:1.13.2-py3-jupyter

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

RUN pip install torch==1.2.0+cpu torchvision==0.4.0+cpu -f https://download.pytorch.org/whl/torch_stable.html

RUN pip install --no-cache-dir fastai fastai jupyter_contrib_nbextensions 

RUN cd /tf && git clone https://github.com/fastai/course-v3

RUN cd /tf && ln -s course-v3/nbs/dl1 part1-lessions
RUN cd /tf && ln -s course-v3/nbs/dl2 part2-lessions

RUN jupyter contrib nbextension install --user && \
    jupyter nbextensions_configurator enable --user

