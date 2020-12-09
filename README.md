# Projecting COVID-19 Incidence Rates among Counties in the United States

## Abstract

In this project, we investigate causal relationships affecting the outcome of county-level COVID-19 incidence rate, normalized by county population. 

In search of causal relationships affecting the outcome of COVID-19 incidence rate in a county, we explore the following variables:
* Citizen political leaning (Node values: Heavily Republican, Republican, Leaning Republican, Even, Leaning Democrat, Democrat, Heavily Democrat)
* State political leaning (Node values: Democrat, Republican)
* Emergency preparedness, operationalized as ICU bed availability per capita (Node values: Low, Medium, High, Very High availability)
* Proportion of population with no high school education (Node values: Very Low, Low, Medium, High, Very High)
* CDC guideline adherence among the county population (Node values: Low, Medium, High)
* State bans on large gatherings (Node values: Gatherings Prohibited, New Limit on Large Gatherings, Expanded Limit, Lifted Limit)
* Median household income (Node values: Very Low, Low, Medium, High, Very High)
* Urban economic index: An index created by the USDA that captures a county-level "urban vs. rural" metric (Node values: Noncore, Micropolitan, Metropolitan)

## Methods
We started with the hypothesized DAG pictured in the top of our Causal Modeling notebook.

We binned our variables to reduce the dimensionality of the DAG:


## How to explore this project

We invite you to explore the Jupyter notebooks in this directory, which contain in-line commentary regarding our methods and conclusions. You may run the Jupyter notebooks to reproduce our findings if your device meets the software prerequisites enumerated below. 
We have separated the project files into three folders:

* **datasets** <br>
Find our raw datasets here.
* **data_cleaning** <br>
Code to clean and collate our model's variables of interest.
* **causal_modeling**<br>
Our main notebook in which we construct a DAG and run experiments.


### Prerequisites for reproducing results on your machine

The following python packages must be installed to run the Jupyter notebooks in this project:

```
collections
matplotlib
networkx
numpy
pandas
pgmpy
pyro
rpy2.rinterface 
torch
xarray
```

The following R packages must also be installed to run in-line R code within the Jupyter notebooks in this project:
```
bnlearn
Rgraphviz
```


## Authors

* [**Srinidhi Gopalakrishnan**](https://www.linkedin.com/in/srinidhi-g/)

* [**Ryan Douglas**](https://www.linkedin.com/in/ryan-douglas-10/)

* [**Chloe Larkin**](https://www.linkedin.com/in/chloe-larkin/)



## License

This project is licensed under the MIT License - see the [LICENSE.md](https://github.com/chloelarkin/county-covid-cases/blob/main/LICENSE.md) file for details

## Acknowledgments

* We were inspired to build our Pyro DAG with the strategy set out by Shreyans Jasoriya, Mohit Chandarana, and Jayanth Chava in their [**Causal Moneyball**](https://github.com/robertness/causalML/tree/master/projects/causal%20moneyball/Causal-analysis-on-football-transfer-prices) final project in Spring 2020, in which they built a BayesianModel to construct conditional probability tables for a large set of nodes.


* **Data Sources:** <br>
[**ICU bed data**](https://www.kaggle.com/ikiulian/global-hospital-beds-capacity-for-covid19?select=hospital_beds_global_regional_v1.csv) <br>
[**Income, demographic, education, and urban influence category data**](https://www.ers.usda.gov/data-products/county-level-data-sets/) <br>
[**State and policy actions to address coronavirus, including mandates**](https://www.kff.org/coronavirus-covid-19/issue-brief/state-data-and-policy-actions-to-address-coronavirus/#socialdistancing) <br>
[**COVID-19 data by county**](https://coronavirus-resources.esri.com/datasets/628578697fb24d8ea4c32fa0c5ae1843_0?where=(Confirmed%20%3E%200)) <br>
[**Voting data by county**](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/VOQCHQ)

