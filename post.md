# An Exploratory Study of Economic Complexity and Human Development Indicators

## Summary
This project aims to conduct an exploratory data visualization on the correlation between Economic Complexity and Human Development Indicators. Economic Complexity has predictive power on country's policy orientation and decision-making in the field of human development and serves as a powerful tool to validate the efficiency of policy changes based on comparative trends as shown in the following data visualizations. In addition to traditional human development indicators - life expectancy, education, and income - it would be interesting to see whether the rising study of environment and energy can be seen as a new human development indicator. The result shows that energy use and CO2 emission can be seen as measures that represent achievements because of their correlations with Economic Complexity Index, but further study has to be done on the field of renewable energy to draw a more definitive conclusion on whether environment can be regarded as the new human development indicator.

## Key Term Explanation

### Economic Complexity Index

The Economic Complexity Index (ECI) is a measure of the relative knowledge intensity of an economy. ECI measures the knowledge intensity of an economy by considering the knowledge intensity of the products it exports. ECI has been validated as a relevant economic measure by showing its ability to predict future economic growth and explain international variations in income inequality. Economic Complexity (EC) surpasses the predictive power of Economic Growth (EG), commonly considered as the unique way to achieve economic and human development. 

(Source: The Observatory of Economic Complexity)

### Human Development Indicators

Human Development Indicators represents achievements in key dimensions in one's life: live a long and healthy life (life expectancy), be knowledgeable (education), and have a decent standard of living (income per capita). It was created to emphasize that people and their capabilities should be the ultimate criteria for assessing the development of a country, not economic growth alone. The corresponding Human Development Index (HDI) is a summary measure of average achievement. It can also be used to evaluate national policy choices and set policy priorities: how two countries with the same level of income per capita can end up with different human development outcomes. However, the HDI has limitations by simplifying and capturing only part of what human development entails but not revealing other criteria such as human security. 

(Source: United Nations Development Programme)

## Data Source Descriptions

In this visualization project, 5 datasets are used to create ggplot2, plotly, and tableau visualizations.

- total.csv (represented by object name 'df' in RMarkdown to produce plotly 3D visualization)

The total dataset stores information on country's ECI and human development indicators related variables in 2007. Main variables included are country name, continent, GDP per capita, ECI, population, life expectancy, lower secondary education completion ratio, and primary education duration. Multiple gapminder datasets are merged to create this dataset in RStudio by combining country names and specifying the year parameter to 2007. 

- total5.csv (represented by object name 'total5' in RMarkdown to produce ggplot2 visualizations)

The total5 dataset stores information largely similar to 'total' but is instead a timeseries data. 

- continent_avg.csv (represented by object name 'continent_avg' in RMarkdown to produce plotly slide bar visualization)

The continent_avg dataset stores timeseries information on each continent's average ECI and average lower secondary education completion ratio. This dataset is transformed based on the 'total5' timeseries data by grouping countries based on continent and calculating each continent's mean value for each year. 

- energy_use and co2_emissions_1964

These two datasets are used to produce the first tableau visualization to compare the difference between the average energy use and the average CO2 emission per person with the reference of average ECI index for each selected country. The two datasets are transposed before use so that year can be a column variable. The datasets are obtained from the gapminder database. 

- global_power_plant_database

The global_power_plant_database dataset is used to produce the world map visualization of the number of power plants, their locations, and their primary fuel type in each country. The dataset is downloaded from the World Resource Institute database. 

## Technologies and Platforms

### Plotly

Plotly is a technical computing company located in Montreal, Quebec that develops and maintains multiple open-source online data analytics and tutorial tools. Plotly develops easily customizable and declarative packages that separate execution and specification and thus allow users to focus on more important relationships within the data. Plotly’s high customizability and dynamicity render it a popular web-based data visualization tool and a R-based data visualization package, though it has comparatively fewer features than Tableau. Two of the following visualizations are produced with plotly package in RStudio and modified by ChartStudio, plotly's online tool for creating, styling, and publishing interactive web-based charts
(Source: Plotly Official Website)

### Tableau
Tableau is an American interactive visualization software company founded in Mountain View, California. It develops and maintains online graph-based data visualizations supported by relational database, online analytical processing cubes, cloud databased, and spreadsheets. Tableau is especially known for its mapping functionalities that automatically connect recognized latitudes and longitudes coordinates to inbuilt spatial files.
(Source: Tableau Official Website and Wikipedia Page)

