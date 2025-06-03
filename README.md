# Project Description

## Qualtrics Survey Importer

The **Qualtrics Survey Importer** is a Python-based tool designed to streamline the process of importing survey questions from Excel sheets into the Qualtrics survey software. This project aims to facilitate researchers and survey creators by automating the conversion of survey drafts stored in Excel format into a format compatible with Qualtrics, thus saving time and reducing manual errors.

### Features
- **Excel Import**: The tool reads survey questions from an Excel file to a Pandas Dataframe, allowing users to structure their surveys in a familiar format.
- **Qualtrics Format Export**: Generates a text file in the Qualtrics advanced format, ready for import into the Qualtrics platform.
- **Customizable**: Users can modify the Excel template to fit their specific survey needs, including various question types and response formats.

## Getting Started

### Prerequisites
- Python 3.x
- Pandas library
- Access to Qualtrics account for importing surveys


### Usage
1. Prepare your Excel file with the survey questions. Ensure it follows the specified format with the necessary columns (e.g., Sections, Labels, Question Type, Survey Question, Choices).
2. Update the `excel_path` and `output_path` variables in the script to point to your Excel file and desired output file location.


### Example Code
```python
# Import the survey draft
excel_path = "2025-05-28 SurveyDraft.xlsx"
sheet_name = "Survey Questions"
output_path = "qualtrics_import.txt"

# Step 1: Import the survey
df = import_survey(excel_path, sheet_name)

# Step 2: Write the Qualtrics TXT file
write_qualtrics_file(df, output_path)
```
