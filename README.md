# Getting Started Contributing to Apache Airflow: Quickstart Onboarding Workshop

## Instruction

### Prepare the Local Development Environment

#### Install Docker

Ensure Docker is installed and running on your machine.

#### Install [mise](https://mise.jdx.dev/).

```bash
curl https://mise.run | sh
```

#### Install Python using mise

```bash
mise use -g python@3.14.0
```

Verify:

```bash
python --version
```

#### Install [uv](https://github.com/astral-sh/uv) using mise

```bash
mise use -g uv@0.10.0
```

Verify:

```bash
uv --version
```

#### Install [prek](https://github.com/j178/prek)

```bash
uv tool install prek
```

### GitHub Setup

#### Create a GitHub account.

If you don’t already have one.

#### Fork the Apache Airflow repository

Fork [the Apache Airflow repository](https://github.com/apache/airflow/).

#### Clone your fork locally

```bash
git clone git@github.com:zkan/airflow.git
cd airflow
```

#### Add the upstream remote and verify

```bash
git remote add upstream git@github.com:apache/airflow.git
git remote -v
```

You should see both:
- `origin` → your fork
- `upstream` → apache/airflow

### Install Breeze

#### Install Breeze (Airflow dev CLI)

From the repository root:

```bash
uv tool install -e ./dev/breeze
```

Verify:

```bash
breeze --help
```

### Start Contributing

In this workshop, we’ll start with documentation or translation contributions. These are the easiest and most beginner-friendly ways to get involved.

You don't need to understand Airflow internals — just improve clarity or language support.

#### Contributing to Documentation

Edit a documentation file, e.g.,  `airflow-ctl/docs/index.rst`.

Make a small improvement:
- Fix a typo
- Improve a sentence
- Clarify wording
- Update formatting

Keep the change small and focused.

Build the documentation.

```bash
breeze build-docs apache-airflow-ctl
```

Preview the documentation locally by running `./docs/start_doc_server.sh` for a lighter resource option.

Then open:
- [http://localhost:8000](http://localhost:8000)
- Documentation list [http://localhost:8000/docs/](http://localhost:8000/docs/).

Verify your change appears correctly.

#### Contributing to Translation (UI i18n)

Another easy entry point is improving UI translations.

Read the Internationalization (i18n) policy [here](https://github.com/apache/airflow/blob/main/airflow-core/src/airflow/ui/public/i18n/README.md). This explains how translations are structured.

To check translation completeness:

```bash
breeze ui check-translation-completeness
```

To check a specific language (e.g., Thai):

```bash
breeze ui check-translation-completeness --language th
```

You can:
- Improve existing translations
- Add missing translations
- Correct unclear wording

### After Your PR Is Merged (or Before Your Next Contribution)

Keeping your fork up to date is important before starting a new branch.

#### Sync with Upstream

To fetch, rebase, and push:

```bash
git switch main
git fetch upstream
git rebase upstream/main
git push origin main
```

Your fork will be aligned with the official repository. Now you're ready to create a new branch and start your next contribution. 🚀
