FROM python:3

WORKDIR /usr/src/app

COPY pyproject.toml poetry.lock ./

# hadolint ignore=DL3013
RUN pip install --no-cache-dir poetry poetry-dynamic-versioning && \
    poetry install

COPY . .
