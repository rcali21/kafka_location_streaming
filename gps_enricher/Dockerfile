FROM python:3.11-slim

WORKDIR /app

# Install dependencies
RUN pip install --no-cache-dir \
    psycopg2-binary \
    geopy \
    requests

# Copy the enricher script
COPY enricher.py .

# Run the enricher
CMD ["python", "-u", "enricher.py"]