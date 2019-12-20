# Is Environment a New Human Development Indicator Predicted by Economic Complexity?
An introduction to Economic Complexity and Human Development Indicator

## Summary

 

## Key Term Explaination

### Economic Complexity Index

The Economic Complexity Index (ECI) is a measure of the relative knowledge intensity of an economy. ECI measures the knowledge intensity of an economy by considering the knowledge intensity of the products it exports. ECI has been validated as a relevant economic measure by showing its ability to predict future economic growth and explain international variations in income inequality. Economic Complexity (EC) surpasses the predictive power of economic growth (EG), commonly considered as the unique way to achieve economic and human development. 

(Source: The Observatory of Economic Complexity)

### Human Development Indicators

Human Development Indicators represents achievements in key dimensions in one's life: live a long and healthy life (life expectancy), be knowledgeable (education), and have a decent standard of living(income per capita). It was created to emphasize that people and their capabilities should be the ultimate criteria for assessing the development of a country, not economic growth alone. The corresponding Human Development Index (HDI) is a summary measure of average achievement. It can also be used to evaluate national policy choices and set policy priorities: how two countries with the same level of income per capita can end up with different human development outcomes. However, the HDI also has limitations by simplifying and capturing only part of what human development entails but not revealing other criteria such as human security. 

(Source: UNITED NATIONS DEVELOPMENT PROGRAMME)

## Data Sources Description

In this visualization project, 4 datasets are used to create ggplot2, plotly, and tableau visualizations.

- total.csv (represented by object name df in rmarkdown to produce plotly visualizations)

The total datasets stores information on country's ECI and humand development indicators related variables in 2007. Main variables includeds are country name, continent, GDP per capita, ECI, population, life expectancy, lower secondary education completion ratio, primary education duration. The datasets is the results of merging multiple gapminder datasets in RStudio by combining country names and specificy year 2007. 

- total5.csv (represented by object name total5 in rmarkdown to produce ggplot2 visualizations)

The total5 datasets stores information largely similar to total but is instead a timeseries data. In the following ggplot2 visualizations, this dataset is also the results of merging multiple gaminder datasets in RStudio and is used to show the general trend of life expectancy and compared the matchability to that of economic growth and ECI. 

- continent_avg.csv (represented by object name continent_avg in rmarkdown for plotly visualizations)

continent_avg dataset stores timeseries information on each continent's average ECI and lower secondary education completion ratio. This dataset is transformation based on the total5 timeseries data by grouping countries based on continent and calculating the mean value. This dataset is used to create the interactive visualization with year slidebar.

- energy_use and co2_emissions_1964

These two datasets are used to produce the tableau visualization to compare the difference between the average energy use and CO2 emissions per person to evaluate a country's energy use efficiency and possible renewable energy development (with the reference to the average ECI index). The two datasets are transposed before use so that year can be a column variable. The datasets are obtained from the gapminder database. 

- global_power_plant_databased 

The global_power_plant_databased is used to produce the world map visualization of power plants number, location, and primary fuel type in each country. The dataset is obtained from the World Resource Institute. 

## Technologies and Platforms Usage

### Plotly

Plotly is a technical computing company located in Montreal, Quebec that develops and maintains multiple open-source online data analytics and tutorial tools. Plotly develops easily customizable and declarative packages that seperate execution and specification and thus allow users to focus on more important relationships within the data. Plotly’s high customizability and dynamicity render it a popular web-based data visualization tool and a R-based data visualization package, though it has comparatively fewer features than Tableau. The following visualizations are produced with plotly package in RStudio and modified by ChartStudio, plotly's online tool for for creating, styling, and publishing interactive web-based charts
(Source: Plotly Official Website)

### Tableau
Tableau is an American interactive visualization software company founded in Mountain View, California. It develops and maintans online graph-based data visualizations supported by relational database, online analytical processing cubes, cloud databased, and spreadsheets. Tableau is especially known for its mapping functionalities that automatically connect to inbuilt sptial files and generate maps based on recognized latitudes and longitudes coordinates. 
(Source: Tableau Official Website and Wikipedia Page)

## Stories 

### The Predictive Power of Economic Complexity 
Economic Complexity (EC) surpasses the predictive power of economic growth (EG), commonly considered as the unique way to achieve economic and human development. In the example below, life expectancy is picked as the representative human development indicator since it also reflects the magnitude of other human develoment indicators to some degrees: better educations and better income are key to remain a healthy lifestyle and afford proper care and treatment. The ggplot2 visualizations below substantiated the superiority of EC in evaluating country economic development and performance: the correlation between ECI and life expectancy and ECI is much more clear than that between EG and life expectancy. 

##### The Correlation Between Life Expectancy and ECI
<img src="http://drive.google.com/uc?export=view&id=15LUcvEKubl8t2NzfIhqQyKOlL9h8HcW6" alt="Google Logo">

##### The Correlation Between Life Expectancy and Economic Growth
<img src="http://drive.google.com/uc?export=view&id=1mxaiix_M1DWlP8KqVtE-h7tv3tirNf-R" alt="Google Logo">

### The Influence on Policy Analysis and Priority

As indicated above, Human Develoment Index can direct government to prioritize key policies areas that 
#### plotly 3d visualization
<iframe width="900" height="600" frameborder="0" scrolling="no" src="//plot.ly/~xiaoyayue/3.embed"></iframe>

#### plotly timeseries visualization
<iframe width="900" height="600" frameborder="0" scrolling="no" src="//plot.ly/~xiaoyayue/5.embed"></iframe>

### ECI and The Environment

Since the HDI also has limitations by only capturing part of what human development entails, it is worth thinking whether other parameters can come into the picture that are inclusive, informative, and indicative. As the issue of climate change has been drawing more attentions worldwide, it is time to unfold the impacts of environment and energy on both human development and economic development. Environment is a multifacet yet tricky factor: it entails promising industrial progress beneficial to product and economic intensity, renewable energy usage indicative to technological advancement, and CO2 emissions alarming to both human health and natural resources development. In the following visualization, we shall explore all questions in mind. 

#### tableau emission and energy use workbook

<iframe seamless frameborder="0"
src="https://public.tableau.com/views/energy_emission_eci_updated/Dashboard1?:embed=yes&:display_count=yes&:showVizHome=no" width = '1000' height = '700' scrolling='yes' ></iframe>

This tableau visualization position side by side the difference between energy use and CO2 emission and the average ECI for each selected country. In the visualizaiton, we can see that it is generally intuitive that a higher CO2 emission and higher energy use indicates higher ECI. However, based on this visualization only, it is hard for us to understand why there are some countries who 

#### tableau powerplant workbook 

<iframe seamless frameborder="0"
src="https://public.tableau.com/views/World_Power_Plants_Overview_updated/Dashboard?:embed=yes&:display_count=yes&:showVizHome=no" width = '1000' height = '700' scrolling='yes' ></iframe>
