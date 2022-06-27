FROM python@sha256:b7e449e11f8c466fbaf021dcc731563cb36a41321420db3cf506ba4d71d33a65
# image tage python:3.9.13

ARG AIRFLOW_VERSION=2.3.2
ARG CONSTRAINT_URL="https://raw.githubusercontent.com/apache/airflow/constraints-${AIRFLOW_VERSION}/constraints-3.9.txt"

RUN echo $CONSTRAINT_URL
RUN pip install "apache-airflow==${AIRFLOW_VERSION}" --constraint "${CONSTRAINT_URL}"

# The Standalone command will initialise the database, make a user,
# and start all components for you.
ENTRYPOINT ["airflow", "standalone"]
