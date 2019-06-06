FROM registry.access.redhat.com/ubi7/ubi-minimal:latest

ENV OPERATOR=/usr/local/bin/packu \
    USER_UID=1001 \
    USER_NAME=packu

# install operator binary
COPY build/_output/bin/packu ${OPERATOR}

COPY build/bin /usr/local/bin
RUN  /usr/local/bin/user_setup

ENTRYPOINT ["/usr/local/bin/entrypoint"]

USER ${USER_UID}
