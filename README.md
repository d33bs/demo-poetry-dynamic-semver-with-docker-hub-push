# Demonstrational Python Poetry Dynamic Semver with Docker Hub Push

A demonstrational repository showing how Python [Poetry](https://python-poetry.org/docs/) dynamic versioning can be used to distribute [Docker container images](https://docs.docker.com/guides/walkthroughs/what-is-a-container/) on [Docker Hub](https://www.docker.com/products/docker-hub) for Python packages.

As part of this work, we do the following:

- Include a demonstrational Python package called "wintry" managed by [`poetry-dynamic-versioning`](https://github.com/mtkennerly/poetry-dynamic-versioning)
- Test a Docker image build and the Python package tests through the built image via [GitHub Actions](https://docs.github.com/en/actions) triggered on pull request
- Update the version through [GitHub Releases](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases)
- Build and push a Docker image to Docker Hub triggered by GitHub Release via GitHub Actions with use of [GitHub repository secrets](https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions) associated with Docker Hub.

## References

Docker Hub repository: [https://hub.docker.com/r/d33bs/wintry](https://hub.docker.com/r/d33bs/wintry)

Source code: [https://github.com/CU-DBMI/demo-poetry-dynamic-semver-with-docker-hub-push](https://github.com/CU-DBMI/demo-poetry-dynamic-semver-with-docker-hub-push)
