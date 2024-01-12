FROM ubuntu:22.04
LABEL authors="evgeny"

RUN apt-get update && apt-get -y install python3 python3-pip

COPY requirements.txt /opt/app/requirements.txt
WORKDIR /opt/app
RUN pip3 install -r requirements.txt
COPY . /opt/app

ENTRYPOINT ["pycodestyle", "functions.py"]