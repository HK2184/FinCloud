# **FinCloud ☁️**
 **FinCloud** is a Python-based system designed to process and analyze financial documents such as salary slips, utility bills, bank statements, and more. It leverages OCR, natural language processing (NLP), and structured data extraction to provide insights and generate reports dynamically.

---

## **Table of Contents**

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [How to Use](#how-to-use)
- [Folder Structure](#folder-structure)
- [Sample Flow](#sample-flow)
- [Future Enhancements](#future-enhancements)
- [License](#license)

---

## **Features**

- **OCR (Optical Character Recognition):**
  - Extracts structured and unstructured data from scanned images (e.g., salary slips, invoices).
  
- **Document Preprocessing:**
  - Image deskewing, noise removal, adaptive thresholding for better OCR accuracy.
  
- **Financial Insights:**
  - Extracts key metrics such as earnings, deductions, and net salary.
  - Classifies expenses into categories like utilities, transportation, etc.

- **Multi-Document Support:**
  - Processes salary slips, bank statements, utility bills, Form 16, and more.

- **Accuracy Analysis:**
  - Calculates field extraction rates and internal consistency.

- **Data Storage and Visualization:**
  - Saves extracted data in structured formats (CSV/JSON) for seamless integration with analytics tools like Power BI.

---

## **Technologies Used**

- Programming Language: **Python**
- Libraries:
  - **pytesseract**: For OCR functionality.
  - **OpenCV**: For image preprocessing and enhancement.
  - **spacy**: For NLP and text analysis.
  - **pandas**: For data manipulation and storage.
  - **matplotlib**: For visualizing trends and extracting insights.
  - **re and dateutil**: For regex-based parsing and date handling.

---

## **Installation**

1. Clone the repository:
   ```bash
   git clone https://github.com/your_username/financial-document-intelligence.git
   cd financial-document-intelligence
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Ensure **Tesseract OCR** is installed:
   - Download and install Tesseract OCR from [here](https://github.com/tesseract-ocr/tesseract).
   - Update the `pytesseract.pytesseract.tesseract_cmd` variable in the code with the correct path on your system.

4. Download the English NLP model:
   ```bash
   python -m spacy download en_core_web_sm
   ```

---
## Dataset
-https://www.kaggle.com/datasets/mehaksingal/personal-financial-dataset-for-india
## **How to Use**


1. **Predefine Document Folders**
   - Organize your financial documents in folders corresponding to their types (e.g., salary slips, utility bills, etc.). Update the `document_paths` variable in the code with the folder paths.

2. **Run the Main Script**
   - Use the following command to process documents:
     ```bash
     python main.py
     ```

3. **View Extracted Insights**
   - After successful execution, all extracted data will be saved in the `processed_results` folder in CSV and JSON formats.

4. **Analyze with Power BI**
   - To import the data into Power BI:
     1. Open Power BI Desktop.
     2. Select `Get Data > Text/CSV`.
     3. Choose the `processed_results/extracted_data.csv` file.
     4. Build visualizations using the imported data.

---

## **Folder Structure**

```plaintext
financial-document-intelligence/
├── README.md            # Documentation
├── requirements.txt     # Dependencies
├── main.py              # Main processing script
├── salary_slip_processor.py # Salary slip-specific logic
├── processed_results/   # Output directory for results
├── uploaded_files/      # Temporary file storage
├── utils/               # Utility functions and reusable components
└── tests/               # Unit tests for document processing
```

---

## **Sample Flow**

1. **Input:**
   - Upload a sample salary slip or utility bill (e.g., `salary_slip.jpg`).

2. **Processing:**
   - The system extracts text using OCR and parses key information (e.g., company name, salary amounts, deductions).

3. **Output:**
   - Saves structured data in a CSV file:
     ```csv
     file_name,document_type,company_name,employee_name,period,total_amount,processed_date
     salary_slip.jpg,Salary Slip,TechCorp,John Doe,March 2025,65000,2025-04-12
     ```

4. **Analytics:**
   - Visualize spending patterns and financial summaries in analytics tools.

---

## **Sample Image**

-<img src="https://github.com/user-attachments/assets/7ab62621-faac-4580-8dd5-56f0acf53c01" width="500" height="600">

-<img src="https://github.com/user-attachments/assets/d3ab7c79-3e4c-44e1-b2f5-d6656f8f385c" width="500" height="500">

---

## **Future Enhancements**

- Add support for more document types like purchase receipts and tax forms.
- Improve OCR accuracy using advanced models like Google Vision or AWS Textract.
- Add a web-based GUI for file uploads and analytics.
- Automate recurring document ingestion using cloud services.

---

## **License**

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for more details.

---

Feel free to customize the README to fit your project’s specific requirements! Let me know if you'd like me to assist in automating README generation or adjusting content.

Citations:
[1] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/62789894/1bb44bf1-6a95-4dd5-9aeb-28d91b9b8e3b/paste-1.txt


