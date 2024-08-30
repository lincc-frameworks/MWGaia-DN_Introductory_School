# LSDB Demo at the MWGaia-DN Introductory School

<img src="https://indico.cern.ch/event/1413524/logo-1468400139.png" alt="Poster">

<img src="https://raw.githubusercontent.com/astronomy-commons/lsdb/main/docs/lincc-logo.png" width="300" height="100">

Demonstration prepared for the [MWGaia-DN Introductory School](https://indico.cern.ch/event/1413524), Coimbra, 2024.
This demo showcases working with HEALPix-partitioned survey catalogs via [LSDB](https://lsdb.readthedocs.io/en/stable/), and time domain analysis with [nested-dask](https://nested-dask.readthedocs.io/en/stable/).

**Time and location:** X pm, Thursday, September 12, in X room

% TODO: Update time and location

### Main references

% TODO: Update slide deck link

* Presentation [slide deck]()

* LSDB ([on GitHub](https://github.com/astronomy-commons/lsdb)) 
  ([on ReadTheDocs](https://lsdb.readthedocs.io/en/stable/))
* HiPSCat ([on GitHub](https://github.com/astronomy-commons/hipscat))
  ([on ReadTheDocs](https://hipscat.readthedocs.io/en/stable/))
* nested-dask ([on GitHub](https://github.com/lincc-frameworks/nested-dask)) 
  ([on ReadTheDocs](https://nested-dask.readthedocs.io/en/stable/))
* nested-pandas ([on GitHub](https://github.com/lincc-frameworks/nested-pandas)) 
  ([on ReadTheDocs](https://nested-pandas.readthedocs.io/en/stable/))


## Getting Started 

You can follow along with this demo by creating your own local environment, or accessing the LINCC-hub (a shared cloud-hosted JupyterHub). We recommend using LINCC-hub because of the close proximity to our servers hosting the survey data. Also, the code should run much quicker and smoother because the instances have powerful resources available.

### Access LINCC Hub [RECOMMENDED]

1. You'll need an account on LINCC-hub. You can sign up by completing [this form](https://forms.gle/Xcm4oQJubSQySciz6), and following the steps. Please complete this prior to attending the demo. You will receive an invite to the GitHub group at the email that is registered with your GitHub acccount. You may need to accept the membership invite.
2. *BEFORE STARTING YOUR SERVER*, note that you should not use the default size! On the "Server Options" page select "Need more CPU or memory...?" and choose a "Large" server.
3. To get started, log into https://lsst.dirac.dev/ with your GitHub sign-on. If this fails, please reach out to scampos@andrew.cmu.edu.
4. After your server has started up (it will take 3 minutes at least!), clone this repo in LINCC-hub ("New" > "Terminal")

```
git clone https://github.com/lincc-frameworks/MWGaia-DN_Introductory_School
```

5. Open the notebooks with the "MWGaia-DN School" kernel. If next to the kernel name there is a label saying "Not Trusted", click it and "Trust" the notebook. Running, especially the first cells, should take a minute. Feel free to run it before the demo starts if you want to follow along.
6. Work through the notebooks and have fun.
7. Shutdown each notebook after you're done to use less memory.

### Local installation

If installing in your own hardware, create a virtual environment and install the relevant packages:

```
>> conda create --name lincc python=3.11
>> conda activate lincc
>> pip install lsdb pyvo ipyaladin cesium scikit-learn aiohttp
```

## Notebooks

### [Notebook 1](Notebook_1_Load_and_Xmatch.ipynb)

In this notebook we will learn how to:

- Load object and source catalogs (lazily)
- Perform crossmatching with existing `LSDB` catalogs
- Save the results of a science workflow to disk

### [Notebook 2](Notebook_2_Basic_Time_Domain.ipynb)

In this notebook we will learn how to:

- Query and filter catalog data
- Compute time-series features for LSDB catalogs using `nested-dask`
- Plot light curves and periodograms

### [Notebook 3](Notebook_3_Vizier_LSDB_Interaction.ipynb)

In this notebook we will learn how to:

- Use VizieR TAP query to access tables and store/handle them in `LSDB`
- Use those catalogs to perform crossmatching with existing `LSDB` catalogs
- Perform time-series analysis and exploration with `nested-dask`

## LINCC Tech Talks

Watch the following [LINCC Tech Talk](https://www.youtube.com/watch?v=yoGhI72Vl40) to learn more about LSDB. Other relevant talks can be found in the [LSST Discovery Alliance website](https://lsstdiscoveryalliance.org/programs/tech-talks/).

## Acknowledgements

This project is supported by Schmidt Sciences.

This project is based upon work supported by the National Science Foundation under Grant No. AST-2003196.

This project acknowledges support from the DIRAC Institute in the Department of Astronomy at the University of Washington. The DIRAC Institute is supported through generous gifts from the Charles and Lisa Simonyi Fund for Arts and Sciences, and the Washington Research Foundation.
