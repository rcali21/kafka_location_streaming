FROM python:3.11-slim

WORKDIR /app

# Install dependencies
RUN pip install --no-cache-dir kafka-python psycopg2-binary

# Copy the consumer script
COPY consumer.py .

# Run the consumer
CMD ["python", "consumer.py"]