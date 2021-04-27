FROM python:3

WORKDIR /app
COPY ./* ./
RUN pip install -r requirements.txt

EXPOSE 80
ENTRYPOINT ["uvicorn", "server:app", "--host", "0.0.0.0", "--port", "80"]

