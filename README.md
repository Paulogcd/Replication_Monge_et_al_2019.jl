# Replication_Monge_et_al_2019

[![Stable](https://img.shields.io/badge/docs-stable-blue.svg)](https://Paulogcd.github.io/Replication_Monge_et_al_2019.jl/stable/)
[![Dev](https://img.shields.io/badge/docs-dev-blue.svg)](https://Paulogcd.github.io/Replication_Monge_et_al_2019.jl/dev/)
[![Build Status](https://github.com/Paulogcd/Replication_Monge_et_al_2019.jl/actions/workflows/CI.yml/badge.svg?branch=main)](https://github.com/Paulogcd/Replication_Monge_et_al_2019.jl/actions/workflows/CI.yml?query=branch%3Amain)
[![Coverage](https://codecov.io/gh/Paulogcd/Replication_Monge_et_al_2019.jl/branch/main/graph/badge.svg)](https://codecov.io/gh/Paulogcd/Replication_Monge_et_al_2019.jl)


This repository is dedicated to the replication of the article _Natural Resources and Global Misallocation_ by Monge et al, 2019, in Julia. 

The article is : Monge-Naranjo, Alexander, Juan M. Sánchez, and Raül Santaeulàlia-Llopis. “Natural Resources and Global Misallocation.” American Economic Journal: Macroeconomics 11, no. 2 (2019): 79–126. https://www.jstor.org/stable/26621311.

We are COMPÉRAT Étienne, CHAMBON Lionel, and GUGELMO CAVALHEIRO DIAS Paulo, and this replication package is done for the *Computational Economics* Class, taught by Florian Oswald during the Fall 2024 semester in the Sciences Po Master of Research in Economics. 

You can go to its dedicated webpage [here](https://www.paulogcd.com/Replication_Monge_et_al_2019.jl/) to have a better overview of the package. 

# Starting the package :

```
using Pkg
Pkg.activate(".")
Pkg.add(url = "https://github.com/Paulogcd/Replication_Monge_et_al_2019.jl")
using Replication_Monge_et_al_2019 # The precompilation might ake some time (24 seconds on Mac M1)

# to get all the results inside a 'output' folder : 
run()

# to delete all the output : 
delete_all()
```

# Replication results : 

We managed to replicate the whole replication package provided by the authors in Stata.
This file is provided in the `output` folder, under the name `pwt_data_3.csv`. 

We also managed to partially reproduce different figures and tables, namely : 

- Figure 1
- Figure 2
- Figure 3
- Figure 4

- Table 1  
- Table 3
- Table 4
- Table 5

We choose not to include the Figure 2, due to it being a statistic description of data of another paper.

All of the obtained figures and tables are described and discussed in the package website.

# Tests procedure and results 

We used the `Test` package to test the quality of the replicated data, and compare it with the data from the Replication package. 
In this sense, although some extensive tests are failing, it does no mean that we did not manage to obtain similar results to the authors. 

Once we are in the folder of the repository, we can run the replication tests.

When running,

```
Pkg.test("Replication_Monge_et_al_2019")
```

We obtain : 

![Tests](./tests_2.png)

And when running 

```
extensive_tests()
```

We obtain : 

![Extensive Tests](./extensive_tests.png)

The tests are more detailed in the dedicated section of the website of the package.