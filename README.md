# Regex Project

## Overview
This project demonstrates the application of Regular Expressions (Regex) in Python to solve text processing and pattern-matching problems. It is implemented in a Jupyter Notebook (`regex_project.ipynb`) and covers multiple real-world use cases where regex can simplify and automate text extraction tasks.

## Features

### Key Use Cases
1. **Extracting Phone Numbers**:
   - Extracts both 10-digit phone numbers and formatted numbers like `(XXX)-XXX-XXXX`.
   - Regex Pattern: `\d{10}|\(\d{3}\)-\d{3}-\d{4}`

2. **Identifying Twitter Handles**:
   - Extracts Twitter handles from URLs in a given text.
   - Regex Pattern: `https:\/\/twitter\.com\/([^,\n]+)`

3. **Finding Text After Specific Keywords**:
   - Identifies and captures text following a phrase, such as "Concentration of Risk:".
   - Regex Pattern: `Concentration of Risk: ([^\n]*)`

4. **Extracting Fiscal Year Data**:
   - Captures fiscal year information, including quarters and semesters.
   - Regex Pattern: `FY(\d{4} (?:Q[1-4]|S[1-2]))`

### Highlights of Regex Concepts
- Capturing groups: Extract specific parts of a match.
- Non-capturing groups: Use `(?:...)` to group expressions without creating separate capturing groups.
- Quantifiers: Apply `+`, `*`, and `{min,max}` for flexible pattern matching.
- Escaping: Use `\` to escape special characters.

### Implementation Details
The notebook provides:
- Clear examples for each regex pattern.
- Explanations of the patterns and their components.
- Outputs demonstrating successful text extraction.

## Prerequisites
- Python
- `re` module (built into Python)
- Jupyter Notebook

## How to Use
1. Clone this repository or download the `regex_project.ipynb` file.
2. Open the notebook using Jupyter Notebook or JupyterLab.
3. Run each cell to see the regex in action.
4. Modify the input text or regex patterns to test different scenarios.

## Learning Objectives
- Understand the power of regex in text processing.
- Learn to construct and use regex patterns effectively.
- Apply regex to solve real-world problems involving text extraction and analysis.

## Example:
### Extracting the Phone Numbers
```python
import re

text_one = """
Elon Musk's phone number is 9998882221. If you have any questions please directly contact him. Tesla's annual revenue is 100 Billion dollars.
Tesla's CFO number is (989)-450-7694
"""

pattern_one = '\\d{10}|\\(\\d{3}\\)-\\d{3}-\\d{4}'

matches = re.findall(pattern_one, text_one)
print(matches)
```

### Output:
```
['9998882221', '(989)-450-7694']
```