# LSDB Demo at Rare Gems in Big Data

<img src="https://github.com/lincc-frameworks/Rare_Gems_Demo/assets/12860669/6ddcd206-d962-4d9f-8937-b6a6dbd31adc" alt="Rare Gems Poster" width="300">

<img src="https://github.com/lincc-frameworks/tape/blob/main/docs/DARK_Combo_sm.png?raw=true" width="300" height="100">

Demonstration prepared for the [Rare Gems in Big Data 2024](https://noirlab.edu/science/events/websites/rare-gems-2024) meeting.
This demo showcases working with HiPSCat tables via [LSDB](https://lsdb.readthedocs.io/en/stable/).

TODO: add time and room for the presentation from Andy, Neven and this demo

See related documentation:

* HiPSCat ([on GitHub](https://github.com/astronomy-commons/hipscat))
  ([on ReadTheDocs](https://hipscat.readthedocs.io/en/stable/))
* LSDB ([on GitHub](https://github.com/astronomy-commons/lsdb)) 
  ([on ReadTheDocs](https://lsdb.readthedocs.io/en/stable/))

## Getting Started 

You can follow along with this demo by creating your own local environment, or accessing the LINCC azure JupyterHub.

### Local installation

If installing in your own hardware, create a virtual environment then `pip install` relevant packages:

```
>> conda create --name lincc python=3.10
>> conda activate lincc
>> pip install lsdb lf-tape ipyaladin cesium aiohttp
```

### Access LINCC Hub

1. You'll need an account on LINCC azure hub. TODO - how to do that.
2. To get started, create a Large instance on https://lsst.dirac.dev/
3. Clone this repo in LINCC-hub ("New" > "Terminal")

```
>> git clone https://github.com/lincc-frameworks/Rare_Gems_Demo
```

4. Open the notebooks in the "LINCC" kernel. TODO - check if this is the name
5. Work through the notebooks and have fun.
6. Shutdown each notebook after you're done to use less memory.

## Notebooks

### Notebook 1

[Link to notebook](Notebook_1_Load_and_Xmatch.ipynb)

**Overview**:
- Learn how to (lazily) load catalogs
- Learn how to use those catalogs and perform crossmatching with existing LSDB catalogs
- Save the results

### Notebook 2

[Link to notebook](Notebook_2_Basic_Time_Domain.ipynb)

**Overview**:

In this notebook we will learn how to use the outputs from LSDB catalogs and use `ensemble` from TAPE to compute time-series features.

### Notebook 3

[Link to notebook](Notebook_3_Vizier_LSDB_Interaction.ipynb)

**Overview**: 
- Learn how to use VizieR TAP query to access tables and store/handle them in `LSDB`
- Learn how to use those catalogs and perform crossmatching with existing `LSDB` catalogs
- Pass HipsCat LSDB catalogs to `TAPE` to perform time-series analysis and exploration
