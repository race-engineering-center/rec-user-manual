# Race Engineering Center user manual

[![Publish docs via GitHub Pages](https://github.com/race-engineering-center/rec-user-manual/actions/workflows/docs.yml/badge.svg)](https://github.com/race-engineering-center/rec-user-manual/actions/workflows/docs.yml)

This repo contains user manual source for Race Engineering Center desktop application
suite

User manual is available
[here](https://race-engineering-center.github.io/rec-user-manual/)

## Local development

You'll need python>=3.7

- Clone this repo
- `cd` into project root folder
- Optionally create and activate venv (see
    [here](https://python.land/virtual-environments/virtualenv) for details)
- Install dependencies `pip install -r requirements.txt`
- Run `mkdocs serve` to launch a local web-server with user manual
- By default, the website with docs will run on http://127.0.0.1:8000/, follow the link
    in the terminal to open docs

## Markdown formatting

This project uses [mdformat](https://mdformat.readthedocs.io/) as the canonical Markdown
formatter with the [mdformat-mkdocs](https://github.com/KyleKing/mdformat-mkdocs) plugin
to preserve Material for MkDocs syntax.

### Using mdformat with uv

Format all Markdown files:

```bash
uv run mdformat .
```

Check formatting without making changes:

```bash
uv run mdformat --check .
```

Format specific files or directories:

```bash
uv run mdformat docs/
uv run mdformat docs/index.md
```

### Configuration

Formatting is configured in `.mdformat.toml`. Prettier is explicitly disabled for
Markdown files via `.prettierignore`.

## Working with images

In case some annotations are needed on an image, use
[excalidraw](https://excalidraw.com) to create an annotated image. Use a screenshot as a
background, save a screenshot with `_src` suffix. Export an image to png with the same
name and `_marks` suffix. Then remove an image from excalidraw and save `.excalidraw`
file without an image with the same base name as the annotated image. This way we can
make the images somewhat reproducible.
