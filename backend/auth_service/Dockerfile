FROM python:3.9-slim

WORKDIR /app

COPY backend/auth_service/requirements.txt ./requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

COPY backend/auth_service/src/ /app/src/
COPY backend/common/ /app/common/

ENV PYTHONPATH=/app

CMD ["uvicorn", "src.main:app", "--host", "0.0.0.0", "--port", "8000"]
