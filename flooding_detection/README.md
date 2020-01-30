# Flood detection from Sentinel2 imagery
World Meteorological Organization (WMO) published on September 2019 an assessment on climate evolution over 2015-2019 period. Natural disasters seem more and more present and the most frequent are storms and floodings. Year 2020 already counts storm Gloria over Spain and France (21-22 of January).

This tutorial explains how to detect floodings on satellite imagery.

# Get images data used for the tutorial
The images used are available at the following links (covering France South-West area):
* Image on 2019 December 10
  * [Green band](https://mundiwebservices.com/dp/s2-l2a-2019-q4/30/T/XP/2019/12/10/S2B_MSIL2A_20191210T110339_N0213_R094_T30TXP_20191210T122431/GRANULE/L2A_T30TXP_A014420_20191210T110434/IMG_DATA/R10m/T30TXP_20191210T110339_B03_10m.jp2)
  * [Near Infrared band](https://mundiwebservices.com/dp/s2-l2a-2019-q4/30/T/XP/2019/12/10/S2B_MSIL2A_20191210T110339_N0213_R094_T30TXP_20191210T122431/GRANULE/L2A_T30TXP_A014420_20191210T110434/IMG_DATA/R10m/T30TXP_20191210T110339_B08_10m.jp2)
* Image on 2019 December 15
  * [Green band](https://mundiwebservices.com/dp/s2-l2a-2019-q4/30/T/XP/2019/12/15/S2A_MSIL2A_20191215T110441_N0213_R094_T30TXP_20191215T122756/GRANULE/L2A_T30TXP_A023400_20191215T110444/IMG_DATA/R10m/T30TXP_20191215T110441_B03_10m.jp2)
  * [Near Infrared band](https://mundiwebservices.com/dp/s2-l2a-2019-q4/30/T/XP/2019/12/15/S2A_MSIL2A_20191215T110441_N0213_R094_T30TXP_20191215T122756/GRANULE/L2A_T30TXP_A023400_20191215T110444/IMG_DATA/R10m/T30TXP_20191215T110441_B08_10m.jp2)

You will have to create an account on Mundi WebServices to be able to download them freely.  
Please put the downloaded images in folder `img`.

## Set virtual environnement
1. Create your virtual environnement and launch it:
Conda was used for this tutorial:  
```bash
conda create -n <your environnement name> python=3.6 anaconda
conda activate <your environnement name>
```

But one could also used pip with virtualenv or pipenv for virtual environment management.

2. Required librairies
* `rasterio`
* `geopandas`
* `numpy`
* `fiona`
* `matplotlib`

3. Add your environnement to ipython kernels list:  
```bash
python -m ipykernel install --user --name=<your environnement name>
```

4. You're ready to run Jupyter:  
```bash
jupyter notebook
```