## Story

### - The Predictive Power of Economic Complexity 
Economic Complexity surpasses the predictive power of Economic Growth, commonly considered as the unique way to evaluate economic and human development. In the example below, life expectancy is picked as the representative human development indicator since it also reflects the magnitude of other human development indicators to some degrees: better educations and better income are key to remain a healthy lifestyle and afford proper care and treatment. The ggplot2 visualizations below substantiate the superiority of Economic Complexity in evaluating country economic development and performance: the correlation between ECI and life expectancy is much clearer than that between Economic Growth and life expectancy. 

##### The Correlation Between Life Expectancy and ECI
<img src="http://drive.google.com/uc?export=view&id=15LUcvEKubl8t2NzfIhqQyKOlL9h8HcW6" alt="Google Logo">

##### The Correlation Between Life Expectancy and Economic Growth
<img src="http://drive.google.com/uc?export=view&id=1mxaiix_M1DWlP8KqVtE-h7tv3tirNf-R" alt="Google Logo">

### - Economic Complexity's Influence and Validation on Policy Choice and Priority

As indicated above, Human Development Index can direct government to prioritize key policy areas in a broad range of policy measures. For example, in education, we can see that lower secondary education completion ratio (ratio) is a much more important and relevant measure than primary education duration (duration) by dragging the 3D visualization below. 

#### Education Parameters and ECI
<iframe width="900" height="600" frameborder="0" scrolling="no" src="//plot.ly/~xiaoyayue/3.embed"></iframe>

To explore further the correlation between Economic Complexity and secondary education completion ratio across time, we could compare their similarities and differences in a timeseries visualization. Below we can see that the variations in ECI correspond to the variations in completion ratio, especially for Europe where a majority of countries are highly developed countries and the line and scatters are highly overlapping. For other continents, ECI is still a pretty good indicator of the changing trend of lower secondary education duration, despite the comparative magnitude gap between the two. 

#### Completion Ratio and ECI Trend Comparison
<iframe width="900" height="600" frameborder="0" scrolling="no" src="//plot.ly/~xiaoyayue/5.embed"></iframe>

### ECI and Environment

Since the HDI has limitations by only capturing part of what human development entails, it is worth thinking whether other parameters can come into the picture that are inclusive, informative, and indicative of country development. As the issue of climate change has been drawing more attentions worldwide, it is time to unfold the impacts of environment and energy on development. Environment is a multi-facet yet tricky factor: it entails promising industrial progress beneficial to product and economic intensity, renewable energy usage indicating technological advancements, and CO2 emissions alarming to both human health and natural resource exploitations and extinctions. In the following visualization, we shall explore all questions in mind. 

<iframe seamless frameborder="0"
src="https://public.tableau.com/views/energy_emission_eci_updated/Dashboard1?:embed=yes&:display_count=yes&:showVizHome=no" width = '1000' height = '700' scrolling='yes' ></iframe>

This tableau visualization position the difference between the average energy use and CO2 emission per person and the average ECI for each selected country side by side. We can see that it is clear that a higher average CO2 emission and energy use indicate a higher ECI. This is intuitive: countries with good economic performance generally have more intensive economic activities and also larger quantities of energy usage to keep up a certain lifestyle. However, based on this visualization only, it is hard for us to understand the meanings of energy use divided by CO2 emission in percentage since there is no apparent pattern shown in the visualization. 

<iframe seamless frameborder="0"
src="https://public.tableau.com/views/World_Power_Plants_Overview_updated/Dashboard?:embed=yes&:display_count=yes&:showVizHome=no" width = '1000' height = '700' scrolling='yes' ></iframe>

With the help of the power plant visualization above, however, we can see that countries or regions that have high percentage usually have more power plants whose primary fuel type is renewable energy, such as hydro, wind, and biomass, or technologically advanced nuclear energy. High percentage can be an indication for high energy efficiency: the lesser energy used to produce the same amount of CO2 emission, the less efficient an energy is. In the visualization, high percentage and renewable energy co-occur in many Northern European countries, South American countries, and Southeastern countries. Although this correlation may not be theoretically solid enough to prove anything, it directs policy makers to an areas worth studying in the future. 
