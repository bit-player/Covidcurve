# The Covid Curve

The code in this repository accompanies the essay "Riding the Covid Coaster," by Brian Hayes, published 18 August 2021 at [http://bit-player.org/2021/riding-the-covid-coaster](http://bit-player.org/2021/riding-the-covid-coaster). It explores various approaches to understanding the trajectory of the Covid-19 epidemic in the United States during its first 18 months.

The programs are organized in three Pluto.jl notebooks:

* covidcurve.jl covers the reconstruction of the Covid-19 incidence curve and attempts to apply Fourier methods, looking for periodic signals in the data. Also a look at time derivatives. Includes code for figures 1, 3, 4, 5, 6, 7, 8, 9, 12.

* SIR_model.jl deals with exponential growth in epidemic processes, and models based on that idea. Figures 10, 11, 13, 14, 16, 17, 18, 19, 20, 21, 23, 24.

* us_states_data.jl breaks down the national Covid data set into records for inividual states and regions. Code for Figure 22.

The underlying data for most of this work was collected and curated by _The New York Times_. The archive is available at [https://github.com/nytimes/covid-19-data](https://github.com/nytimes/covid-19-data). The version I used in the code below, including data from 21 January 2020 through 20 July 2021, is commit c3ab8c1beba1f4728d284c7b1e58d7074254aff8. You can access the identical set of files at [https://github.com/nytimes/covid-19-data/tree/c3ab8c1beba1f4728d284c7b1e58d7074254aff8](https://github.com/nytimes/covid-19-data/tree/c3ab8c1beba1f4728d284c7b1e58d7074254aff8). But you should probably get the most up-to-date version, with the latest data.

Within the _Times_ archive I have used the files within a folder named "rolling-averages," which has daily new cases rather than cumulative cases, and has precomputed the seven-day trailing average of the data sequences.

The code is written in the [Julia programming language](https://julialang.org/) and organized in [Pluto.jl notebooks](https://github.com/fonsp/Pluto.jl).

Instructions:

1. You'll need a working installation of Julia with the Pluto.jl package installed. Version 0.15.1 or later is needed to automatically find, load, and install packages.

2. In a terminal window, cd to the directory where you have stored this file. Start Julia, then at the "julia>" prompt, type "using Pluto; Pluto.run('_filename_.jl')".

3. A browser window will open with this notebook displayed. Pluto will then download all the necessary packages and their dependencies, and will evaluate the cells in the proper order. This can take several minutes, and it can rev up your CPU fan. But then you're done.Five variants of Monte Carlo simulations of the Ising model of ferromagnetism, all written in JavaScript and meant to run in a browser window.
