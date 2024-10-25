
# NYC Taxi Trip Data Analysis

## Overview

This project is a part of the Big Data Technologies course at Macquarie University. The analysis focuses on New York City's yellow taxi trip data from January, March, and June 2023. The goal is to explore, clean, and analyze the data to uncover trends, derive meaningful insights, and provide actionable recommendations.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Key Tasks](#key-tasks)
  - [Data Loading](#data-loading)
  - [Data Exploration and Pre-processing](#data-exploration-and-pre-processing)
  - [Featurization](#featurization)
  - [Data Analysis](#data-analysis)
  - [Conclusion](#conclusion)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Data Dictionary](#data-dictionary)
- [Results and Visualizations](#results-and-visualizations)
- [Video Demonstration](#video-demonstration)
- [Contributors](#contributors)

## Dataset

The dataset includes Yellow Taxi Trip records from New York City for the months of January, March, and June 2023. It contains detailed information about each trip, such as:
- Pick-up and drop-off dates and times.
- Trip distances.
- Itemized fare amounts.
- Payment methods.
- Passenger counts.

You can access the dataset from the following links:
- [January 2023](https://d37ci6vzurychx.cloudfront.net/trip-data/yellow_tripdata_2023-01.parquet)
- [March 2023](https://d37ci6vzurychx.cloudfront.net/trip-data/yellow_tripdata_2023-03.parquet)
- [June 2023](https://d37ci6vzurychx.cloudfront.net/trip-data/yellow_tripdata_2023-06.parquet)

Supplementary data such as taxi zone maps and lookup tables are also used in this analysis.

## Key Tasks

### Data Loading
- Load NYC taxi trip data for January, March, and June 2023 using pandas.
- Compare and identify trends between the three months.

### Data Exploration and Pre-processing
- Handle missing values and noisy data.
- Identify and explain highly correlated columns in the dataset.

### Featurization
- Create new features such as:
  - Rush-hour flag.
  - Trip complexity score based on actual vs. straight-line distance.
- Calculate the frequency of pick-ups and drop-offs in each taxi zone.

### Data Analysis
- Answer specific questions such as:
  - Ranking of vendors by popularity.
  - Determining peak travel hours.
  - Calculating average trip distances and passenger counts for weekdays and weekends.
  - Investigating correlations between fare amount, tips, and the number of passengers.

### Conclusion
- Summarize the findings and challenges encountered during the analysis.
- Suggest possible next steps or further analyses.

## Requirements

- Python 3.x
- Jupyter Notebook
- Libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`
  - `geopandas` (for spatial analysis)
  - `scikit-learn` (for additional data processing)

You can install the required libraries using the following command:

```bash
pip install -r requirements.txt
```

## Installation

1. Clone the repository:

```bash
git clone https://github.com/your-username/nyc-taxi-analysis.git
```

2. Navigate to the project directory:

```bash
cd nyc-taxi-analysis
```

3. Install the required libraries:

```bash
pip install -r requirements.txt
```

4. Open the Jupyter Notebook:

```bash
jupyter notebook BigDataAssignment3.ipynb
```

## Usage

1. Download the dataset from the provided links and place them in the `data/` directory.
2. Open the Jupyter Notebook and run the cells to perform the analysis.

## Data Dictionary

The yellow taxi trip data includes various fields, as outlined below:

| **Field Name**          | **Description**                                                                                          |
|-------------------------|----------------------------------------------------------------------------------------------------------|
| VendorID                | A code indicating the TPEP provider (1=Creative Mobile Technologies, LLC; 2=VeriFone Inc.)               |
| tpep_pickup_datetime     | The date and time when the meter was engaged.                                                            |
| tpep_dropoff_datetime    | The date and time when the meter was disengaged.                                                         |
| Passenger_count          | The number of passengers in the vehicle (driver-entered value).                                          |
| Trip_distance            | The elapsed trip distance in miles reported by the taximeter.                                            |
| PULocationID             | TLC Taxi Zone in which the taximeter was engaged.                                                        |
| DOLocationID             | TLC Taxi Zone in which the taximeter was disengaged.                                                     |
| RateCodeID               | Final rate code (1=Standard, 2=JFK, 3=Newark, 4=Nassau/Westchester, 5=Negotiated fare, 6=Group ride).   |
| Store_and_fwd_flag       | Whether the trip record was held in vehicle memory before sending to the vendor (Y=Yes, N=No).           |
| Payment_type             | How the passenger paid (1=Credit card, 2=Cash, 3=No charge, 4=Dispute, 5=Unknown, 6=Voided trip).       |
| Fare_amount              | Time-and-distance fare calculated by the meter.                                                          |
| Extra                    | Miscellaneous extras, such as rush hour/overnight charges.                                               |
| MTA_tax                  | $0.50 MTA tax automatically triggered.                                                                  |
| Improvement_surcharge    | $0.30 improvement surcharge levied at flag drop.                                                         |
| Tip_amount               | Tip amount (automatically populated for credit card tips, cash tips not included).                       |
| Tolls_amount             | Total amount of all tolls paid.                                                                          |
| Total_amount             | Total amount charged to passengers, excluding cash tips.                                                 |
| Congestion_Surcharge     | Total collected for NYS congestion surcharge.                                                           |
| Airport_fee              | $1.25 pick-up fee at LaGuardia and JFK airports.                                                         |

For more details, refer to the [NYC TLC Data Dictionary](https://www.nyc.gov/assets/tlc/downloads/pdf/trip_record_user_guide.pdf).

## Results and Visualizations

- Vendor popularity rankings.
- Peak travel hours analysis.
- Correlation between fare and tips.
- Visualizations of trip distribution by taxi zone.

Images generated during the analysis can be found in the `visualizations/` folder.

## Video Demonstration

A video demonstrating the code and analysis can be viewed on YouTube at the following link:

[YouTube Video Link](https://studio.youtube.com/video/7f5JwwQUvGQ/edit)

## Contributors

- **Suresh Ghatani**
