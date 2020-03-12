# Jupyter Notebook with Google Sheets

A Jupyter notebook that connects to Google Sheets.
I've initially developed this to be used for work - displaying generated SVG images for survey results. I used this as a way to remove identifiable emails and restrict other colleagues from accessing the actual data source.  I've removed all sensitive data and copied over most of the code so that the process is documented.

## Maintainer

### Run notebook

```shell
source venv/bin/activate
pip install -r requirements.txt
jupyter notebook
```

Running the notebook will recreate `images` folder completely and create a new `email_hash.json` file, which will show who has which hash for this generation.

### Ignored files

- `key/service_acccount_GS.json`: key to authenticate to Google Sheets
- `email_hash.json`: Email to ID file

## Requirements

- [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/running.html): Running IPython notebooks
- Orca: Image generation
- Key: See tutorial for [accessing Google Sheets](https://jingsblog.com/2018/12/03/connect-your-jupyter-notebook-to-google-spread-sheet/). This is the JSON provided when setting up a service user account in GCP.

