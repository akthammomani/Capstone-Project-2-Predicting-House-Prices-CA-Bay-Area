# Data Wrangling: Predicting House prices North California

![Data_Wrangling_hh](https://user-images.githubusercontent.com/67468718/104858187-6ec96180-58d2-11eb-8e6e-f110ef5193fb.JPG)

## 1. Introduction:

The Data wrangling step focuses on collecting our data, organizing it, and making sure it's well defined. For our project we have collected below datasets to have a good foundation to build a Machine Learning model where we can provide a good estimate of house prices in North California:

  1. Main Dataset: Source www.redfin.com:
    * Obtained sold houses from Dec 2019-Dec 2020.
    * The sold houses located in North California distributed between 49 cities and 94 Zip Codes.
    * Data has 8,790 Observations and 27 Variables.

2. Adding Median Income per Zip code:
    * Source: http://www.usa.com/rank/california-state--median-household-income--zip-code-rank.htm and since the data from 2010-2014, and according to              
      https://www.statista.com/statistics --> the median Income in California has grown by 6.36% we’ll use this % to adjust this Dataset YoY.
      
3. Adding Hotness score (0-100) to refelect the demand and supply per zip code:
    * Source: https://www.realtor.com/research/data/
      
4. Adding Public School per zip code:
    * Source: https://hifld-geoplatform.opendata.arcgis.com/datasets/87376bdb0cb3490cbda39935626f6604_0
    
5. Adding GreatSchools Rating to reflect Schools rating in all the selected 47 cities in North California:
    * Source: GreatSchools.org API https://www.greatschools.org/api/request-api-key

6. Adding Shoping and Mall centers in CA per city:
    * Source: https://en.wikipedia.org/wiki/List_of_shopping_malls_in_California
    
7. Adding Universities and colleges list in CA per city:
    * Source: http://www.free-4u.com/Colleges/California-Colleges.html
    
8. Adding BART (Bay Area Rapid Transit) stations with parking (Y/N) per zip code in North California:
    * Source: https://www.bart.gov/stations
    
9. We have 8 Datasets to support this project, so Data cleaning & Wrangling will be needed:
    * Clean NANs, duplicate values, wrong values and removing insignificant columns.
    * Merging and concatenation will be needed.
    * The GreatSchools API is a REST-based web service: will need to use Python Packages: requests, xml.etree.ElementTree and glob:
         - requests: To request the data from GreatSchools API
         - xml.etree.ElementTree module : to implement a simple and efficient API for parsing and creating XML data.
         - glob: to concatenate all the API output in one final DataFrame.
    
## 2. Data Wrangling Objectives:    
    
We have 8 Datasets to support this project, so we'll focus in below:
   * Clean NANs, duplicate values, wrong values and removing insignificant columns.
   * Renaming Column labels.   
   * Correct datatypes.
   * Merging and concatenation will be needed.
   * The GreatSchools API is a REST-based web service (**Completed**): will need to use Python Packages: requests, xml.etree.ElementTree and glob:
        - requests: To request the data from GreatSchools API
        - xml.etree.ElementTree module : to implement a simple and efficient API for parsing and creating XML data.
        - glob: to concatenate all the API output in one final DataFrame.
   * **Data Wrangling layout and the Initial DataFrame structure**: at this stage we'll not be overzealous in our cleaning because we need to explore the data to better understand it in the exploratory data analysis Stage (EDA) where we'll provide the final datframe Structure.

![Data_Wrangling_initial](https://user-images.githubusercontent.com/67468718/103534919-a7822900-4e44-11eb-9f68-c6124e66bbd1.JPG)

## 3. Merging DataFrames:   

Data Frames to be Merged: 
   1. **df_main_sold_houses_final** is the main DataFrame
   2. school_df
   3. df_bart_final
   4. df_malls_final
   5. df_median_income
   6. housing_final_df_v1
   7. df_universities_final
   
   ![Data_Wrangling](https://user-images.githubusercontent.com/67468718/103494183-52b1c480-4dea-11eb-8673-612746b0d229.JPG)
   
## 4. Target Features:      

![Features](https://user-images.githubusercontent.com/67468718/103541349-2892ed80-4e50-11eb-95ee-0be69ea98781.JPG)
