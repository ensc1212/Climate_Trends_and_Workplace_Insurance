# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Exploring Climate Data of Singapore


### Problem Statement

You are a data analyst at an insurance company that attended a forum held by the Singapore Actuarial Society on how the insurance industry may be impacted by climate trends across the world. You are concerned and wish to understand if the same trends apply to Singapore and have identified workplace safety to be a key area of interest. This analysis will identify weather patterns in Singapore and its implication on workplace related insurance.


---

### Datasets

There are 11 datasets included in the [`data`](../data/) folder for this project. These correspond to rainfall and workplace injury information. 

* [`rainfall-monthly-highest-daily-total.csv`](../data/rainfall-monthly-highest-daily-total.csv): The highest daily total rainfall for the month recorded at the Changi Climate Station.
* [`rainfall-monthly-number-of-rain-days.csv`](../data/rainfall-monthly-number-of-rain-days.csv): Monthly number of rain days from 1982 to 2022. A day is considered to have “rained” if the total rainfall for that day is 0.2mm or more.
* [`rainfall-monthly-total.csv'`](../data/rainfall-monthly-total.csv'): The total monthly rainfall recorded at the Changi Climate Station.
* [`relative-humidity-monthly-mean.csv`](../data/relative-humidity-monthly-mean.csv'): The monthly mean relative humidity recorded at the Changi Climate Station.
*  [`relative-humidity-absolute-monthly-extreme-minimum.csv`](../data/relative-humidity-absolute-monthly-extreme-minimum.csv'): The absolute extreme minimum relative humidity for the month recorded at the Changi Climate Station.
* [`sunshine-duration-monthly-mean-daily-duration.csv`](../data/sunshine-duration-monthly-mean-daily-duration.csv): The monthly mean sunshine hours in a day recorded at the Changi Climate Station.
* [`surface-air-temperature-monthly-mean.csv`](../data/surface-air-temperature-monthly-mean.csv): The monthly mean air temperature recorded at the Changi Climate Station.
*  [`surface-air-temperature-monthly-mean-daily-minimum.csv`](../data/surface-air-temperature-monthly-mean-daily-minimum.csv): The monthly mean daily minimum temperature recorded at the Changi Climate Station.
*  [`surface-air-temperature-monthly-mean-daily-maximum.csv`](../data/surface-air-temperature-monthly-mean-daily-maximum.csv): The monthly mean daily maximum temperature recorded at the Changi Climate Station.
*  [`wet-bulb-temperature-hourly.csv`](../data/wet-bulb-temperature-hourly.csv): The monthly mean hourly wet bulb temperature recorded at the Changi Climate Station. Wet bulb temperature mirrors how the human body cools itself with sweat.
* [`workplace-accidents-years.csv`](./data/workplace-accidents-years.csv): The number of cases of work place injuries in a year, grouped by type of injury and industry of workplace.

### Data Dictionary

|Feature|Type|Dataset|Unit of Measure|Description|
|:---|:---|:---|:---|:---|
|maximum_rainfall_in_a_day|float|h_daily_total|Millimetre|The highest daily total rainfall for the month recorded at the Changi Climate Station.| 
|no_of_rainy_days|int|mthly_rainy_days|Days|The number of rain days (day with rainfall amount of 0.2mm or more) in a month recorded at the Changi Climate Station.| 
|total_rainfall|float|mthly_rainfall_total|Millimetre|The total monthly rainfall recorded at the Changi Climate Station.| 
|mean_rh|float|humidity|Percentage|The monthly mean relative humidity recorded at the Changi Climate Station.| 
|rh_extremes_minimum|int|humidity_min|Percentage|The absolute extreme minimum relative humidity for the month recorded at the Changi Climate Station.| 
|mean_sunshine_hrs|float|sunshine|Hours|The monthly mean sunshine hours in a day recorded at the Changi Climate Station.| 
|mean_temp|float|surface_temp|Degree Celsius|The monthly mean air temperature recorded at the Changi Climate Station.| 
|temp_mean_daily_min|float|s_temp_min_mean|Degree Celsius|The monthly mean daily minimum temperature recorded at the Changi Climate Station.| 
|temp_mean_daily_max|float|s_temp_max_mean|Degree Celsius|The monthly mean daily maximum temperature recorded at the Changi Climate Station.| 
|wet_bulb_temperature|float|wb_temp|Degree Celsius|The monthly mean hourly wet bulb temperature recorded at the Changi Climate Station. Wet bulb temperature mirrors how the human body cools itself with sweat. Note: Found data entry error which was fixed in code.| 
|injuries|int|work_accidents_years|Cases|The number of cases of work place injuries in a year, grouped by type of injury and industry of workplace.|


---

### Key Takeaways

1. Through the years, temperature in Singapore has been increasing while relative humidity has been decreasing. From our correlation tests, correlation between mean relative humidity and mean temperature is -0.63 which indicates a strong negative correlation between the two variables. According to the Clausius-Clapeyron equation, the air can generally hold around 7% more moisture for every 1C of temperature rise. Thus, if moisture content is not increasing at the same rate, relative humidity decreases (Willett, 2020).
2. Standard deviation for number of rainy days and mean relative humidity has been increasing through the years. This is in line with global climate change trends, with weather patterns becoming more erratic. (Medvigy et al., 2012)
3. Correlation between mean temperature and light injuries (construction industry) is 0.84 which indicates a very strong positive correlation between the two variables. This shows that high temperatures can cause heat exhaustion which leads to an increase in workplace accidents, specifically the construction industry where construction workers perform manual work outdoors with little to no shade.
4. Correlation between wet bulb temperature and major injuries (Transportation & Storage) is 0.67 which indicates a strong positive correlation between the two variables. This shows that high levels of humidity combined with high temperatures can cause heat exhaustion which leads to an increase in workplace accidents, specifically the transport and storage industry. Wet bulb temperature is typically the highest between the months of April and July.


---

### Recommendations and Conclusion

Over the years, weather pattern trends in Singapore seem to follow the global average trends, with increasing temperatures, decreasing relative humidity and more erratic weather patterns. While Singapore has not seen extreme weather related disasters causing obvious and visible damage, for example, the California wildfires or the floods in Northen Italy, we are slowly experiencing negative impacts of climate change. As such, literature on global climate trends are still applicable to local context.
One such application is workplace safety which is shown in this project to be closely linked to weather patterns and as such, we should proactively seek out implications of climate trends to the insurance industry to prevent adverse selection, improve pricing models and gather marketing insights.

#### Correlation between Mean Temperature and Light Injuries (Construction)
1. With the trend of increasing temperatures across the years, the actuarial team should look into adequately accounting for the increase in temperature to their long-term workplace safety pricing models so that the insurance company does not become susceptible to adverse selection (adverse selection refers to a scenario where either the buyer or the seller has information about an aspect of product quality that the other party does not have. Adverse selection is a common scenario in the insurance sector, where those who are  high-risk are more likely to sign up for insurance. (CFI, 2022)) by policyholders, where they unwittingly offer cheaper premiums than competitors who have adequately accounted for the impact brought forth by rising temperatures (Storey et al., 2019).
2. Develop an Actuaries Climate Index (ACI), which  seeks to quantify changes in the climate and is used to make  informed decisions.

#### Correlation between Wet Bulb Temperature and Major Injuries (Transportation & Storage)
1. As identified above, the months between April and July have the highest wet bulb temperature. The actuarial team should look into increasing prices for Collision Damage Waiver (a temporary vehicle insurance one can purchase on a monthly basis to cover a large portion of their insurance premiums, typically around 90%, should they get into an accident) for the months between April and July. This is so that the pricing model does not underestimate the impact of wet bulb temperature on the rate of major accidents in the Transportation & Storage industry.  
2. It would also be recommended for the marketing team to increase marketing efforts during periods with expected high wet bulb temperature as transport companies are likely to experience a surge in accidents during those months. Clickthrough rates on advertisements for Collision Damage Waiver ought to be higher as intent is there. This way, the insurance company will beat out competitors to their money by out representing them on advertisement channels specifically for those months, without wasting resources on months with lower wet bulb temperature an thus lower accident rates and consequently lower clickthrough rates.


---

### Citations
CFI Team, C. (2022, December 27). Adverse Selection. Corporate Finance Institute. Retrieved May 26, 2023, from https://corporatefinanceinstitute.com/resources/wealth-management/adverse-selection/

McQuillan, L. (2022, July 20). Too hot to handle: How to survive amid extreme heat and humidity. CBC. Retrieved May 25, 2023, from https://www.cbc.ca/news/health/heat-humidity-bodies-wet-bulb-1.6525711#:~:text=The%20hotter%20and%20more%20humid,others%2C%20according%20to%20Health%20Canada.

Medvigy, D., & Beaulieu, C. (2012). Trends in Daily Solar Radiation and Precipitation Coefficients of Variation since 1984. Journal of Climate, Volume 25(Issue 4), 1330–1339. https://doi.org/10.1175/2011JCLI4115.1

Park, RJ, Pankratz, N, Behrer, AP (2021) Temperature, workplace safety, and labor market inequality. Discussion Paper Series 14560, IZA Institute of Labor Economics. Retrieved May 25, 2023, from https://ftp.iza.org/dp14560.pdf

Storey, C., MacFarlane, A., Spira, J., Davangere, M., Thulliez, M., Bagree, N., Hughes, R., & Watt, S. (2019). Climate Change for Actuaries: An Introduction. Institute and Faculty of Actuaries. Retrieved May 25, 2023, from https://www.actuaries.org.uk/system/files/field/document/Climate-change-report-29072020.pdf

Willett, K. (2020, December 1). Guest post: Investigating climate change’s ‘humidity paradox.’ Carbon Brief. Retrieved May 25, 2023, from https://www.carbonbrief.org/guest-post-investigating-climate-changes-humidity-paradox/