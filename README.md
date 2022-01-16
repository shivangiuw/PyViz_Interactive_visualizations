# Visualization and analysis of real-estate data using hvPlot and GeoViews

## Housing Rental Analysis for `San Francisco` to find properties that are viable investment opportunities using python data visualization skills, including aggregation, interactive visualizations, and geospatial analysis on following parameters:

* Number of Housing units
* Sales price per square foot (Average for the period/ Years)
* Gross rent (Average for the period/ Years)
* Neighborhoods 


## Technologies

This tool leverages python 3.7 with the following packages:

* [pandas] (https://pandas.pydata.org/docs/getting_started/index.html)- for data analysis
* [jupyter lab] (https://jupyterlab.readthedocs.io/en/stable/)- to work with notebooks, code, data and plots
* [hvplot] (https://hvplot.holoviz.org/user_guide/Introduction.html)- to display an interactively explorable 
                                      plot with panning, zooming, hovering, and clickable/selectable legends
* [geoviews] (https://geoviews.org/) - to explore and visualize geographical data


## Installation Guide

```
 conda install pandas
 pip install jupyterlab
 conda install -c pyviz hvplot geoviews

 ```
## Usage

Analysis of the housing property data is done through following steps:

1. Calculate and plot the housing units per year.
Using `groupby` function to group the data by year, aggregate the results by the mean of the groups and then visualize the results of housing_units_by_year as a bar chart.

 ![](Images/bokeh_plot(5).png)

 ![](Images/bokeh_plot(4).png)


### Observation on the overall trend in housing units over the period under analysis
 * The number of housing units has been increasing year on year, where the growth has been steady which is due to inflow of population as a result of growth in tech industry in the bay area which has led to increased in demand in owned housing and rental.

2. Calculate and plot the average prices per square foot.

- Using `groupby`  and `mean` function to group the data by year and further aggregate the results. Using `sort_values()`, look at the gross rent .
- Further sort the data to include the averages per year for only the `sale price per square foot` and the `gross rent`. Plot the visualization for both using `hvplot`.

 ![](Images/bokeh_plot(3).png)

### Observations on gross rent and average sale price per square foot for San Francisco
* The lowest gross rent reported for the years included in the DataFrame is in year 2010 of USD 1239.00 which grew to more than thrice in six years.

* A drop in average sale price per square foot can be seen in year 2011 with average sale price per square foot is 341.90 as compared to year 2010 where the average sale price is 369.34. Afterwards there has been gradual growth in average sale price per square foot iver the years in San Francisco area.

* The gross rent increased to 1530.00 in year 2011 from 1239.00 as in year 2010 which kept growing rapidly in later years for the city.

3. Compare the Average Sale Prices by Neighborhood

- Here, group the data by year by year and neighborhood and further aggregate the results. 
- Further sort the data to include the averages per year for only the sale price per square foot and the gross rent.
- Create an interactive plot with hvPlot that visualizes both sale_price_sqr_foot and gross_rent creating an interactive widget for neighborhoods.

 ![](Images/bokeh_plot(2).png)


### Observations on gross rent and average sale price per square foot by Neighborhoods

* In Anza Vista neighborhood, we observe from the plot that average sale price per square foot in the year 2016(88.402) is less than that of year 2012(344.491) due to drop in housing prices since 2014 whereas growth in gross for the neighborhood accelerated in year 2014 which may be due to preference and more demand for rental housing than owned housing.

4. Build an Interactive Neighborhood Map

-  In this section, explore the geospatial relationships in the data by using interactive visualizations with hvPlot and GeoViews. 
- To build the map, combine the housing average prices data (created during the initial import), with the one which includes the neighborhood location data using `concat` and aggregate the result using `mean`.
- To create the geospatial visualization, use hvPlot with GeoViews enabled, create a points plot for the the combined DataFrame.

 ![](Images/bokeh_plot(1).png)


### Neighborhood with the highest gross rent, and the highest sale price per square foot.

* Looking at the  interactive map and hovering over, we can confirm that `Westwood Park` neighborhood (darkest blue dot in map) has the highest gross rent of 3959.00. Also, we can say that `Union Square District` neighborhood (biggest dot)has the highest sale price per square foot of 903.99.

### The trend in rental income growth compare to the trend in sales prices and Does this same trend hold true for all the neighborhoods across San Francisco.

* Both rental income and sales prices in San Francisco have seen an upward trend, however the rental income has been growing more than sales prices as growth in sales prices has been sluggish over the years.Although almost all the neighborhoods saw a rapid growth in rental income but we can certainly not say that the trend had been the same for all the neighborhoods in San Francisco, as some neighborhoods like Anza Vista, Hayez valley, Marina etc. saw a downward trend in sales prices in later period i.e after 2014 while some others saw a zigzag trend in  sales prices per square foot like Golden Gate Heights. While some neighborhoods had consistent sales prices over the years like Bayview and Westwood Park, others saw a sluggish growth over the years.

### Do neighborhoods exist that you would suggest for investment, and why?

* Looking at the trend, we can see there has been growth in housing prices as well as gross rent in most of the neighborhoods in San Francisco due to growth in tech industry and the average household incomes and inflow of more population in the area. We should further see this trend in future due to continuos expansion in tech industry in the area.

* To confirm our insights, we look at the data visualizations. Looking at the data and visualizations for investment, neighborhoods with growth in housing prices over the years as well as with the higher rent or growth in gross rent are best options for investment as the investor can earn rental income(high and growing)if buying the house as second home, and also earn profit from house price appreciation over the years if he wishes to sell the house in future. The neighborhoods with slow growth in housing prices but with robust growth or high rent can be considered the good investments for long term. Also, the neighborhoods with lower housing sale price sqr foot but with consistent gross rent can be considered for small budget investments to have regular monthly income from it for long term.

##### Analysis could be taken further by calculating yearly growth in sales per square foot for housing units by neighborhoods and comparing/matching them with gross rent. Further sorting the neighborhoods with positive and higher growth in prices as well as best rent values according to the investment budget can be considered for investment.
