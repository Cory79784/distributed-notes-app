FROM python:3.12-slim

RUN apt-get update && apt-get install -y \
    g++ \
    gcc \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /notification-service

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

CMD ["python", "notification.py"]
