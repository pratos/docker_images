FROM python:3.6

RUN apt-get update && apt-get install -y tesseract-ocr

COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

RUN mkdir /data /notebooks

# Setting up volumes
VOLUME ["/data", "/notebooks"]

EXPOSE 8888

CMD jupyter notebook --no-browser --ip=0.0.0.0 --allow-root --NotebookApp.token='ocr'
