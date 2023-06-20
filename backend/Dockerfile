FROM python:3.9-slim

RUN apt update && apt install -y netcat-traditional

WORKDIR /app

COPY requirements.txt .

RUN pip install -r requirements.txt

COPY blog/ .
COPY entrypoint.sh .

RUN chmod 777 /app/entrypoint.sh
ENTRYPOINT ["/app/entrypoint.sh"]