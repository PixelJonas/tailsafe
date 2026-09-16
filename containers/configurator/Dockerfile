FROM registry.access.redhat.com/ubi9/python-312@sha256:608649675c344ac80d58842b883515f39a2232398386805bc6a741f823340a4e

USER 0
RUN dnf install -y httpd-tools && dnf clean all

WORKDIR /app
COPY scripts /app/scripts
COPY containers/configurator/entrypoint.sh /app/entrypoint.sh

ENTRYPOINT ["/app/entrypoint.sh"]
