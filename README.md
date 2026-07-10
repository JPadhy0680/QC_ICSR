# XML_R3 Comparator - Permanent MedDRA Version

This package loads the MedDRA master file permanently from the repository `data/` folder instead of asking users to upload it each time.

## Required repository structure

```text
app.py
requirements.txt
data/
  MedDRA.xlsx
```

`MedDRA.csv` and `MedDRA.xlsm` are also supported, but `MedDRA.xlsx` is recommended.

## What changed

- Source XML upload remains available.
- Processed XML upload remains available.
- MedDRA upload has been removed.
- The app automatically loads `data/MedDRA.xlsx`, `data/MedDRA.xlsm`, or `data/MedDRA.csv`.
- Cache refresh uses file modified time and file size, so updated MedDRA files reload after redeploy/reboot.

## Deployment note

After pushing or replacing `data/MedDRA.xlsx` in GitHub, reboot or redeploy the Streamlit app.
