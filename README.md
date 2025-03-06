
# Dose Response Curve and LD50 Analysis

## Description

This R script generates a dose-response curve based on survival rates at 24 hours after bacterial injection. It also calculates the LD50 (lethal dose for 50% of individuals) and its standard error. In addition, the virulence of the two bacterial strains can be compared by running a likelihood ratio test to determine if the dose-response curves are significantly different.



## Installation

Ensure that you have R installed. Then, install the required packages:

`install.packages("MASS")`

`install.packages("tidyverse")`



## Data Preparation

Before running the analysis, prepare a CSV file with the following columns:

  * strain: Strain administered
  
  * bacterial_dose: Number of bacteria administered
  
  * time: Time when survival rate was checked
  
  * surv: Number of surviving individuals
  
  * total: Total number of individuals in the experiment
  
  * experimenter: Name of the experimenter
  
  * exp_date: Date of the experiment


#### Example Input Data (CSV)
Ensure your input file is structured as follows:

| strain | bacterial_dose | time | surv | total | experimenter | exp_date |
|--------|----------------|------|------|-------|--------------|----------|
| A      | 10000          | 24   | 0    | 5     | X            | 20250306 |
| A      | 1000           | 24   | 3    | 5     | X            | 20250306 |
| A      | 100            | 24   | 5    | 5     | X            | 20250306 |

Save the file as data.csv.



## Usage

### 1. Running the Analysis

Modify the analyze date in the script and then run the entire script in the R console.

### 2. Dose Response Curve and LD50 Calculation

Enter the code “Dose response curve and LD50” into the R console and select the CSV file of the bacterial strain you wish to analyze.
A png file of the Dose response curve and a CSV file with the LD50 will then be automatically saved.
The last line of the R console output shows the standard error of the LD50.

##### NOTES
If you select multiple CSV files for multiple strains when entering data, you can display multiple dose response curves on a single graph. Note that the standard error calculation can only be performed when one bacterial strain is selected.


#### Example Output Files

<ins>LD50_results.csv</ins>

| time | strain | LD50 | max_dose | min_dose |
|------|--------|------|----------|----------|
| 24   | A      | 800  | 10000    | 100      |

<ins>Dose-Response Curve Graph</ins>

The following graph is automatically generated as curve.png:![MRSA8 横軸固定](https://github.com/user-attachments/assets/4da54f84-4c72-44c1-9ee5-73ef82a1bb1c)




### 3. Likelihood Ratio Test

Enter the “Likelihood ratio test” code into the R console and select the CSV files of the two bacterial strains you wish to compare.
You will see the calculated p-value in the last line of the R console output.



## License

This project is licensed under the GPL-3.0 License - see the [LICENSE](LICENSE) file for details.


## Author

Name: Chikara Kaito

GitHub: chikarakaito
