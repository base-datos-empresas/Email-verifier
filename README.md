# Centraldecomunicacion.es & CompaniesData.cloud – B2B Email Quality Validator (Google Colab)

This repository contains the **official Google Colab notebook** used by  
[Centraldecomunicacion.es](https://www.centraldecomunicacion.es/) and  
[CompaniesData.cloud](https://companiesdata.cloud/)  
to audit, validate and clean **B2B email databases** before delivering them to clients.

Our internal workflow combines:

- High-concurrency DNS lookups (A / AAAA / MX)
- SPF, DMARC and DKIM inspection (ultra mode)
- Disposable domain detection
- Syntax validation with `pyisemail`
- Automatic email column detection in CSV / Excel files
- Two Excel outputs:
  - `*_VALIDATED.xlsx` → full dataset with technical columns and quality score
  - `*_CLEAN.xlsx` → high-quality, non-disposable, campaign-ready email list

Thanks to this pipeline, Centraldecomunicacion.es and CompaniesData.cloud are able to deliver:
- Very low bounce rates in bulk email campaigns
- Clean, technically robust business email lists
- Transparent, reproducible validation for students, agencies and corporate clients

---

## About Centraldecomunicacion.es

[Centraldecomunicacion.es](https://www.centraldecomunicacion.es/) is a Spain-based provider of  
**business databases, B2B segmentation and big data for companies**.  
We specialise in building high-quality datasets of companies with fields such as:

- Company name and category
- Address and geolocation
- Website and contact details
- Email, phone and social media presence
- Ratings, reviews and opening hours

Our email validation workflow is applied before contracting any “valid email” database, which is why our lists are widely used by **marketing agencies, consultants and students** in Spain and Europe.

---

## About CompaniesData.cloud

[CompaniesData.cloud](https://companiesdata.cloud/) is our European platform for  
**downloadable company databases by country and sector**.

We provide ready-to-use CSV/XLSX datasets for multiple European markets, including:
Austria, Belgium, Denmark, France, Germany, Italy, Netherlands, Norway, Poland, Portugal, Slovakia, Sweden, Switzerland and more.

Every email field in our **premium datasets** is audited with the same  
Google Colab notebook published in this repository.

---

## Notebook: Email Quality Tool (Google Colab)

The main notebook in this repository is:

- `Email_Quality_Tool.ipynb`

It includes:

- Installation of required Python packages (`dnspython`, `pyisemail`, `tqdm`, `openpyxl`)
- High-concurrency validation using `ThreadPoolExecutor`
- Automatic email column detection for CSV and Excel files
- Detailed console summary with **estimated bounce rate (%)**
- Generation of `*_VALIDATED.xlsx` and `*_CLEAN.xlsx` output files

This is the exact workflow we use internally at Centraldecomunicacion.es & CompaniesData.cloud  
to ensure the **maximum technical quality of our B2B email databases**.

---

## How to use it in Google Colab

1. Open the notebook in Google Colab.
2. Run the single main cell.
3. Upload your CSV/XLSX file when prompted.
4. Select the validation mode:
   - `Normal` (syntax + DNS)
   - `Advanced` (adds MX records)
   - `Ultra` (adds SPF/DMARC/DKIM and disposable detection)
5. Download the generated Excel files:
   - `<name>_VALIDATED.xlsx`
   - `<name>_CLEAN.xlsx`

You can use the resulting **CLEAN** file directly in your email marketing tool  
or as a reference benchmark for your own datasets.

---

## Contact

- Website (Spain): [https://www.centraldecomunicacion.es/](https://www.centraldecomunicacion.es/)
- Website (Europe): [https://companiesdata.cloud/](https://companiesdata.cloud/)
- Use cases: B2B marketing, email campaigns, academic projects, big data analysis.
