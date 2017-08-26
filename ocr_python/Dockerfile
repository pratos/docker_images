FROM ubuntu:16.04

RUN apt-get update
RUN apt-get install -y software-properties-common vim
RUN add-apt-repository ppa:jonathonf/python-3.6
RUN apt-get update

RUN apt-get install -y build-essential python3.6 python3.6-dev python3-pip python3.6-venv libmagickwand-dev python-wand

# update pip
RUN python3.6 -m pip install pip --upgrade
RUN python3.6 -m pip install wheel
  
COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

RUN mkdir /data /notebooks

# Setting up volumes
VOLUME ["/data", "/notebooks"]

EXPOSE 8888

CMD jupyter notebook --no-browser --ip=0.0.0.0 --allow-root --NotebookApp.token='ocr'
