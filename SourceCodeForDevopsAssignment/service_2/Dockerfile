# service_2/Dockerfile

FROM python:3.10-slim

WORKDIR /app

COPY . .

RUN pip install --no-cache-dir flask

EXPOSE 8002

CMD ["python", "app.py", "--host=0.0.0.0", "--port=8002"]
