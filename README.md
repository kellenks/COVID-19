# COVID-19

### SIR Isaac Newton's public repo for COVID-19 Math Modeling Contest

#### Documentation
We provide documentation to supplement our paper submission and to share our methodology. 
* The raw data is available from the xlsx or csv files, but all notebooks should be run to generate needed pickle files
* To use, clone and run notebooks in the following order:
  1) Base_Commuting_Matrix
  2) Adjusted_Commuter_Flows
  3) Case_Death_Estimations
  4) Disease_Spread_Algorithm
  5) Results, Validation
* Code is lightly commented. Please contact ksandvi@emory.edu if you have any questions




In an effort to maximize collaboration, we are happy to share some data we think could be helpful.


#### Data

* #### Parsed Google mobility data: mobile phone tracking by county (FIPS code)
  * Great for social distancing metrics
  * Trends as of March 29 and April 5
  * Raw: Empty/Null values for non-reported measures
  * Filled: Empty/Null county-level values replaced by state-level measures
  * Excel and Pickle files
  * Original PDF's can be found by searching for "Google Mobility Reports"
  * Contact Kellen at ksandvi@emory.edu for Python notebook used for PDF-TXT conversion and parsing
  * Note: A much more exhaustive CSV file of daily mobility tracking is now available on the webpage
  
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
 
