# ETL-project
A basic ETL project that included transforming the list of world's largest banks by market cap with data represented in  USD to GBP. 

# EXTRACTION

# Extraction of the table:
Data was extracted from wikipedia 
(link = https://en.wikipedia.org/wiki/List_of_largest_banks?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMDeveloperSkillsNetworkPY0221ENSkillsNetwork23455645-2022-01-01)
Table named : "By Market Capitilization" was used and using "requests","pandas" and "beautiful soup" it was stored in a "json file" called "bank-market-cap.json"
The json file was then converted into a dataframe and called "extracted_data" 

# Extraction of the currency exchange rates:
Using an API (link = https://exchangeratesapi.io/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMDeveloperSkillsNetworkPY0221ENSkillsNetwork23455645-2022-01-01)

Exchange rates were extracted and stored in a dataframe using pandas and later on the exchange rate of GBP was acquired and saved as a "float" in a variable called
"exchange_rate"

# TRANSFORM

The data to be transform was the column called ""Market Cap (US$ Billion)" which had the values represented in USD$ in the "extracted_data" dataframe was transformed into GBP by multiplying the "exchange_rate" and the specified column [Market Cap (US$ Billion)] of "extracted_data"
The column was renamed from "Market Cap (US$ Billion)" to "Market Cap (GBP Billion)" 


# LOADING

A load function was made to load the transformed data into a csv file

# Logging

A log file was made to ensure all the ETL process worked

