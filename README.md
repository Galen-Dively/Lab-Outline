## Lab Outline Generator

### Description

This Python script automates the process of creating a lab outline document from an assignment rubric. By copying the entire rubric from Canvas into a file called `input/assignment.txt`, the script extracts the requirements linked to learning outcomes and organizes them into a well-structured document. This document is created in `.docx` format and is then opened automatically in LibreOffice for further editing.

### How It Works

1. **Input File:**  
   You start by copying the full rubric from Canvas and saving it as `input/assignment.txt`. When copying the rubric, you may notice that some criteria are only visible with the phrase *"This criterion is linked to a Learning Outcome"* appearing after the item is copied into the file. This phrase is used by the script to identify the assignment requirements.

2. **Extracting Requirements:**  
   The script reads the rubric line by line and extracts the deliverables (requirements) that follow the phrase *"This criterion is linked to a Learning Outcome"*. These deliverables are stored in a list for inclusion in the final document.

3. **Document Creation:**  
   A new `.docx` file is created with a table that has two columns: "Requirements" and "Submission". Each extracted deliverable is placed under the "Requirements" column. You can enter a title for the document, which is then saved to an `output/` folder in the current working directory.

4. **Opening the Document in LibreOffice:**  
   Once the document is generated, the script automatically opens it in LibreOffice for further editing. This allows you to review and complete the assignment directly from the generated document.



### Requirements

- **Python 3.x**  
  The script uses the `docx` library to generate `.docx` files. Make sure to install the required dependencies:
  ```bash
  pip install python-docx


* LibreOffice must be installed and available in your system's `PATH` to open the generated document automatically. There is an option once the program is running to not open in libre.
1. Install the required libraries:
'pip install python-docx'

2. Ensure LibreOffice is installed and accessible via the command line.

3. Copy the rubric into the `input/assignment.txt` file.

4. Run the script:
`python lab_outline.py`
