# (Core) Preparing Time Series from Wide-Form Data

# Tasks

You will be working with Zillow's publicly available Zillow House Value Index (ZHVI) https://www.zillow.com/research/data/

- Specifically, you will be using the Home Value data set for:
    - Data Type = "ZHVI All Homes (SFR+Condo/Coop) - Time Series - Smoothed - Seasonally Adjusted"
    - Geography = "City"
- We have already downloaded the file for you and uploaded it to Google Drive.

- Direct URL (for Pandas): https://docs.google.com/spreadsheets/d/e/2PACX-1vQN3Ksa9szQuO4G1-msXWAp17KtVHQCBnuEieu_auu1wSiBf3-krHusIx5VBMkihxj-KZLBosDIGEyR/pub?output=csv



## Part 1

- First, you will prepare the dataset for time series analysis:
    - Load in the Zillow Home Value Index dataframe.

- Filter the 4 largest cities into a new dataframe.
    - Tip: the "SizeRank" column has already ranked the cities by size. The larger the city, the smaller the rank value.
        - Therefore the 4 largest cities would have rank values of [0,1,2,3]

- Melt the data to long-form and prepare it for time series analysis.
    - Convert the melted dates into datetime datatype.
    - Make the datetime column the index.
- Resample the dataframe as monthly frequency, grouped by City.

## Part 2

- Once you've prepared the dataframe with the time series data for the 4 largest cities:
    - Plot the home values for all 4 cities. (Hint: use unstack)
        - Make sure to add a title and axis labels.
        - Reformat the y-axis ticks to use thousands of dollars with a "K" at the end. (e.g. "200K, 400K, etc")
            - Hint: use the FuncFormatter from matplotlib.

- Answer the following 2 questions using pandas:

- 1) Which City had the highest Typical Home Value at the end of 2008? Which had the least?
    - Hint: You can use the unstacked dataframe or use pd.IndexSlice with the multiindex. 
- 2) How much did the home values change from November 2008 to December 2008 (in dollars)?
    - Hint: you can use .diff() to calculate the change in values
  ## Q1
- 1) Which City had the highest Typical Home Value at the end of 2008? Which had the least?
- Hint: You can use the unstacked dataframe or use pd.IndexSlice with the multiindex.
 - A: - the highest value was in new york  for $510309
 - the lowest value was in houston for    $131283

  ## Q2
- 2) How much did the home values change from November 2008 to December 2008 (in dollars)?
    - Hint: you can use .diff() to calculate the change in values
 
    - ![image](https://github.com/clovestad/Preparing-Time-Series-from-Wide-Form-Data/assets/103072823/19121ee8-457f-4b57-833d-c1adae8b7bb9)
