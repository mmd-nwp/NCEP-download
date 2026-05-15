### 3. `ARCHITECTURE.md` (The System Map)
*Place this in the root directory.*

```markdown
# System Architecture

This document maps out how data flows from raw input to the end-user web application.

## 🗺️ High-Level Data Flow

1. **Data Ingestion:** Python scripts (`/backend/ingest.py`) fetch raw data from [Source].
2. **Heavy Computation:** Python passes arrays to the compiled Fortran module (`/backend/compute.f90`) via `f2py` for high-performance number crunching.
3. **Storage:** Processed results are written to the [Database Type, e.g., PostgreSQL] database.
4. **Web Frontend:** The user accesses the website. The [Web Framework, e.g., Flask/Django/React] backend queries the database and serves the visual results to the user.

## 🗄️ Database Schema Overview
* **Table: `users`** - Tracks organizational logins.
* **Table: `processed_data`** - [Description of what this holds]
* **Table: `reports`** - [Description of what this holds]

*(Note: Keep this updated if tables are added or dropped!)*
