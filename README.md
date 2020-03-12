# Jupyter Notebook with Google Sheets

A Jupyter notebook that connects to Google Sheets. Jupyter notebook is handy for demonstrating analytics alongside code and Github is a good place to host it. There are limitations around interactive graphs provided by `plotly` - and in order to show the plots, you would want to generate images.

I've initially developed this to be used for work - displaying generated SVG images for survey results. I used this as a way to remove identifiable emails and restrict other colleagues from accessing the actual data source.

I've removed all sensitive data and copied over most of the code so that the process is documented.


## Set up
### Requirements

#### Code dependencies

- Install Python3
- Set up virtualenv

```shell
python3 -m venv venv
```

- Install dependencies: this will install [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/running.html)

```shell
source venv/bin/activate
pip install -r requirements.txt
```

#### Authentication
- Authentication with Google Sheets: See tutorial for [accessing Google Sheets](https://jingsblog.com/2018/12/03/connect-your-jupyter-notebook-to-google-spread-sheet/). If this is your first time using this service, you will also need to enable the API from your GCP account. Following the aforementioned tutorial should result in a key JSON file.
- The key JSON file needs to be placed in `key/service_acccount_GS.json`

### Optional Requirements
You also need to install Orca for image generation. Follow their [tutorial](https://github.com/plotly/orca) - make sure you use Node 8 if you are going to use `npm` to do the installation.


## Updating the notebook

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
