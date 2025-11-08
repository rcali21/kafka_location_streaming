FROM python:3.11-slim

# System deps (optional but handy)
RUN apt-get update && apt-get install -y --no-install-recommends curl && rm -rf /var/lib/apt/lists/*

WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY app.py .

# Expose the service
EXPOSE 5000

# Run FastAPI via uvicorn, bind to all interfaces
CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "5000"]
