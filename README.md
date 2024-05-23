# post-disaster-comms

[![ssec](https://img.shields.io/badge/SSEC-Project-purple?logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAA0AAAAOCAQAAABedl5ZAAAACXBIWXMAAAHKAAABygHMtnUxAAAAGXRFWHRTb2Z0d2FyZQB3d3cuaW5rc2NhcGUub3Jnm+48GgAAAMNJREFUGBltwcEqwwEcAOAfc1F2sNsOTqSlNUopSv5jW1YzHHYY/6YtLa1Jy4mbl3Bz8QIeyKM4fMaUxr4vZnEpjWnmLMSYCysxTcddhF25+EvJia5hhCudULAePyRalvUteXIfBgYxJufRuaKuprKsbDjVUrUj40FNQ11PTzEmrCmrevPhRcVQai8m1PRVvOPZgX2JttWYsGhD3atbHWcyUqX4oqDtJkJiJHUYv+R1JbaNHJmP/+Q1HLu2GbNoSm3Ft0+Y1YMdPSTSwQAAAABJRU5ErkJggg==&style=plastic)](https://ise.washington.edu/news/article/2024-01-14/building-community-resilience-2-million-nsf-grant-will-transform-disaster)
[![BSD License](https://badgen.net/badge/license/BSD-3-Clause/blue)](LICENSE)

This repository is a collection of resources for post-disaster communications. It is a work in progress and will be updated as the project progresses.

## Infrastructure Setup

There are some infrastructure tools that are needed to run supabase in the server.

1. Docker: Docker will be the underlying platform for running the container applications for the backend.
    To install docker in ubuntu, follow the instructions in the [official documentation](https://docs.docker.com/engine/install/ubuntu/).

    **Note: To allow docker to run as non-root user, do `sudo usermod -aG docker ubuntu`**

2. k3d: k3d is a lightweight wrapper to run k3s (A certified lightweight Kubernetes distribution) in docker. It is used to run the kubernetes cluster for the backend. To install k3d, follow the instructions in the [official documentation](https://k3d.io/v5.6.3/#installation).

3. kubectl: kubectl is the command line tool for interacting with the kubernetes cluster. To install kubectl, follow the instructions in the [official documentation](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/#install-kubectl-binary-with-curl-on-linux).

4. Helm: Helm is the package manager for kubernetes. To install helm, follow the instructions in the [official documentation](https://helm.sh/docs/intro/install/).

5. Stern: Stern is a tool for tailing multiple pods on kubernetes. To install stern, follow the instructions in the [official documentation](https://github.com/stern/stern?tab=readme-ov-file#installation).

## Supabase Setup

Supabase is an open source Firebase alternative. It is a service that provides a Postgres database with a RESTful API and real-time capabilities. It is used as the backend for the project.

For this project, we will be utilizing the community supabase kubernetes helm chart.
The helm chart can be found in [supabase-community/supabase-kubernetes](https://github.com/supabase-community/supabase-kubernetes).

Deploying supabase via Kubernetes allows for a cloud agnostic deployment as long as a Kubernetes cluster is available.

See [Official Documentation](https://supabase.com/docs)

## Flutter

Flutter is an open-source UI software development kit created by Google.

This will be used for the mobile application development.

See [Official Documentation](https://flutter.dev/docs)

## Contributing

You can contribute to this project by creating issues or forking this repository and opening a pull request.

Please review our [Code of Conduct](./CODE_OF_CONDUCT.md) before contributing.

## License

[BSD 3-Clause License](./LICENSE)
