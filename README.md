-------------- Drought Data --------------

All of the Jupyter notebooks run with python. Suggested is to use VSC and open
the replication folder with "open Folder". This should set the wd correctly.
Then Proceed as follows:

Open the Jupyter Notebook agri_stress_data and run the file to produce the agri_stress variable.
File is in drought_data_output: agri_stress_long.csv / agri_stress_pivoted.csv

Download the raw SPEI observation from the Global Drought observatory.
They are .tif files and very large. They are saved locally and downloadable on request.
Open the Jupyter Notebook data_extraction.ipynb and run it.
This aggregates the SPEI observations (Pixels) By District and Dekad
Output is spei3_hf_raw.csv in the drought_data_output folder

Run spei_processing.ipynb. This creates the spei_yearly_master.csv
This contains all variables for analysis.

All these outputs are then used to run the analysis.

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




-------------- Full Analysis --------------

Find and run "DEV_Analysis.rmd". Note that you will have to set the directory.
Alternatively, you can find "DEV_Analysis.rmd" which is just the knitted-to-pdf
version of this code. In it is all our relevant analyses, and is the code file
which creates all our figures. Set "latex_format" = TRUE in the setup chunk
and run the code to save the figures. Set "latex_format" = FALSE in the setup 
chunk in order to just run the code in the console.
Note that there is an "Data Choice Selection" chunk, where by simply setting 
certain settings to "TRUE", you can run all the regressions according to certain 
criterions such as: dependent variables in logs, excluding Yerevan city, restricting 
the sample to more rural districts, restricting the sample to districts with higher
poverty rates, and including up to 6 lags.



-------------- Appendix --------------

The "DEV_appendix.rmd" file essentially is a cleaned-up, shortened version
of the full analysis file with the plots and tables not present in the
actual paper. It also includes more detailed explanations of the data.



