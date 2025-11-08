# Solar Challenge Week 1 — Task 1: Git & Environment Setup

## Setup Instructions

### Clone Repository
```bash
git clone https://github.com/chelone936/solar-challenge-week1.git
cd solar-challenge-week1
```

### Create & Activate Environment
```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

### Trigger CI/CD
Push to GitHub — check **Actions** tab to confirm  CI Pipeline passes.

## Folder Structure
```
├── .github/workflows/
│   └── ci.yml
│   └── unittests.yml
├── src/
│   └── __init__.py
├── notebooks/
│   └── __init__.py
│   └── README.md
├── tests/
│   └── __init__.py
├── scripts/
│   └── __init__.py
│   └── README.md
├── app/
├── requirements.txt
├── .gitignore
└── README.md
```

