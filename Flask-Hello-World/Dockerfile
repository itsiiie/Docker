# ────── Builder Stage ──────
FROM python:3.11-slim AS builder

WORKDIR /app

# Copy only requirements first for caching
COPY requirements.txt .

# Install dependencies
RUN pip install --prefix=/install --no-cache-dir -r requirements.txt

# ────── Final Stage ──────
FROM python:3.11-slim

WORKDIR /app

# Copy installed packages from builder
COPY --from=builder /install /usr/local

# Copy app code
COPY app.py .

EXPOSE 5000

CMD ["python", "app.py"]
