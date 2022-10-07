# 2022-Statistical-Risk-Assessment

Replication files for the 2022 edition of USHMM's statistical risk assessment. 

You should use the data stored in the repo, "prepared2021predictors-2022-09-30.csv". This is preferable to regenerating the data yourself, since doing so requires a host of ancillary files, pulling data from online sources, etc. We nevertheless include a folder containing the R files used to make the data (Make Data), for reference and replicability. Within this folder:

- "Adding in new data" is an R Markdown file that appends data for each country in 2021 to the prepared data through 2020.
- The input folder contains the data prepared through 2020 from last year's analysis: "prepared2020predictors-2021-08-25.csv"
- The output folder contains the prepared data, updated through 2020: "prepared2021predictors-2022-09-30.csv"
- The output folder also contains an updated file with just the mass killing variables: "mkl_data.csv"

The main files of interest are in the Modelling folder. 

- "run model" is an R Markdown file that takes the latest data ("prepared2021predictors-2022-09-30.csv") and generates forecasts. It allows you to input a vector of base years, from which you would like to generate one and two-year forecasts. The most relevant forecasts have been included in the results folder, generated from base year 2021, predicting outcomes in the next year (2022) and in the next two years (2022 and 2023). Note that if you choose to run the model for base years earlier than 2016, there is some missingness in the data that will prevent you from getting predicted probabilities for all 162 of the countries.
- "base2021-run-2022-09-30" and "base2021-coeffs-run-2022-09-30" are the outputs of the "run model" file. The former file shows the predicted probabilities for each country, and the latter shows the weights for each of the predictors selected. 
