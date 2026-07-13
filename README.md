# Core Data Ingestion Engine ⚙️

An automated, containerized data pipeline built in Python that extracts, validates, and flattens paginated API data for downstream analytical processing.

## 🏗️ Architecture
![Pipeline Architecture](assets/architecture.png)
*(Insert your diagram image here)*

## 🚀 Key Features
* **Automated Pagination:** Dynamically traverses API cursor limits with exponential backoff for rate limiting.
* **Defensive Schema Validation:** Verifies structural integrity of incoming JSON payloads before processing, dropping corrupt records natively.
* **Environment Security:** 100% decoupled configuration using `.env` injection.
* **Container Parity:** Fully packaged via Docker to ensure identical execution environments across local and cloud servers.
* **Persistent Storage:** Utilizes Docker Bind Mounts to securely write flattened JSON arrays to host disk storage.
* **Structured Logging:** Emits runtime states (`INFO`, `WARNING`, `ERROR`) to a persistent `pipeline.log` file.

## 💻 Prerequisites
* Docker Desktop installed and running.
* Python 3.9+ (if running locally without Docker).