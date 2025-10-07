# Macheo Report Generator

This script automates how we pull and compile reports from Monday.com.
It grabs Word files and images from each intervention board, fills them into a report template, and emails the finished report automatically. No more manual copy-pasting.

---

## How It Works

* Connects to Monday.com using your API key.
* Finds the latest task ending with “Report-M & E Experiment.”
* Downloads any attached Word docs or images.
* Combines everything into a clean `.docx` file.
* Sends the report through Gmail.

---

## Setup

1. Install dependencies:

   ```bash
   pip install requests python-docx
   ```
2. Update your details in the script:

   ```python
   SENDER_EMAIL = "macheoreports@macheo.org"
   RECIPIENT_EMAIL = "macheoreports@macheo.org"
   API_KEY = "your_monday_api_key"
   ```
3. Run `AUTOMATEDDONORWORKFLOW.ipynb` in Jupyter Notebook.

---

## Output

The script creates and emails a Word report like:

```
Report_<BoardName>_Task_<TaskID>_<Date>.docx
```

---

**Author:** Damaris Wanjiru Chege
**Org:** Macheo Children Organisation
**Email:** [damarischege47@gmail.com](mailto:damarischege47@gmail.com)
