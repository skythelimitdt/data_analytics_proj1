# World Energy Consumption

## Contributors
- Amy Hanks
- Eylem Yildirim
- Sezer Bozoglan

## Project Overview
We chose World Energy Consumption dataset for this project. 

### Analysis:
We answered these questions:
- What is the relationship between energy production per capita and energy consumption per capita across countries?
- Is there a correlation between renewable energy consumption and GDP?
- Is there a correlation between Total Energy Consumption per capita and Total Energy Production per capita in different continents?
- How do energy production and consumption fluctuations correlate with major events?
- What are the projected renewable energy consumption trends for the next 50 years based on current data?


## Data Collection
Data was collected from Kaggle: [link to data](https://www.kaggle.com/datasets/pralabhpoudel/world-energy-consumption/data)

## Data Cleanup
  - Filled all missing fields with 0s
  - Created additional fields: non_renewables_consumption, Total Energy Consumption, non_renewables_production, Total Energy Production,
non-renewables_prod_per_capita, total_prod_per_capita, non-renewables_cons_per_capita, total_cons_per_capita
- Created DataFrames for 'countries' and 'continents'
- Our analysis range was 1985-2022
- Renewable energy projections covered 2010-2022
  
## Report
Key Points:
- Our report analysis looked at Renewable and non-renewable energy data, production and consumption data, countries and continents and GDP. 
- 37 countries in the data represented about 90% of World's production/consumption so our analysis for World's Energy Consumption and Production was based on these top countries.
- We created top_countries_renewable_cons and top_countries_renewable_prod that represented 80% of World's Renewable Energy Consumption and 77% of the World's Renewable Energy Production

**Pie graph showing renewable energy consumption categories for year 2022**
![Renewable Energy Consumption in 2022](Resources/e_renewable_energy.png)

**Pie graph showing non-renewable energy consumption categories for year 2022**
![Non-Renewable Energy Consumption in 2022](Resources/e_non-renewable-consumption.png)

**Pie graph showing renewable and non-renewable energy consumption for year 2022**
![Energy Consumption in 2022](Resources/e_topcountryrnw.png)

 #### What is the Relationship Between Energy Production Per Capita and Energy Consumption Per Capita Across Countries?

 We chose three different years, nearly a decade apart each, to plot the energy consumption per capita and the energy production per capita for each country in that year to see the comparison.

![Energy Consumption and Production per Capita 1995](Resources/a_per_capita_countries1995.png)

![Energy Consumption and Production per Capita 2005](Resources/a_per_capita_countries2005.png)

![Energy Consumption and Production per Capita 2018](Resources/a_per_capita_countries2018.png)


**These graphs show:**
- There are few countries that produced the same amount of energy per capita as they consumed per capita. 
- Several of the countries produced less than they consumed per capita. 
- Then there are some that produced more energy per capita than they consumed per capita. 
- Looking at these graphs we see that there is some shift in production and consumption per capita between countries, but the overall shape of the data per capita stays generally  stable throughout the years. It is interesting to note that the graph of 2018 data shows a decrease in production and consumption per capita overall. This could possibly be due to better technology or more global concerns about energy consumption. It definitely merits more research.

**We included 37 countries that represented 90%+ of World's production and consumption**


![Correlation of Energy Consumption Per Capita and Energy Production Per Capita](Resources/a_per_capita_regression.png)

  - Correlation Coefficient: 0.79
  - r^2 :  0.62
  - T-statistic: 5.296761358343689
  - p-value: 1.3704128715598114e-07
  - ANOVA for Energy Consumption Per Capita from 2008-2018:
  - F_onewayResult(statistic = 0.014319448497051985, p value = 0.9999999844247471)
  - ANOVA for Energy Production Per Capita from 2008-2018:
  - F_onewayResult(statistic = 0.04569316056743195, p value = 0.9999954920296542)

 The correlation coefficient of 0.79 suggests that the energy consumption per capita and energy production per capita are strongly correlated. The r^2 value of 0.62 shows moderate to strong association between the consumption and production, but since 38% of the variability is still unexplained there is potential for further modeling. The positive T-statistic and the very small p-value suggests there is a statistically significant positive difference between energy production per capita and energy consumption per capita across the countries in our dataset. This suggests that energy production per capita exceeds energy consumption per capita across countries we looked at.  <br>

 This could possibly mean certain regions rely on energy imports and others produce excess to fill that need, or perhaps different countries have better production efficiency or different energy needs. <br>

 The ANOVA results with f-statistics both very low and the p values extremely high indicate that energy consumption per capita and energy production per capita have been relatively stable across the years 2008-2018. 


#### Is There a Correlation Between Renewable Energy Consumption and GDP Across Countries

 We calculated the average GDP and Average Renewable Energy Consumption for countries across the years and plotted the information.

![Average GDP and Average Renewable Energy Consumption 1985-2018](Resources/a_avg_gdp_rens_line.png)

-This graph shows similar shapes in the lines of Average GDP and Average Renewables Energy Consumption 

 We chose the top six countries for overall energy consumption and plotted GDP and renewable energy consumption for each of them from 1985-2018

**Results for USA, China, Russia:**
![GDP and Energy Consumption United States, China and Russia (1985-2018)](Resources/a_gdp_rens_countries1.png)

**Results for Japan, India, Germany:**
![GDP and Energy Consumption Japan, India, and Germany (1985-2018)](Resources/a_gdp_rens_countries2.png)

**These graphs show:**

- The United States, China, and India all have GDP and Renewable Energy Consumption lines that generally follow each other in shape. 
- Russia’s GDP has had minimal changes over time with a slow, but mostly steady increase of GDP since the early 2000’s, and their renewable energy consumption is nearly unchanged over time. 
- Japan’s renewable energy consumption generally follows the GDP curve, but with more variability and then a steep increase from around 2012 on.
- Germany’s GDP has had steady growth and their renewable energy consumption followed that  until around 2000 when it started to increase steeply.
- The United States has the largest gap between GDP and Renewable Energy Consumption, possibly indicating a slower adoption of renewable energy sources.
- China has had the fastest growth in both GDP and Renewable Energy Consumption
- Overall we see that the general trend of  increased GDP with increased renewable energy consumption.


**We included 37 countries that represented 90%+ of World's production and consumption**

- We predicted there would be a positive correlation between GDP and renewable energy consumption because we assumed that more wealthy countries would have the technology and social knowledge/pressure to access and use renewable energy.


![Regression Analysis GDP and Renewable Energy Consumption](Resources/a_gdp_renewables_regression.png)


    Correlation Coefficient: 0.79
    T-statistic: 20.76401788304955
    p-value: 1.2461860989954291e-81
    ANOVA for Renewables Consumption:
    F_onewayResult(statistic = 0.31264537493261196, p value = 0.9777430943553933)
    ANOVA for GDP
    F_onewayResult(statistic = 0.14436975081836945, p value = 30.9990640510303093)

- The correlation coefficient of 0.79 suggests that GDP and renewable energy consumption have a strong positive correlation. This indicates increases in GDP correlates to increases in renewables consumption. The positive T-statistic and the very small p-value suggests there is a statistically significant positive difference between GDP and renewables energy consumption across the countries in our dataset. 

- The ANOVA results with f-statistics both very low and the p values extremely high indicate that GDP and renewables energy consumption have been relatively stable across the years 2008-2018. 

- This positive correlation between GDP and Renewables Energy Consumption supports our hypothesis that these variables are positively correlated. This strong positive correlation could imply that as countries become wealthier they may also be more conscious of climate change and sustainability. Perhaps wealthier countries are more likely to invest in renewable energy sources. They may have more technological advancements, government policies to require/incentivise use of renewable energy, or financial capacity to invest in such sources. 


#### How do energy production and consumption fluctuations correlate with major events?

Created a line graph for renewable and non renewable energy production and consumption over the years with the major events to see the trends

![Energy Consumption and Production Trends Over The Years](Resources/e_majorevents.png)

 - Created events dataframe and merged with our main dataframe to include the events we want to analyze. We then created new columns for lagged years as effects of major events may have delayed or lingering impacts

 - Regression analysis with lagged variables

 - Regression results for "energy production and consumption fluctuations correlate with major events" supported the fact that there is a correlation between major events and energy production/consumption values

#### What are the projected renewable energy consumption trends for the next 50 years?
Built a linear regression model and projected future renewable energy consumption levels

![Projected Renewable Energy Next 50 Years](Resources/e_projected_ren-energy_cons.png)

<br>Calculated projected percentage change in renewable energy consumption in 2072: 201.83%
   
- Found projected values for non-renewables energy consumption and created dataframe

- Merged data frames for both projected values and plotted a pie chart to show projected energy consumption values for 2072

![Projected Renewable Energy Next 50 Years](Resources/e_projected_energy.png)

## Tech Stack
- Jupyter Lab
- matplotlib
- pandas
- hvplot
- numpy
- scipy.stats
- seaborn
- statsmodels.api
- holoviews

## Data Ethics and Considerations

The dataset used in this project is sourced from Kaggle. It is intended for informational purposes only and is not to be used for any commercial applications. All data will be handled ethically and responsibly in accordance with the source’s terms of use.


## References

- Ritchie, H., Rosado, P., Mathieu, E., & Roser, M (2023). Our World in Data: Energy dataset. Our World in Data. Retrieved from: [https://www.kaggle.com/datasets/pralabhpoudel/world-energy-consumption/data]
  
- Energy Institute - Statistical Review of World Energy (2024) [https://www.energyinst.org/statistical-review/]
 
- Ember - Yearly Electricity Data (2024) [https://ember-climate.org/data-catalogue/yearly-electricity-data/]; Energy Institute - Statistical Review of World Energy (2024) [https://www.energyinst.org/statistical-review/]
 
- Population based on various sources (2023) [https://ourworldindata.org/population-sources]
  
- U.S. Energy Information Administration - International Energy Data (2023) [https://www.eia.gov/opendata/bulkfiles.php]

- International Renewable Energy Agency (IRENA)-Renewable energy statistics (2023) [https://www.irena.org/Publications/2023/Jul/Renewable-energy-statistics-2023]



ChatGPT help on creating graphs with hvplot.pandas
- Creating event indicators for the major events, help from chatGPT
  def create_lagged_event_indicator(events_merge_df, lag_years=2):
    """
    Creates lagged event indicators for up to `lag_years` after the event.
    For example, if an event occurred in 2014, it will flag the years 2015, 2016, etc.
    """
    for lag in range(1, lag_years + 1):
        events_merge_df[f'event_indicator_lag_{lag}'] = events_merge_df['event_indicator'].shift(+lag, fill_value=0)
    return events_merge_df
- Regression analysis with lagged variables, help from chatGPT:
 
    X_prod = sm.add_constant(X_prod)
    X_cons = sm.add_constant(X_cons)


    model_prod = sm.OLS(y_prod, X_prod).fit()

    model_cons = sm.OLS(y_cons, X_cons).fit()

- ChatGPT help: 
  bar charts with all countries and both per capita variables
  left and right axes line plots 
  
