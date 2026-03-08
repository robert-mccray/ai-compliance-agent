# 📋 AI Compliance Agent (Governance-as-Code)

A localized AI engine that automates infrastructure compliance audits. It ingests strict regulatory documents (SOC2, Vendor SLAs) and cross-references the requirements against actual deployed Infrastructure-as-Code (Terraform) to immediately flag non-compliant architectures before they reach production.

## 🏗️ Architecture
1. **Ingestion:** Reads raw text from compliance policies and HCL (HashiCorp Configuration Language) from Terraform states.
2. **Analysis:** Prompts a local LLM to act as a rigorous IT Auditor, comparing the requested security baselines against the actual codified infrastructure.
3. **Reporting:** Outputs a markdown-formatted gap analysis detailing exact violations and the required IaC fixes.

## 🚀 How to Run Locally

### Prerequisites
1. **Ollama:** Must be running locally with the `llama3` model.
2. **Python:** 3.10+ installed.

### Execution Steps
1. Clone the repository.
2. Review the mock data in `/data/vendor_sla.txt` and `/data/main.tf` to understand the intentional compliance gap.
3. Run the Python auditing engine:
   ```bash
   python engine/auditor.py
   ```
4. Review the generated gap analysis in your terminal to see the AI flag the missing encryption blocks.


---
