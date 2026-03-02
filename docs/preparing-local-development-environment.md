# Preparing the Local Development Environment

## Install Docker

Ensure Docker is installed and running on your machine.

## Install mise

[mise](https://mise.jdx.dev/){target=_blank}

```bash
curl https://mise.run | sh
```

## Install Python using mise

```bash
mise use -g python@3.14.0
```

Verify:

```bash
python --version
```

## Install uv using mise

[uv](https://github.com/astral-sh/uv){target=_blank}

```bash
mise use -g uv@0.10.0
```

Verify:

```bash
uv --version
```

## Install prek

[prek](https://github.com/j178/prek){target=_blank}

```bash
uv tool install prek
```
