ARG ALPINE_VERSION=${ALPINE_VERSION}
FROM alpine:${ALPINE_VERSION}

ARG TERRAFORM_VERSION=${TERRAFORM_VERSION}
ARG TERRAGRUNT_VERSION=${TERRAGRUNT_VERSION}
ARG TERRAGRUNT_TFPATH=${TERRAGRUNT_TFPATH}

RUN apk add --no-cache --update git bash wget openssl

ADD https://releases.hashicorp.com/terraform/${TERRAFORM_VERSION}/terraform_${TERRAFORM_VERSION}_linux_amd64.zip ./
ADD https://releases.hashicorp.com/terraform/${TERRAFORM_VERSION}/terraform_${TERRAFORM_VERSION}_SHA256SUMS ./


RUN sed -i '/.*linux_amd64.zip/!d' terraform_${TERRAFORM_VERSION}_SHA256SUMS \
    && sha256sum -cs terraform_${TERRAFORM_VERSION}_SHA256SUMS \
    && unzip terraform_${TERRAFORM_VERSION}_linux_amd64.zip -d /bin \
    && rm -f terraform_${TERRAFORM_VERSION}_linux_amd64.zip \
    && rm -f terraform_${TERRAFORM_VERSION}_SHA256SUMS

ADD https://github.com/gruntwork-io/terragrunt/releases/download/v${TERRAGRUNT_VERSION}/terragrunt_linux_amd64 /bin/terragrunt

RUN chmod +x /bin/terragrunt