FROM python:3.12.4

WORKDIR /app

RUN pip install gunicorn==23.0.0

COPY requirements.txt .

RUN pip install -r requirements.txt

COPY . .

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "backend.wsgi"]

