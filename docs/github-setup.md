# GitHub Setup

## Create a GitHub account.

Create a GitHub account if you don't already have one.

## Fork the Apache Airflow repository

Fork [the Apache Airflow repository](https://github.com/apache/airflow/){target=_blank} to your GitHub account.

## Clone your fork locally

```bash
git clone git@github.com:zkan/airflow.git
cd airflow
```

## Add the upstream remote and verify

Add the official Airflow repository as the `upstream` remote:

```bash
git remote add upstream git@github.com:apache/airflow.git
git remote -v
```

You should see both remotes:

- `origin` → your fork
- `upstream` → `apache/airflow`
