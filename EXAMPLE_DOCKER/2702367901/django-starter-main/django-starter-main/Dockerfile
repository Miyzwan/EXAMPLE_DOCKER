# Stage 1: Build
FROM python:3.11-slim AS builder

WORKDIR /app

# Install build dependencies
RUN apt-get update && apt-get install -y build-essential libpq-dev && rm -rf /var/lib/apt/lists/*

# Install Python dependencies into /install
COPY requirements.txt .
RUN pip install --upgrade pip && pip install --prefix=/install -r requirements.txt

# Stage 2: Production
FROM python:3.11-slim

WORKDIR /app

# Copy installed dependencies from builder
COPY --from=builder /install /usr/local

# Copy project files
COPY . .

# Collect static files (optional, jika pakai static)
RUN python manage.py collectstatic --noinput

# Expose port (default Django)
EXPOSE 8000

# Jalankan migrasi sebelum start (opsional, bisa juga pakai entrypoint script)
CMD ["sh", "-c", "python manage.py migrate && python manage.py runserver 0.0.0.0:8000"]