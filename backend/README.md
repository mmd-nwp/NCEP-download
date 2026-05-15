# Backend & Data Pipeline Documentation

This directory contains the Python scripts and Fortran source code responsible for processing the data before it reaches the database and web frontend.

## ⚙️ Environment Setup
To get this running on a local machine, you will need:
* **Python:** version [e.g., 3.10+]
* **Fortran Compiler:** [e.g., gfortran]
* **Database:** [e.g., PostgreSQL 14]

### 1. Install Dependencies
```bash
# Example commands
pip install -r requirements.txt

# Example command to compile Fortran via f2py or makefile
f2py -c -m my_fortran_module source.f90

# Database setup.
python db_setup.py
