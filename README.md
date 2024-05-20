# LSDB Demo at Rare Gems in Big Data

<img src="https://github.com/lincc-frameworks/Rare_Gems_Demo/assets/12860669/6ddcd206-d962-4d9f-8937-b6a6dbd31adc" alt="Rare Gems Poster" width="300">

<img src="https://github.com/lincc-frameworks/tape/blob/main/docs/DARK_Combo_sm.png?raw=true" width="300" height="100">

Demonstration prepared for the [Rare Gems in Big Data 2024](https://noirlab.edu/science/events/websites/rare-gems-2024) meeting.
This demo showcases working with HiPSCat tables via [LSDB](https://lsdb.readthedocs.io/en/stable/), and doing time domain analysis with [TAPE](https://tape.readthedocs.io/en/stable).


See related documentation:

* HiPSCat ([on GitHub](https://github.com/astronomy-commons/hipscat))
  ([on ReadTheDocs](https://hipscat.readthedocs.io/en/stable/))
* LSDB ([on GitHub](https://github.com/astronomy-commons/lsdb)) 
  ([on ReadTheDocs](https://lsdb.readthedocs.io/en/stable/))
* TAPE ([on GitHub](https://github.com/lincc-frameworks/tape)) 
  ([on ReadTheDocs](https://tape.readthedocs.io/en/stable))

Demo time and place:
  - 4.00 pm, Wednesday, May 22, in Kiva room

Relevant talks:
  - 3.00 pm, Monday, May 20, Anastasios (Andy) Tzanidakis [presentation](https://drive.google.com/file/d/13oTzaXXR5XZokFXEdXjtsYmHFBCesvLy/view)
  - 11.15 am, Tuesday, May 21, Neven Caplar - [presentation](https://docs.google.com/presentation/d/19_krkvCRt4RCUs4AKpmqqr--AQQC6MGiuBjCgq-inqw/edit?usp=sharing)



## Getting Started 

You can follow along with this demo by creating your own local environment, or accessing the LINCC-hub (a shared cloud-hosted JupyterHub).

### Local installation

If installing in your own hardware, create a virtual environment then `pip install` relevant packages:

```
>> conda create --name lincc python=3.10
>> conda activate lincc
>> pip install lsdb lf-tape ipyaladin cesium aiohttp sklearn
```

### Access LINCC Hub

1. You'll need an account on LINCC-hub. You can sign up by completing [this form](https://forms.gle/n3cTLqh3eiQQrgD19), and following the steps. Please complete this prior to attending the demo.
2. *BEFORE STARTING YOUR SERVER*, note that you should not use the default size! On the "Server Options" page select "Need more CPU or memory...?" and choose a "Large" server. 
3. To get started, log into https://lsst.dirac.dev/. If this fails, reach out over slack on [#lsdb_tape_tutorial](https://raregems2024.slack.com/archives/C073N8DFC22) and tag @nevencaplar.
4. After your server has started up (it will take 3 minutes at least!), clone this repo in LINCC-hub ("New" > "Terminal")

```
git clone https://github.com/lincc-frameworks/Rare_Gems_Demo
```

5. Open the notebooks in the "Rare Gems 2024" kernel. Running, especially the first cell, can take a minute, so feel free to run it before the demo start if you want to follow along.
6. Work through the notebooks and have fun.
7. Shutdown each notebook after you're done to use less memory.

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

## Acknowledgements

This project is supported by Schmidt Sciences.

