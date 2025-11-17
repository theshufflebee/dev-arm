-------------- Drought Data --------------




-------------- Final Data --------------
Find and run "DEV_data.rmd" in R. Note that you will have to set the directory.
This code imports all the household, agriculture, and drought data and cleans it
according to our needs. Alternatively, you can find "DEV_data.pdf" which is just
the knitted-to-pdf version of this code.
It then saves it as 4 key datasets: 
-final_data.Rdata  -> District level data that we use for our analysis.
-final_data_quartiles.Rdata
-final_data_deciles.Rdata
-final_data_household.Rdata




-------------- Analysis --------------
Find and run "DEV_Analysis.rmd". Note that you will have to set the directory.
Alternatively, you can find "DEV_Analysis.rmd" which is just the knitted-to-pdf
version of this code. In it is all our relevant analyses.
Note that there is an "Data Choice Selection" chunk, where by simply setting 
certain settings to "TRUE", you can run all the regressions according to certain 
criterions such as: dependent variables in logs, excluding Yerevan city, restricting 
the sample to more rural districts, restricting the sample to districts with higher
poverty rates, and including up to 6 lags.


