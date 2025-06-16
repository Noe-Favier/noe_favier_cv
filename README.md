# Noé Favier - Curriculum Vitae

This repository contains the LaTeX source code for my CV.

## Structure

- `main.tex`: Main LaTeX file for the CV.
- `sections/`: Contains modularized parts of the CV (education, experience, skills, etc.).
- `build/`: Output directory for compiled files (ignored by git).

## Build Instructions

This project uses `latexmk` within a Docker container to ensure a consistent build environment.

### Secrets

You'll need to create `.env.tex` file from the [.env.example.tex](.env.example.tex) file and fill it with your data

### Requirements

- `docker` and `docker-compose`
- VS Code with the LaTeX Workshop extension (recommended)

### Build with VS Code

On save, the LaTeX Workshop extension will automatically build the PDF using the provided configuration. The temporary files and the resulting PDF are stored in the `build/` directory.

### Manual Build

```bash
docker-compose exec latex latexmk -pdf -interaction=nonstopmode -synctex=1 -outdir=build main.tex
```
