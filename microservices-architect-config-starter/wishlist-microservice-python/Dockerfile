FROM python:3
MAINTAINER dharma
WORKDIR /app
COPY . .
#to install we need to use to flask
RUN pip install flask flask_cors

EXPOSE 1003

CMD ["python","index.py"]
