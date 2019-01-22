FROM python:3.5

# Airflow environment setup
ENV AIRFLOW_GPL_UNIDECODE=True
ENV AIRFLOW_HOME=/opt/airflow

# Requirements installation
COPY requirements.txt /requirements.txt
RUN pip install -r requirements.txt

# Working dir setup
RUN mkdir -p /opt/airflow \
    && chown nobody /opt/airflow

USER nobody
WORKDIR /opt/airflow

# The basic command. Overrided by compose for
# service specification