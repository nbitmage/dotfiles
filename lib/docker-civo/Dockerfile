FROM civo/cli:latest

RUN apk add --update --no-cache --virtual .deps curl shadow

# Add kubectl for `civo k8s`
RUN curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl \
 && chmod +x ./kubectl \
 && mv ./kubectl /usr/local/bin/kubectl

# Clean up
RUN apk del .deps
