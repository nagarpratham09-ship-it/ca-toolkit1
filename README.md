
"# CA Toolkit — GST Reconciliation

Professional CA-grade GST Reconciliation tool built with Streamlit.

## Features

- **Dashboard** — Client overview, urgent deadlines, overdue tracking
- **GST Tool** — Upload Purchase Register & GSTR-2B Excel files, reconcile with blank row fix
- **Clients** — Add, edit, delete, search, filter, export CSV

## Fix Applied

Blank Excel rows no longer create false \"Missing in 2B\" records. The `clean_gst_dataframe()` function filters out None/NaN/empty rows before key creation.

## How to Run Locally

```bash
pip install -r requirements.txt
streamlit run app.py
```

## Deploy on Streamlit Cloud

1. Push this folder to GitHub
2. Go to [share.streamlit.io](https://share.streamlit.io)
3. Connect your GitHub repo
4. Set main file path: `app.py`
5. Click Deploy

## File Structure

```
streamlit_ca_toolkit/
├── app.py               # Main Streamlit application
├── requirements.txt     # Python dependencies
├── README.md            # This file
└── clients_data.xlsx    # Auto-created on first run
```

## Excel Format Required

Both Purchase Register and GSTR-2B files must have these columns:

| GSTIN | Invoice No | Amount |
|-------|-----------|--------|
| 27AABCU9603R1ZM | INV001 | 10000 |
| 29AABCT1332L1ZG | INV002 | 20000 |
"
