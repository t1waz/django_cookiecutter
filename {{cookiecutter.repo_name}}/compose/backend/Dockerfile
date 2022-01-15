FROM python:3.8

WORKDIR /app

RUN mkdir /entrypoint

COPY ./requirements.txt /app

COPY ./compose/backend/entrypoint.sh /entrypoint
RUN chmod +x /entrypoint/entrypoint.sh

RUN apt-get update

RUN pip install --upgrade pip \
    && pip install -r requirements.txt

ENTRYPOINT ["/entrypoint/entrypoint.sh"]
