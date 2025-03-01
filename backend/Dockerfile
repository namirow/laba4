FROM python:3.9-alpine

WORKDIR /app
COPY requirements.txt /app/ 
RUN pip install --no-cache-dir -r /app/requirements.txt 

ENV PYTHONUNBUFFERED 1


RUN pip install --no-cache-dir -r requirements.txt

COPY . .


EXPOSE 8000
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "backend.wsgi:application"]
