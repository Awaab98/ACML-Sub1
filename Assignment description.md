# Assignment Description

## Project Setup

### 1. Project Documentation
- Created `Assignment description.md` file to document the project setup and implementation details

### 2. Virtual Environment Setup
- Created a Python virtual environment using `python -m venv venv`
- Virtual environment directory: `venv/`
- To activate the virtual environment:
  - Windows: `venv\Scripts\activate`
  - Linux/Mac: `source venv/bin/activate`

### 3. Dependencies Management
- Created `requirements.txt` file to track Python dependencies
- This file will be used for installing required libraries in the future
- Install dependencies using: `pip install -r requirements.txt`

### 4. Git Repository Setup
- Initialized a Git repository using `git init`
- Created `.gitignore` file to exclude unnecessary files from version control
- The `.gitignore` includes:
  - Virtual environment folders (`venv/`, `.venv/`, etc.)
  - Python cache files (`__pycache__/`, `*.pyc`)
  - IDE configuration folders (`.vscode/`, `.idea/`)
  - Distribution and build files
  - OS-specific files (`.DS_Store`, `Thumbs.db`)

