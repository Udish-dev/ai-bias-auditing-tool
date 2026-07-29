# AI Bias Auditing Tool

An interactive AI Bias Auditing Tool built using **Python, Pandas, Fairlearn, Matplotlib, and Google Colab**. This project helps identify potential bias in datasets by comparing outcome rates across demographic groups and generating fairness metrics, visualizations, and audit reports.

## Features

- Upload any CSV dataset
- Select a sensitive attribute using dropdown menus
- Select an outcome column dynamically
- Calculate approval rates for different groups
- Measure fairness using Fairlearn
- Generate visual charts automatically
- Produce a bias audit report
- Beginner-friendly and fully runnable in Google Colab

## Technologies Used

- Python
- Pandas
- Fairlearn
- Matplotlib
- ipywidgets
- Google Colab

---

## Project Workflow

```text
Upload Dataset
      ↓
Select Sensitive Attribute
      ↓
Select Outcome Column
      ↓
Run Bias Audit
      ↓
Generate Fairness Metrics
      ↓
Create Visualizations
      ↓
Produce Audit Report
```

---

## Installation

Install the required libraries in Google Colab:

```python
!pip install fairlearn ipywidgets
```

---

## Usage

### Step 1: Upload Dataset

Upload any CSV file containing:

- A sensitive attribute (Gender, Age, Race, etc.)
- An outcome column (Approved/Rejected, Good/Bad, Yes/No)

Example:

| Gender | Loan_Approved |
|----------|----------|
| Male | Yes |
| Female | No |
| Male | Yes |

---

### Step 2: Select Columns

Using the dropdown menus:

- Select the sensitive attribute column
- Select the outcome column

Example:

```text
Sensitive Attribute: Gender
Outcome Column: Loan_Approved
```

---

### Step 3: Run Bias Audit

The tool automatically:

- Converts outcomes into binary values
- Calculates approval rates
- Computes Demographic Parity Difference
- Generates charts
- Produces a bias assessment report

---

## Fairness Metric

### Demographic Parity Difference

Measures whether different demographic groups receive positive outcomes at different rates.

Formula:

```text
Highest Group Approval Rate
-
Lowest Group Approval Rate
```

### Interpretation

| Score | Meaning |
|---------|---------|
| 0.00 | Perfect parity |
| < 0.05 | Low disparity |
| 0.05 – 0.10 | Moderate disparity |
| > 0.10 | Significant disparity |

---

## Example Output

```text
Approval Rates

Female    0.75
Male      0.69

Demographic Parity Difference: 0.06

Assessment:
Moderate disparity detected.
```

---

## Visualizations

### Approval Rate by Group

Displays approval rates for each demographic group.

### Outcome Distribution by Group

Displays counts of positive and negative outcomes across groups.

---

## Example Dataset

This project was tested using the German Credit Dataset.

Relevant columns:

```text
status_and_sex
target
```

Where:

- `status_and_sex` → Sensitive Attribute
- `target` → Outcome Column
- `good` → Positive Outcome
- `bad` → Negative Outcome

---

## Repository Structure

```text
AI-Bias-Auditing-Tool/
│
├── README.md
├── bias_audit_colab.ipynb
├── requirements.txt
├── sample_data/
│   └── german_credit_data.csv
├── screenshots/
│   ├── approval_rate_chart.png
│   ├── outcome_distribution_chart.png
│   └── audit_report.png
└── LICENSE
```

---

## Future Improvements

- Additional Fairlearn fairness metrics
- PDF report generation
- Streamlit web application
- Bias mitigation recommendations
- Machine learning model auditing
- Real-time fairness dashboard

---

## Learning Outcomes

This project demonstrates:

- Responsible AI principles
- Fairness and bias analysis
- Data preprocessing with Pandas
- Interactive user interfaces with widgets
- Data visualization with Matplotlib
- Fairness measurement using Fairlearn

---

## Author

**Ben Designer**

College Freshman Project – AI Bias Auditing Tool using Python and Fairlearn.

---

## License

This project is licensed under the MIT License.

Feel free to use, modify, and improve it for educational and research purposes.
