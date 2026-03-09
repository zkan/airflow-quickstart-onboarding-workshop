# Preparing the Local Development Environment

Before contributing to Apache Airflow, we need to prepare the local development environment. In this section, we will install several tools used throughout the workshop:

- **Docker** - runs the Airflow development environment in containers
- **mise** - manages development runtimes such as Python and uv
- **Python** - the programming language used to develop Apache Airflow
- **uv** - a fast Python package manager
- **prek** - runs code quality checks before committing changes

These tools ensure a consistent environment for developing and contributing to Airflow.

## Install Docker

Docker is required to run the Airflow development environment because Breeze uses Docker containers to manage services and dependencies.

Ensure Docker is installed and running on your machine.

## Install mise

[mise](https://mise.jdx.dev/){target=_blank} is a runtime manager that helps install and manage development tools such as Python and uv.

Install it using the following command:

```bash
curl https://mise.run | sh
```

## Install Python using mise

Apache Airflow requires Python. We use mise to install and manage the Python version used for development.

```bash
mise use -g python@3.14.0
```

Verify the installation:

```bash
python --version
```

## Install uv using mise

[uv](https://github.com/astral-sh/uv){target=_blank} is a fast Python package manager used in the Airflow development workflow.

Install it using `mise`:

```bash
mise use -g uv@0.10.0
```

Verify the installation:

```bash
uv --version
```

## Install prek

[prek](https://github.com/j178/prek){target=_blank} is a pre-commit runner used in the Airflow project to run code quality checks automatically before committing changes.

Install it with:

```bash
uv tool install prek
```
