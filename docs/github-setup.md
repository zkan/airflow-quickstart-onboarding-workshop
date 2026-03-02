# GitHub Setup

## Create a GitHub account.

If you don't already have one.

## Fork the Apache Airflow repository

Fork [the Apache Airflow repository](https://github.com/apache/airflow/){target=_blank}.

## Clone your fork locally

```bash
git clone git@github.com:zkan/airflow.git
cd airflow
```

## Add the upstream remote and verify

```bash
git remote add upstream git@github.com:apache/airflow.git
git remote -v
```

You should see both:

- `origin` → your fork
- `upstream` → apache/airflow
