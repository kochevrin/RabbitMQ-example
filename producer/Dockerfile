# basic python image
FROM python:3.12-alpine

# install pika to access rabbitmq
COPY requirements.txt /app/producer/requirements.txt
RUN pip install -r /app/producer/requirements.txt

# Without this setting, Python never prints anything out.
ENV PYTHONUNBUFFERED=1

# declare the source directory
WORKDIR /app/producer

# copy the file
COPY producer.py .

# start command
CMD [ "python", "producer.py" ]
