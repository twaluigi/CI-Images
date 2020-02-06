ARG  PYTHON_VERSION=${PYTHON_VERSION}
FROM python:${PYTHON_VERSION}

ARG AWSCLI_VERSION=${AWSCLI_VERSION}

RUN apt-get update && apt-get install -y --no-install-recommends jq\
    && pip install awscli==$AWSCLI_VERSION --no-cache-dir && apt-get clean