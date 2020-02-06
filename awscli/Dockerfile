ARG  PYTHON_VERSION=${PYTHON_VERSION}
FROM python:${PYTHON_VERSION}

ARG AWSCLI_VERSION=${AWSCLI_VERSION}

RUN apk add --no-cache --update jq\
    && pip install awscli==$AWSCLI_VERSION --no-cache-dir