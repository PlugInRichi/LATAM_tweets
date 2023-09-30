FROM alpine:3.14

ENV PYTHONUNBUFFERED=1

RUN mkdir src

COPY requirements.txt ~/requirements.txt
COPY ../src ~/src

RUN apk add --update --no-cache python3 && ln -sf python3 /usr/bin/python
RUN python3 -m ensurepip
RUN pip3 install --no-cache --upgrade pip setuptools
RUN apk add gcc python3-dev musl-dev linux-headers
RUN pip install -r requirements.txt

WORKDIR ~

EXPOSE 8888