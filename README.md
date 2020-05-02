# COVID-19

### SIR Isaac Newton's public repo for COVID-19 Math Modeling Contest


In an effort to maximize collaboration, we are happy to share some data/code we think could be helpful for other groups!



## Contents
* #### Parsed Google mobility data: mobile phone tracking by county (FIPS code)
  * Great for social distancing metrics
  * Trends as of March 29 and April 5
  * Raw: Empty/Null values for non-reported measures
  * Filled: Empty/Null county-level values replaced by state-level measures
  * Excel and Pickle files
  * Original PDF's can be found by searching for "Google Mobility Reports"
  * Contact Kellen at ksandvi@emory.edu for Python notebook used for PDF-TXT conversion and parsing
  
 * #### Aggregated, county-level features
   * Collected from the following sources: https://www.countyhealthrankings.org/ 
    , https://hifld-geoplatform.opendata.arcgis.com/datasets/hospitals/data
    , https://www.census.gov/data-tools/demo/saipe/#/?map_geoSelector=aa_c&s_year=2018&s_state=&s_county=
    , https://electionlab.mit.edu/data
    , https://www.census.gov/data/tables/2015/demo/metro-micro/commuting-flows-2015.html
    , http://www.usreligioncensus.org/
    , https://www.fcc.gov/general/form-477-census-tract-information
   * Excel and Pickle files
   * Information on each county (may contain missing values):
 ```Python
 ['FIPS',
 'State',
 'County',
 'Premature death: Deaths',
 'Premature death: Years of Potential Life Lost Rate',
 'Poor or fair health: % Fair or Poor Health',
 'Poor physical health days: Average Number of Physically Unhealthy Days',
 'Poor mental health days: Average Number of Mentally Unhealthy Days',
 'Low birthweight: Unreliable',
 'Low birthweight: % Low Birthweight',
 'Adult smoking: % Smokers',
 'Adult obesity: % Adults with Obesity',
 'Food environment index: Food Environment Index',
 'Physical inactivity: % Physically Inactive',
 'Access to exercise opportunities: % With Access to Exercise Opportunities',
 'Excessive drinking: % Excessive Drinking',
 'Alcohol-impaired driving deaths: # Alcohol-Impaired Driving Deaths',
 'Alcohol-impaired driving deaths: # Driving Deaths',
 'Alcohol-impaired driving deaths: % Driving Deaths with Alcohol Involvement',
 'Sexually transmitted infections: # Chlamydia Cases',
 'Sexually transmitted infections: Chlamydia Rate',
 'Teen births: Teen Birth Rate',
 'Uninsured: # Uninsured',
 'Uninsured: % Uninsured',
 'Primary care physicians: # Primary Care Physicians',
 'Primary care physicians: Primary Care Physicians Rate',
 'Primary care physicians: Primary Care Physicians Ratio',
 'Dentists: # Dentists',
 'Dentists: Dentist Rate',
 'Dentists: Dentist Ratio',
 'Mental health providers: # Mental Health Providers',
 'Mental health providers: Mental Health Provider Rate',
 'Mental health providers: Mental Health Provider Ratio',
 'Preventable hospital stays: Preventable Hospitalization Rate',
 'Mammography screening: % With Annual Mammogram',
 'Flu vaccinations: % Vaccinated',
 'High school graduation: Cohort Size',
 'High school graduation: High School Graduation Rate',
 'Some college: # Some College',
 'Some college: Population',
 'Some college: % Some College',
 'Unemployment: # Unemployed',
 'Unemployment: Labor Force',
 'Unemployment: % Unemployed',
 'Children in poverty: % Children in Poverty',
 'Income inequality: 80th Percentile Income',
 'Income inequality: 20th Percentile Income',
 'Income inequality: Income Ratio',
 'Children in single-parent households: # Single-Parent Households',
 'Children in single-parent households: # Households',
 'Children in single-parent households: % Single-Parent Households',
 'Social associations: # Associations',
 'Social associations: Social Association Rate',
 'Violent crime: Annual Average Violent Crimes',
 'Violent crime: Violent Crime Rate',
 'Injury deaths: # Injury Deaths',
 'Injury deaths: Injury Death Rate',
 'Air pollution - particulate matter: Average Daily PM2.5',
 'Drinking water violations: Presence of Water Violation',
 'Severe housing problems: % Severe Housing Problems',
 'Severe housing problems: Severe Housing Cost Burden',
 'Severe housing problems: Overcrowding',
 'Severe housing problems: Inadequate Facilities',
 'Driving alone to work: % Drive Alone to Work',
 'Long commute - driving alone: # Workers who Drive Alone',
 'Long commute - driving alone: % Long Commute - Drives Alone',
 'Life expectancy: Life Expectancy',
 'Premature age-adjusted mortality: # Deaths',
 'Premature age-adjusted mortality: Age-Adjusted Death Rate',
 'Child mortality: # Deaths',
 'Child mortality: Child Mortality Rate',
 'Infant mortality: # Deaths',
 'Infant mortality: Infant Mortality Rate',
 'Frequent physical distress: % Frequent Physical Distress',
 'Frequent mental distress: % Frequent Mental Distress',
 'Diabetes prevalence: % Adults with Diabetes',
 'HIV prevalence: # HIV Cases',
 'HIV prevalence: HIV Prevalence Rate',
 'Food insecurity: # Food Insecure',
 'Food insecurity: % Food Insecure',
 'Limited access to healthy foods: # Limited Access',
 'Limited access to healthy foods: % Limited Access to Healthy Foods',
 'Drug overdose deaths: # Drug Overdose Deaths',
 'Drug overdose deaths: Drug Overdose Mortality Rate',
 'Motor vehicle crash deaths: # Motor Vehicle Deaths',
 'Motor vehicle crash deaths: Motor Vehicle Mortality Rate',
 'Insufficient sleep: % Insufficient Sleep',
 'Uninsured adults: # Uninsured',
 'Uninsured adults: % Uninsured',
 'Uninsured children: # Uninsured',
 'Uninsured children: % Uninsured',
 'Other primary care providers: Other Primary Care Provider Rate',
 'Other primary care providers: Other Primary Care Provider Ratio',
 'Disconnected youth: % Disconnected Youth',
 'Reading scores: Average Grade Performance',
 'Math scores: Average Grade Performance',
 'Median household income: Median Household Income',
 'Children eligible for free or reduced price lunch: % Enrolled in Free or Reduced Lunch',
 'Residential segregation - Black/White: Segregation index',
 'Residential segregation - non-White/White: Segregation Index',
 'Homicides: Homicide Rate',
 'Suicides: # Deaths',
 'Suicides: Crude Rate',
 'Firearm fatalities: # Firearm Fatalities',
 'Firearm fatalities: Firearm Fatalities Rate',
 'Juvenile arrests: Non-Petitioned Cases',
 'Juvenile arrests: Petitioned Cases',
 'Juvenile arrests: Denominator',
 'Juvenile arrests: Juvenile Arrest Rate',
 'Traffic volume: Average Traffic Volume per Meter of Major Roadways',
 'Homeownership: # Homeowners',
 'Homeownership: % Homeowners',
 'Severe housing cost burden: # Households with Severe Cost Burden',
 'Severe housing cost burden: % Severe Housing Cost Burden',
 'Demographics: Population',
 'Demographics: % less than 18 years of age',
 'Demographics: % 65 and over',
 'Demographics: # Black',
 'Demographics: % Black',
 'Demographics: # American Indian & Alaska Native',
 'Demographics: % American Indian & Alaska Native',
 'Demographics: # Asian',
 'Demographics: % Asian',
 'Demographics: # Native Hawaiian/Other Pacific Islander',
 'Demographics: % Native Hawaiian/Other Pacific Islander',
 'Demographics: # Hispanic',
 'Demographics: % Hispanic',
 'Demographics: # Non-Hispanic White',
 'Demographics: % Non-Hispanic White',
 'Demographics: # Not Proficient in English',
 'Demographics: % Not Proficient in English',
 'Demographics: % Female',
 'Demographics: # Rural',
 'Demographics: % Rural',
 'democrat_score', # percent of voters who voted for Hillary Clinton in 2016
 'poverty_percent', # percent of population under poverty line
 'median_income',
 'population',
 'popultion_density',
 'lat', #centroid
 'lon', #centroid
 'religious_adherents', #number of religious adherents
 'hospital_beds', #number of hospital beds
 'diffusion' # (number of communters into and out of county)/(population of county)]
 ```
