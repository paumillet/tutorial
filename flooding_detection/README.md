# Kepler.gl for Jupyter notebook
Kepler.gl is a web-app developed by Uber to visualize large geospatial datasets. The high performance of the application and the styling options ease the exploration of the displayed data. For more informations, please visit their [GitHub](https://github.com/keplergl/kepler.gl), the [application](https://kepler.gl/) or have a look at the [documentation](https://github.com/keplergl/kepler.gl/blob/master/docs/api-reference/overview.md).

Data scientists in Uber work with Jupyter notebook to explore new datasets and expressed their need to have Kepler.gl integrated in Jupyter notebook. Kepler.gl widget has just been released, let's have a look on how to use it with this tutorial.

## Set virtual environnement
1. Create your virtual environnement and launch it:
* From conda :  
```bash
conda create -n <your environnement name> python=3.6 anaconda
conda activate <your environnement name>
```
2. The only required librairy is `keplergl`. All dependencies as `geopandas` will be installed with `keplergl`. To do so, simply run:  
```bash
pip install keplergl
```
3. Add your environnement to ipython kernels list:  
```bash
python -m ipykernel install --user --name=<your environnement name>
```  
4. You're ready to run Jupyter:  
```bash
jupyter notebook
```