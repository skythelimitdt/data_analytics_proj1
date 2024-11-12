# Read the file we downloaded from Kaggle(https://www.kaggle.com/datasets/pralabhpoudel/world-energy-consumption/data)
# Data is reviewed and cleaned up
  -All columns are reviewed to see what we have
  -Info for the data fields is listed
  -Listed all fields with unavailable data
  -Filled all NAs with 0s to make calculations later
# Once data is reviewed, we created some additional columns: non_renewables_consumption, Total Energy Consumption, non_renewables_production, Total Energy Production,
non-renewables_prod_per_capita, total_prod_per_capita, non-renewables_cons_per_capita, total_cons_per_capita
# Displayed all data fields and their count
# We created countries_world_energy_df dataframe based on iso_code not equal to 0. Then we locked the data fields to >= 1980. So we can look at about 40 years of data
# We created top_countries data field based on:
  -Sorted countries_world_energy_df dataframe by Total Energy Production and Total Energy Consumption to find the top countries to include in the dataframe
  -The datafield we created included 89% of the World's Energy Production and Consumption
# We created top10_country_consumption and top10_country_production dataframes
# We created top_countries_renewable_consumption based on 11 countries that covered 75% of World's Renewable Energy Consumption and 71% of the World's Energy Production

![Energy Production and Consumption Over Years](Resources/e_topcountryrnw.png)
