# 🗂️ Meeting Notes Optimization Pipeline

This project automates the process of cleaning and uploading meeting notes into **Google BigQuery**. It is designed for teams that want to centralize and analyze their meeting summaries using scalable cloud-based infrastructure.

---

## ⚙️ Features

- Load and inspect raw meeting notes data
- Clean and standardize text and structure
- Add metadata like source, timestamp, and tags
- Upload the optimized data to BigQuery

---

## 🚀 How to Use

### 1. Install Dependencies

Use the following command to install required Python packages:

```bash
pip install -r requirements.txt
```

---

### 2. Add Your Google Cloud Credentials

- Create a service account key in Google Cloud IAM
- Download the `.json` key file and rename it to `credentials.json`
- Place it in the root of this repository

---

### 3. Run the Notebook

Open `notebook.ipynb` and run all the cells. Make sure to:

- Modify the `project_id`, `dataset_id`, and `table_name` variables if needed
- Confirm that the dataframe is correctly loaded and cleaned
- The data will then be uploaded to your BigQuery table

```python
from google.oauth2 import service_account
from google.cloud import bigquery

credentials = service_account.Credentials.from_service_account_file("credentials.json")
client = bigquery.Client(credentials=credentials, project=credentials.project_id)

table_id = f"{project_id}.{dataset_id}.{table_name}"
job = client.load_table_from_dataframe(df_cleaned, table_id)
job.result()
```

---

## 📁 Output

Your cleaned meeting notes will be available in Google BigQuery, ready for querying or dashboarding.

---

## 📩 Contact

For questions or collaboration, feel free to reach out!

