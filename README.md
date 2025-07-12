✅ README_Variant_Comparison_Tool.md
markdown
Copy
Edit
# 🧩 Variant Comparison Tool

## 📌 Purpose
This tool allows you to visually compare JSON variant metadata across multiple delivery configurations like `dazn-latin`, `global`, etc. It highlights differences in keys and values between different sources (e.g., DCA, DCB, DCC, DCD) for a given `OverRideID`.

## 📂 Input Format (CSV)

- The CSV must contain the following headers:
  - `OverRideID` (unique row identifier)
  - `DCA`, `DCB`, `DCC`, `DCD` — each cell contains a JSON string.

### 🧾 Sample Row
```csv
OverRideID,DCA,DCB,DCC,DCD
12345,"{""dazn-latin"":{""M"":{""streamId"":{""S"":""1vtud8pdzcdye1ay1yci35fatp""},""languages"":{""L"":[{""S"":""EnglishSingle""}]},""outletApiId"":{""S"":""1t1c484upiyok1nr8dkwfpt1rp""}}},""global"":{""M"":{""languages"":{""L"":[{""S"":""EnglishSingle""}]},""closedCaptions"":{""L"":[]}}}}",...
⚙️ Features
Visual JSON comparison across DCA, DCB, DCC, and DCD

Highlights:

✅ Green if values match DCA

❌ Red if values differ

JSON is automatically expanded

Toggle between dark/light theme

Search support across entire JSON and OverRideID

Highlighted matching text during search

Expand/collapse all JSONs

Supports both CSV upload and JSON paste

🔍 Search Behavior
Case-insensitive

Highlights only matched text

Automatically expands matching sections

💾 Output
Can download the entire comparison table as comparison.xlsx (Excel)

🧠 Tips
If any JSON structure is invalid, it will display Invalid JSON

All JSON values are expected to be valid DynamoDB JSON (Amazon format) or well-formatted key-value objects
