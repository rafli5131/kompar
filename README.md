# Weather Collection with Python Threads — Yogyakarta

A coursework project that collects current weather observations for districts (kecamatan) in the Special Region of Yogyakarta and writes the results to an Excel workbook.

## What it demonstrates

- Using Python `threading.Thread` to request multiple locations.
- Fetching structured weather data from WeatherAPI over HTTPS.
- Reading and updating spreadsheets with `openpyxl`.
- Handling request failures without losing the rest of the dataset.

## Setup

Requires Python 3, `requests`, `openpyxl`, and a WeatherAPI API key.

```bash
git clone https://github.com/rafli5131/kompar.git
cd kompar/project-1
python -m pip install requests openpyxl
```

Set the API key as a **local environment variable**, never hard-code it or commit it:

**Linux/macOS:**

```bash
export WEATHER_API_KEY="your-new-key"
python cuaca_multithread.py
```

**PowerShell:**

```powershell
$env:WEATHER_API_KEY = "your-new-key"
python .\cuaca_multithread.py
```

The script reads `DIY.xlsx` (district names in the first column) and writes weather results to columns B–H **in the same file**. Back up the workbook before running if you need to preserve original data.

## Structure

- [`project-1/cuaca_multithread.py`](project-1/cuaca_multithread.py) — concurrent data collection.
- [`project-1/DIY.xlsx`](project-1/DIY.xlsx) — input/output workbook.
- [`project-1/README.md`](project-1/README.md) — original coursework context.

## Security and limitations

A former WeatherAPI key was accidentally included in earlier revisions of this repository. It has been removed from the current source, but **must be revoked or rotated at WeatherAPI** because historical Git commits remain accessible. This code is a teaching example and does not implement API rate limiting or automated integration tests.

The original coursework credits its collaborators in the project README.
