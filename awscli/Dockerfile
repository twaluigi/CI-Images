ARG  PYTHON_VERSION=${PYTHON_VERSION}
FROM python:${PYTHON_VERSION}-slim-buster

ARG AWSCLI_VERSION="${AWSCLI_VERSION}"

RUN apt-get update && apt-get install jq --no-install-recommends -y && rm -rf /var/lib/apt/lists/*
RUN pip install awscli==$AWSCLI_VERSION --no-cache-dir
CMD ["python3"]