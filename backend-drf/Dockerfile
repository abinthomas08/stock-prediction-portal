FROM python:3.11-slim

# Install system build dependencies
RUN apt-get update && apt-get install -y \
    build-essential \
    gcc \
    g++ \
    libffi-dev \
    libssl-dev \
    libpq-dev \
    && rm -rf /var/lib/apt/lists/*

# Set working directory
WORKDIR /app

# Install Python deps
COPY backend-drf/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy rest of the backend app
COPY backend-drf .

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
