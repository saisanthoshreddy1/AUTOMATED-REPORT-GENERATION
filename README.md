# AUTOMATED-REPORT-GENERATION

**COMPANY**: CODTECH IT SOLUTIONS

**NAME**: K.Sai Santhosh Reddy

**INTERN ID**: CT04DF611

**DOMAIN**: PYTHON

**DURATION**: 4 WEEKS (MAY 30TH,2025 TO JUNE 30TH,2025)

**MENTOR**: NEELA SANTOSH.

## 1. Libraries and Setup

The script starts by importing several essential libraries. The `csv` and `StringIO` modules are used to simulate file-like reading from a multi-line string. `StringIO` allows the string (formatted as CSV) to behave like a file object, which `csv.DictReader` can parse easily.

Next, the script uses several components from the ReportLab library. This includes `SimpleDocTemplate` for laying out the document, `Paragraph` and `Table` for content, and `Spacer` for visual spacing. Custom styles are created using `ParagraphStyle` for a polished look, and `TableStyle` is used to control table formatting such as cell padding, borders, and colors.

## **2. Reading and Parsing CSV Data**

The `read_data()` function reads the CSV string and converts each row into a dictionary using `csv.DictReader`. The result is a list of dictionaries where each dictionary represents one employee’s record. This function helps in abstracting the input, making it easy to swap in an actual CSV file or a different data source later.

## **3. Analyzing the Data**

The `analyze_data()` function processes the raw employee data and calculates important summary statistics. It keeps a running count of employees, total salary, and total years of service. Importantly, it aggregates this data by department, tracking each department's number of employees, total salaries, and total tenure years.

After gathering these values, the function computes average salary and years of service both for the entire company and per department. These calculations help in providing both macro-level and micro-level insights in the final report.

## **4. Creating the PDF Report**

The `generate_pdf_report()` function takes the parsed data and the calculated summary to build a professional PDF document. It first defines the document's layout and margins using `SimpleDocTemplate`. Three custom text styles are defined using `ParagraphStyle`: one for the title, one for section headers, and one for the body text. This ensures the report has visual hierarchy and readability.

The report starts with a title and an overall summary section, including total employee count, average salary, and average years of service. Following this, a department-wise summary table is presented. This table displays department names along with employee count, average salary, and average tenure per department.

Finally, the report includes a detailed table listing every individual employee’s name, department, salary, and years at the company. This table is styled with alternating row colors and bold headers to improve readability.

## **5. Script Execution and Output**

The final block of code checks if the script is being run directly with `if __name__ == "__main__":`. If so, it reads the data, analyzes it, and generates the PDF. The filename is set as `"sample_report.pdf"`, and a confirmation message is printed when the process is complete.

## **Conclusion**

Overall, this script demonstrates clean separation of concerns: one function handles reading, another handles analysis, and a third builds the output. It effectively uses Python’s built-in features alongside ReportLab to produce a practical report. It’s flexible enough to be extended—for example, to accept input from a real CSV file or to visualize the results with charts. This kind of script is useful in HR, finance, or project reporting systems where data must be analyzed and presented clearly.

## **OUTPUT**

![Image](https://github.com/user-attachments/assets/1a1c8483-06e0-4121-a78f-f46ab927a607)


