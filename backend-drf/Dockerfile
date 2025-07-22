# backend-drf/Dockerfile
FROM python:3.11-slim

WORKDIR /app

COPY backend-drf/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY backend-drf .

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
