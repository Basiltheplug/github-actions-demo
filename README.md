# Multi-Cloud CI Demo (Azure/GCP/AWS) — Python + GitHub Actions

This repo demonstrates a tiny Python app with full CI and multi-cloud validation.

## What’s here
- `hello.py`, `test_hello.py`: minimal app + tests  
- `Makefile`: `install`, `lint`, `test`, `all`  
- GitHub Actions:
  - `.github/workflows/python-app.yml`: install/lint/test on Python 3.10/3.11/3.12
  - `.github/workflows/cloud-validate.yml`: installs **Azure CLI**, **gcloud**, **awscli** and runs safe diagnostics (no secrets)

## How to run locally (example: Azure Cloud Shell)
```bash
git clone <your fork>
cd <repo>
python3 -m venv ~/.venv && source ~/.venv/bin/activate
make all
