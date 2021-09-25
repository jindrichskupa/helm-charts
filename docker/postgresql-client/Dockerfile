FROM debian:stable-slim
ARG POSTGRES_VERSION

RUN echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list && \
    wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | apt-key add - && \
    apt update && apt -y install postgresql-client-$POSTGRES_VERSION && \
    apt-get autoremove -y && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists
