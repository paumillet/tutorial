Python virtual environment: `kepler_env`
To create it from conda: `conda create -n kepler_env python=3.6 anaconda`

Once your virtual environment is launched (`conda activate kepler_env`), install kepler.gl: `pip install keplergl`.  
In Kepler notebook, geopandas is also required: `pip install geopandas`.

Add your env to ipython kernels list: `python -m ipykernel install --user --name=kepler_env`  
and run Jupyter `jupyter notebook`.