FROM python:3.11-slim

# Add build tools and system libs
RUN apt-get update && apt-get install -y \
    gcc \
    g++ \
    build-essential \
    libffi-dev \
    libssl-dev \
    libpq-dev \
    python3-dev \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY backend-drf/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY backend-drf .

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
