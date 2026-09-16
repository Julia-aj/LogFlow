FROM python:3.11-slim

WORKDIR /app

COPY ingestion/requirements.txt /app/ingestion/requirements.txt
RUN pip install --no-cache-dir -r /app/ingestion/requirements.txt

COPY ingestion /app/ingestion

ENTRYPOINT ["python", "ingestion/producer.py"]
CMD ["--scenario", "normal"]
