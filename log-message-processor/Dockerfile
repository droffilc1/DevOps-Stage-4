FROM python:3.11-slim

RUN apt update && apt install -y build-essential python3-dev libssl-dev libffi-dev \
  && rm -rf /var/lib/apt/lists/*  # Clean up to reduce image size

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir --upgrade pip setuptools wheel \
  && pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 8000

CMD ["python", "main.py"]

