FROM python:3

LABEL base_image="python:3"
LABEL software="wintry"
LABEL about.summary="An example project leveraging various automation."
LABEL about.home="https://github.com/d33bs/test-semver-docker-deploy"
LABEL about.documentation="https://github.com/d33bs/test-semver-docker-deploy"
LABEL about.license_file="https://github.com/d33bs/test-semver-docker-deploy/LICENSE"
LABEL about.license="SPDX:BSD-3-Clause"
LABEL about.tags="general"

WORKDIR /usr/src/app

COPY pyproject.toml poetry.lock ./

# hadolint ignore=DL3013
RUN pip install --no-cache-dir poetry poetry-dynamic-versioning

COPY . .

RUN poetry install --no-interaction --no-dev

# hadolint ignore=DL3059
RUN echo 'alias python="poetry run python"' >> ~/.bashrc
