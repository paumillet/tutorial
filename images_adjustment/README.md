# Images adjustment tutorial

## Launch with environment.yml with Conda

First, create your virtual environment, given the requirements reported in `environment.yml`:  
```bash
conda env create -n adjustment_env -f environment.yml
```

Then, activate your virtual environment:  
```bash
conda activate adjustment_env
```

Add this virtual environment to the environments list in Jupyter:
```bash
python -m ipykernel install --user --name=adjustment_env
```

Run Jupyter notebook:
```bash
jupyter notebook
```

A new page should open in your browser and list the files in your folder. The notebook `images_adjustment.ipynb` shoud appear in the list. Open it and in Kernel menu, go to `Change kernel` and select the `adjustment_env`.

You can now start following the tutorial.

## Install manually your own environment
Requirements:
* OpenCV
    * with pip:  
    ```bash
    pip install opencv-python
    pip install opencv-contrib-python
    ```
    * with conda: `conda install -c menpo opencv`

* Numpy
    * with pip: `pip install numpy` 
    * with conda: `conda install -c anaconda numpy`

* Matplotlib
    * with pip: `pip install matplotlib` 
    * with conda: `conda install -c conda-forge matplotlib`

* iPyWidgets
    * with pip: `pip install ipywidgets`
    * with conda: `conda install -c anaconda ipywidgets`