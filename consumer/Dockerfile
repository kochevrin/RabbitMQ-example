# basic python image
FROM python:3.12-alpine

# install pika to access rabbitmq
COPY requirements.txt /app/consumer/requirements.txt
RUN pip install -r /app/consumer/requirements.txt

# Without this setting, Python never prints anything out.
ENV PYTHONUNBUFFERED=1

# declare the source directory
WORKDIR /app/consumer

# copy the file
COPY consumer.py .

# start command
CMD [ "python", "consumer.py" ]
