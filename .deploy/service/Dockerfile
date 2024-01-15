FROM nvidia/cuda:11.8.0-runtime-ubuntu20.04
WORKDIR /root

RUN apt update && \
        apt -y install python3-pip

COPY requirements.txt .
RUN pip3 install -r requirements.txt

COPY wheels/ ./wheels
RUN pip3 install wheels/*

COPY src/ .

CMD ["python3", "main.py"]
EXPOSE 80