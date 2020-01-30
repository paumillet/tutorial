# Sentinelsat tutorial
Python librairy that makes you able to search for and download Sentinel data.

## Set virtual environnement
1. Create your virtual environnement and launch it:
Conda was used for this tutorial:  
```bash
conda create -n <your environnement name> python=3.6 anaconda
conda activate <your environnement name>
```

But one could also used pip with virtualenv or pipenv for virtual environment management.

2. Required librairies
* `sentinelsat`: `pip install sentinelsat`
* `geopandas`
* `folium`
* `zipfile`

3. Add your environnement to ipython kernels list:  
```bash
python -m ipykernel install --user --name=<your environnement name>
```

4. You're ready to run Jupyter:  
```bash
jupyter notebook
```