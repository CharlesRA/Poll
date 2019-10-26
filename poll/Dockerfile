FROM python:3

RUN mkdir /poll

WORKDIR /poll

COPY requirements.txt /poll/

RUN pip install -r requirements.txt

COPY . /poll/

CMD flask run --host=0.0.0.0 --port=80
