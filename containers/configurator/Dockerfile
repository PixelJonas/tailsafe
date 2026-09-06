FROM registry.access.redhat.com/ubi9/python-312@sha256:414e82ae451b0c31cb4a2b73d888ffcd75652530ac1abedd6905d6fb0e47d463

USER 0
RUN dnf install -y httpd-tools && dnf clean all

WORKDIR /app
COPY scripts /app/scripts
COPY containers/configurator/entrypoint.sh /app/entrypoint.sh

ENTRYPOINT ["/app/entrypoint.sh"]
