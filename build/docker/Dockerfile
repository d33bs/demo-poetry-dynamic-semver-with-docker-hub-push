FROM python:3

# set various metadata, loosely following biocontainers standards from:
# https://biocontainers-edu.readthedocs.io/en/latest/what_is_biocontainers.html
LABEL base_image="python:3"
LABEL software="wintry"
LABEL about.summary="An example project leveraging various automation."
LABEL about.home="https://github.com/CU-DBMI/demo-poetry-dynamic-semver-with-docker-hub-push"
LABEL about.documentation="https://github.com/CU-DBMI/demo-poetry-dynamic-semver-with-docker-hub-push"
LABEL about.license_file="https://github.com/CU-DBMI/demo-poetry-dynamic-semver-with-docker-hub-push/blob/main/LICENSE"
LABEL about.license="SPDX:BSD-3-Clause"

# set the workdir to /app
WORKDIR /app

# copy pyproject and poetry lockfile for stepped installation
COPY pyproject.toml poetry.lock ./

# install poetry and poetry dynamic versioning
# hadolint ignore=DL3013
RUN pip install --no-cache-dir poetry poetry-dynamic-versioning

# copy the rest of the repository
COPY . .

# install the project from poetry
RUN poetry install --no-interaction

# set an alias for running python through the poetry env
# hadolint ignore=DL3059
RUN echo 'alias python="poetry run python"' >> ~/.bashrc
