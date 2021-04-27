FROM python:3

WORKDIR /app
ENV PIP_DISABLE_PIP_VERSION_CHECK=1
ENV PIP_NO_CACHE_DIR=1
# lets only reload requirements when the file has actually changed
COPY requirements.txt ./
RUN pip install -r requirements.txt
# now let's copy the rest
COPY ./* ./

EXPOSE 80
ENTRYPOINT ["uvicorn", "server:app", "--host", "0.0.0.0", "--port", "80"]

