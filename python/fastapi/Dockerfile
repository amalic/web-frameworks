FROM python:3

WORKDIR /app
# lets only reload requirements when the file has actually changed
COPY requirements.txt ./
RUN pip install -r requirements.txt


COPY ./* ./

EXPOSE 80
ENTRYPOINT ["uvicorn", "server:app", "--host", "0.0.0.0", "--port", "80"]

