FROM pytorch/pytorch:1.13.1-cuda11.6-cudnn8-runtime
WORKDIR /app
COPY ./requirements.txt ./requirements.txt
RUN apt-get -y update
RUN apt-get -y install git
RUN python -m pip install --upgrade pip
RUN pip install -r requirements.txt
RUN pip install torch-scatter==2.1.1 torch-sparse==0.6.17 -f https://data.pyg.org/whl/torch-1.13.1+cu116.html
RUN pip install git+https://github.com/TorchSpatiotemporal/tsl.git
RUN pip install pytorch-lightning==1.7.7