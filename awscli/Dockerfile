FROM python:3.7.4-slim-buster

ENV AWSCLI_VERSION

RUN apt-get update && apt-get install jq --no-install-recommends -y && rm -rf /var/lib/apt/lists/*
RUN pip install awscli==${AWSCLI_VERSION} --no-cache-dir
CMD ["python3"]