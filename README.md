# Data Syndication & Validation Projects

This repository contains two Python projects designed to demonstrate core skills required for a Junior Data Analyst role, specifically focusing on the challenges of product information management (PIM) and data syndication. These projects showcase data mapping, transformation, validation, and the creation of automated data-processing pipelines.

---

## 🚀 Project 1: eCommerce Product Data Syndication Pipeline (`project1.py`)

This project simulates the process of taking clean product data from a central source (`pim_products.csv`) and syndicating it to a fictional eCommerce retailer, "ElectroWorld," which requires data in a specific JSON format.

### Key Features:
* **Data Mapping:** Maps internal field names (`product_id`, `category`) to retailer-specific names (`sku`, `category_id`).
* **Data Transformation:** Converts human-readable category strings (e.g., "Electronics") into required numeric IDs (e.g., 501).
* **Validation:** Includes a basic check to skip products with unrecognized categories, preventing bad data from being sent.
* **Output:** Generates a compliant `electroworld_feed.json` file ready for API submission.


## ⚙️ Project 2: Config-Driven Data Validation Engine (`project2.py`)

This is a more advanced and scalable engine that processes a "messy" customer data file (`customer_data.csv`) against a set of rules defined in an external configuration file (`retailer_A_config.yaml`). This demonstrates the ability to handle data quality issues proactively.

### Key Features:
* **External Configuration:** All mapping, transformation, and validation rules are defined in a YAML file, making the engine adaptable to new retailer requirements without changing the code.
* **Robust Validation:** Checks for common data issues like negative prices, empty required fields, and inconsistent formatting.
* **Dual-File Output:**
    * `syndication_ready.csv`: Contains only the records that passed all validation checks, correctly transformed.
    * `validation_errors.log`: A detailed report of all records that failed, specifying which rule was broken and why. This simulates a real-world issue resolution workflow.


## 🛠️ Technical Skills Demonstrated
* **Data Analysis & Manipulation:** Python (Pandas)
* **Data Mapping & Transformation**
* **Data Validation & Cleansing**
* **System Integration Concepts:** Simulating data flow from a PIM to a retailer.
* **File I/O:** Reading from CSV/YAML and writing to JSON/CSV/Log files.
* **Problem-Solving:** Proactively identifying and flagging data quality issues.
