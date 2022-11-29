FROM python:3
RUN pip install --no-cache-dir hashtable-nicolerg

WORKDIR /
COPY .python_startup .
ENV PYTHONSTARTUP=./.python_startup
