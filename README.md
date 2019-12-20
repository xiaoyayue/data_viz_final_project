# Is Environment a New Human Development Indicator?
An introduction to Economic Complexity and Human Development Indicator

## Executive summary

A link to your visualization

## Data Sources Description

In this visualization project, 4 datasets are used to create ggplot2, plotly, and tableau visualizations
1. total.csv (represented by object name df in rmarkdown to produce plotly visualizations)

The total datasets stores information on country's ECI and humand development indicators related variables in 2007. Main variables includeds are country name, continent, GDP per capita, ECI, population, life expectancy, lower secondary education completion ratio, primary education duration. The datasets is the results of merging multiple gapminder datasets in RStudio by combining country names and specificy year 2007. 

2. total5.csv (represented by object name total5 in rmarkdown to produce ggplot2 visualizations)

The total5 datasets stores information largely similar to total but is instead a timeseries data. In the following ggplot2 visualizations, this dataset is also the results of merging multiple gaminder datasets in RStudio and is used to show the general trend of life expectancy and compared the matchability to that of economic growth and ECI. 

3. continent_avg.csv (represented by object name continent_avg in rmarkdown for plotly visualizations)

continent_avg dataset stores timeseries information on each continent's average ECI and lower secondary education completion ratio. This dataset is transformation based on the total5 timeseries data by grouping countries based on continent and calculating the mean value. This dataset is used to create the interactive visualization with year slidebar.

4. energy_use and co2_emissions_1964

These two datasets are used to produce the tableau visualization to compare the difference between the average energy use and CO2 emissions per person to evaluate a country's energy use efficiency and possible renewable energy development (with the reference to the average ECI index). There two datasets are transposed before use so that year can be a column variable. The datasets are obtained from the gapminder database. 

5. global_power_plant_databased 

The global_power_plant_databased is used to produce the world map visualization of power plants number, location, and primary fuel type in each country. The dataset is obtained from the World Resource Institute. 

## Technologies and Platforms Usage

List/description of the significant technologies/platforms used

## Stories 
Key highlights/stories your visualization can be used to highlight (talking points)

#### ggplot eci
<img src="http://drive.google.com/uc?export=view&id=15LUcvEKubl8t2NzfIhqQyKOlL9h8HcW6" alt="Google Logo">

### gdp
<img src="http://drive.google.com/uc?export=view&id=1mxaiix_M1DWlP8KqVtE-h7tv3tirNf-R" alt="Google Logo">

#### plotly 3d visualization
<iframe width="900" height="600" frameborder="0" scrolling="no" src="//plot.ly/~xiaoyayue/3.embed"></iframe>

#### plotly timeseries visualization
<iframe width="900" height="600" frameborder="0" scrolling="no" src="//plot.ly/~xiaoyayue/5.embed"></iframe>

#### tableau powerplant workbook 

<iframe seamless frameborder="0"
src="https://public.tableau.com/views/World_Power_Plants_Overview_updated/Dashboard?:embed=yes&:display_count=yes&:showVizHome=no" width = '1000' height = '700' scrolling='yes' ></iframe>

#### tableau emission and energy use workbook

<iframe seamless frameborder="0"
src="https://public.tableau.com/views/energy_emission_eci_updated/Dashboard1?:embed=yes&:display_count=yes&:showVizHome=no" width = '1000' height = '700' scrolling='yes' ></iframe>
