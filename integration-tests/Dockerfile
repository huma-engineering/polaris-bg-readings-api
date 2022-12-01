FROM python:3.9-slim

WORKDIR /app

RUN apt-get update -y && apt-get upgrade -y

# Install dependencies
ADD requirements.txt .
RUN apt-get update \
    && pip install -r requirements.txt

# Add the app
ADD . .

# Engage.
CMD ["behave", "--no-capture"]
