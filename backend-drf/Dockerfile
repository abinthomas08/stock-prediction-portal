FROM python:3.11-slim

# Install build dependencies
RUN apt-get update && apt-get install -y \
    gcc \
    g++ \
    libpq-dev \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY backend-drf/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY backend-drf .

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
