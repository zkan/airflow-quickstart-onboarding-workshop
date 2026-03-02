# Start Contributing

In this workshop, we'll start with documentation or translation contributions.
These are the easiest and most beginner-friendly ways to get involved.

You don't need to understand Airflow internals — just improve clarity or
language support.

## Contributing to Documentation

Edit a documentation file, e.g., `airflow-ctl/docs/index.rst`.

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

Preview the documentation locally by running `./docs/start_doc_server.sh` for a
lighter resource option.

Then open:

- [http://localhost:8000](http://localhost:8000){target=_blank}
- Documentation list [http://localhost:8000/docs/](http://localhost:8000/docs/){target=_blank}

Verify your change appears correctly.

## Contributing to Translation (UI i18n)

Another easy entry point is improving UI translations.

Read the Internationalization (i18n) policy
[here](https://github.com/apache/airflow/blob/main/airflow-core/src/airflow/ui/public/i18n/README.md){target=_blank}.
This explains how translations are structured.

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
