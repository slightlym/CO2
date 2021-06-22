## CO2
Data preparation for Swiss CO2 emissions analysis in Tableau

### Why this project?
In several Swiss campaigns for CO2-related referendum topics I met twice the argument that Switzerland produces little CO2 and thus does not need any additional measures to reduce its impact. Moreover, it happened that the same argument is used in other European countries, sometimes even by ecological partisans.

I think it is a big misunderstanding or a conscious manipulation. It is true that (some) European countries produce (relatively) little CO2 by themselves: there is almost no mining, and production of consumption goods is delegated to countries like China. However, being among the richest world countries, they consume a lot and contribute to production indirectly through their consumption.

In other words, while Switzerland does not produce a lot of CO2 by itself, it makes other countries to produce it a lot. It is called emissions export.

### What is this project about?
The idea is simple: take data from the very same source as authors of the thesis that Switzerland produces little CO2 and show what's wrong with approach of looking just at the total CO2 production.

The data source is [Global Carbon Budget](https://essd.copernicus.org/articles/12/3269/2020/) for 2018 (at the moment of publication, it is the latest year for which both territorial production and CO2 by consumption are available for a big number of world countries (118).

The dashboard will be made in Tableau Public. This repository shows how the data preparation was done.

### Data sources
Two data files were used:

1. Global production and consumption data are taken from [Data supplement to the Global Carbon Budget 2020](https://www.icos-cp.eu/science-and-impact/global-carbon-budget/2020). On the page, one needs to go down to Download section and choose the second file, [2020 National Emissions v1.0](https://data.icos-cp.eu/licence_accept?ids=%5B%22xUUehljs1oTazlGlmigAhvfe%22%5D). In this file, data from the sheet `Territorial Emissions` are saved as `Territorial emissions.csv`, and data from the sheet `Consumption Emissions` are saved as `Consumption emissions.csv`.
2. Per capita production data are taken from [Robbie Andrew's website](https://folk.universitetetioslo.no/roberan/GCB2020.shtml). Robbie Andrew is from CICERO for International Climate Research, and the page is reported to be a repository for figures presented in the Global Carbon Budget 2020. The dataset used is [full fossil CO2 dataset in CSV format, per capita (1750–2019)](https://folk.uio.no/roberan/GCP/data2020/GCB2020v18_percapita_flat.zip). This file is used as is. It is not really needed for the study, and if you prefer a different data source for the population by country, it should not change the results dramatically.

Having these three files (`Territorial emissions.csv`, `Consumption emissions.csv` and Robbie Andrew's `GCB2020v18_MtCO2_flat.csv` files) is all you need to run the data preparation as described in the Jupyter Notebook.
