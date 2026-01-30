---
name: office-docs
description: Process Microsoft Office documents (Excel, PowerPoint) and PDFs. Use when user asks to read, create, edit, analyze, or convert Excel spreadsheets (.xlsx), PowerPoint presentations (.pptx), or PDF files (.pdf). Also use for data extraction, report generation, and document automation tasks.
---

# Office Document Processing Skill

## Environment Setup

Always activate the virtual environment before running Python code:

```bash
source ~/.claude-office-venv/bin/activate
```

## Excel Files (.xlsx)

### Read Excel file
```python
import pandas as pd

# Read entire file
df = pd.read_excel("file.xlsx")

# Read specific sheet
df = pd.read_excel("file.xlsx", sheet_name="Sheet1")

# Read all sheets
all_sheets = pd.read_excel("file.xlsx", sheet_name=None)  # Returns dict
```

### Write Excel file
```python
import pandas as pd

# Write DataFrame to Excel
df.to_excel("output.xlsx", index=False)

# Write multiple sheets
with pd.ExcelWriter("output.xlsx", engine="openpyxl") as writer:
    df1.to_excel(writer, sheet_name="Data", index=False)
    df2.to_excel(writer, sheet_name="Summary", index=False)
```

### Advanced Excel with openpyxl
```python
from openpyxl import Workbook, load_workbook
from openpyxl.styles import Font, Fill, Alignment, PatternFill
from openpyxl.chart import BarChart, Reference

# Load existing workbook
wb = load_workbook("file.xlsx")
ws = wb.active

# Create new workbook
wb = Workbook()
ws = wb.active
ws.title = "My Sheet"

# Write data
ws["A1"] = "Header"
ws["A1"].font = Font(bold=True)
ws.append(["Col1", "Col2", "Col3"])  # Add row

# Add chart
chart = BarChart()
data = Reference(ws, min_col=2, min_row=1, max_col=3, max_row=10)
chart.add_data(data, titles_from_data=True)
ws.add_chart(chart, "E2")

wb.save("output.xlsx")
```

## PowerPoint Files (.pptx)

### Read PowerPoint
```python
from pptx import Presentation

prs = Presentation("file.pptx")

for slide_num, slide in enumerate(prs.slides, 1):
    print(f"--- Slide {slide_num} ---")
    for shape in slide.shapes:
        if shape.has_text_frame:
            for paragraph in shape.text_frame.paragraphs:
                print(paragraph.text)
```

### Create PowerPoint
```python
from pptx import Presentation
from pptx.util import Inches, Pt
from pptx.enum.text import PP_ALIGN

prs = Presentation()

# Add title slide
slide_layout = prs.slide_layouts[0]  # Title slide layout
slide = prs.slides.add_slide(slide_layout)
title = slide.shapes.title
subtitle = slide.placeholders[1]
title.text = "Presentation Title"
subtitle.text = "Subtitle here"

# Add content slide
slide_layout = prs.slide_layouts[1]  # Title and content layout
slide = prs.slides.add_slide(slide_layout)
title = slide.shapes.title
title.text = "Slide Title"
body = slide.placeholders[1]
tf = body.text_frame
tf.text = "First bullet point"
p = tf.add_paragraph()
p.text = "Second bullet point"
p.level = 0

# Add image
slide.shapes.add_picture("image.png", Inches(1), Inches(2), width=Inches(4))

prs.save("output.pptx")
```

### Add table to PowerPoint
```python
from pptx import Presentation
from pptx.util import Inches

prs = Presentation()
slide = prs.slides.add_slide(prs.slide_layouts[5])  # Blank slide

rows, cols = 4, 3
table = slide.shapes.add_table(rows, cols, Inches(1), Inches(1.5), Inches(8), Inches(3)).table

# Set header row
table.cell(0, 0).text = "Name"
table.cell(0, 1).text = "Value"
table.cell(0, 2).text = "Status"

# Fill data
data = [["Item 1", "100", "Active"], ["Item 2", "200", "Pending"], ["Item 3", "300", "Complete"]]
for i, row_data in enumerate(data, 1):
    for j, cell_data in enumerate(row_data):
        table.cell(i, j).text = cell_data

prs.save("output.pptx")
```

## PDF Files (.pdf)

### Extract text from PDF
```python
import pdfplumber

with pdfplumber.open("file.pdf") as pdf:
    # Extract from all pages
    full_text = ""
    for page in pdf.pages:
        full_text += page.extract_text() or ""

    # Extract from specific page
    first_page_text = pdf.pages[0].extract_text()
```

### Extract tables from PDF
```python
import pdfplumber
import pandas as pd

with pdfplumber.open("file.pdf") as pdf:
    for page in pdf.pages:
        tables = page.extract_tables()
        for table in tables:
            df = pd.DataFrame(table[1:], columns=table[0])
            print(df)
```

### Get PDF metadata
```python
import pdfplumber

with pdfplumber.open("file.pdf") as pdf:
    print(f"Pages: {len(pdf.pages)}")
    print(f"Metadata: {pdf.metadata}")

    # Page dimensions
    page = pdf.pages[0]
    print(f"Width: {page.width}, Height: {page.height}")
```

## Common Data Analysis Patterns

### Excel to DataFrame analysis
```python
import pandas as pd

df = pd.read_excel("data.xlsx")

# Quick analysis
print(df.describe())
print(df.info())

# Filter and aggregate
summary = df.groupby("Category")["Amount"].sum()

# Export results
summary.to_excel("summary.xlsx")
```

### PDF table to Excel conversion
```python
import pdfplumber
import pandas as pd

all_tables = []
with pdfplumber.open("report.pdf") as pdf:
    for page in pdf.pages:
        tables = page.extract_tables()
        for table in tables:
            if table:
                df = pd.DataFrame(table[1:], columns=table[0])
                all_tables.append(df)

# Combine and save
if all_tables:
    combined = pd.concat(all_tables, ignore_index=True)
    combined.to_excel("extracted_tables.xlsx", index=False)
```

### Data to PowerPoint report
```python
import pandas as pd
from pptx import Presentation
from pptx.util import Inches

# Load data
df = pd.read_excel("data.xlsx")

# Create presentation
prs = Presentation()

# Title slide
slide = prs.slides.add_slide(prs.slide_layouts[0])
slide.shapes.title.text = "Data Report"
slide.placeholders[1].text = f"Generated from {len(df)} records"

# Summary slide with key metrics
slide = prs.slides.add_slide(prs.slide_layouts[1])
slide.shapes.title.text = "Key Metrics"
body = slide.placeholders[1].text_frame
body.text = f"Total Records: {len(df)}"
body.add_paragraph().text = f"Total Amount: ${df['Amount'].sum():,.2f}"

prs.save("report.pptx")
```

## Tips

1. **Always activate the venv first**: `source ~/.claude-office-venv/bin/activate`
2. **Use pandas for data manipulation**: It integrates well with openpyxl
3. **Handle missing data**: Use `df.fillna()` or `df.dropna()` before processing
4. **Large files**: Use `chunksize` parameter in `pd.read_excel()` for memory efficiency
5. **PDF quality**: pdfplumber works best with text-based PDFs, not scanned images
