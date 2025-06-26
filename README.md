# Weather-Data-Analysis-and-Visualization
Weather Data Analysis and Visualization – Iran 2025

This project demonstrates a complete workflow for cleaning, analyzing,
and visualizing historical weather data—specifically maximum and minimum daily temperatures—for selected cities in Iran.
The process includes data preprocessing, handling missing values,
unit conversion, slicing datasets, and comparative line plotting using Matplotlib.
Project Structure.

	....It must be executed in order....

data_cleaning_1.py— Data Cleaning and Preparation:
•	Reads raw data from weather_orginal_file.csv.
•	Removes unnecessary columns and exports a simplified version as weather_change.csv.
•	Handles missing values:
o	Drops rows where all values are NaN.
o	Fills missing TMAX and TMIN values with their respective mean.
o	Converts temperature units from Fahrenheit to Celsius.
•	Outputs cleaned datasets:
o	weather_cleaned_TMAX.csv
o	weather_cleaned_TMIN.csv
•	Extracts the first 75 records into a new file for analysis: weather_city_sanandaj.csv.

data_cleaning_2.py— Tehran Dataset Cleanup:
•	Loads data from city_tehran.csv.
•	Computes and fills missing values for TMAX and TMIN using column-wise averages.
•	Converts temperatures to Celsius.
•	Outputs cleaned file as city_tehran_TMAX_TMIN.csv.

show_temp_high_low_sanandaj.py— Sanandaj Temperature Line Plot:
•	Loads cleaned weather_city_sanandaj.csv.
•	Parses TMAX and TMIN values and timestamps.
•	Checks for missing or corrupted temperature data.
•	Generates a line chart for daily high and low temperatures in Sanandaj using matplotlib.

show_temp_high_low_tehran.py— Tehran Temperature Line Plot:
•	Loads data from city_tehran_TMAX_TMIN.csv.
•	Extracts daily highs and lows with error handling.
•	Creates a comparative line chart similar to file 3.py for Tehran.

comparing_two_cities.py— Tehran vs. Sanandaj High Temp Comparison:
•	Loads both cleaned datasets (city_tehran_TMAX_TMIN.csv and weather_city_sanandaj.csv).
•	Extracts and parses date-wise maximum temperatures from each.
•	Displays a side-by-side line chart comparing daily high temperatures for the year 2025 between Tehran and Sanandaj.

Technologies & Libraries Used:
•	Python 3.x
•	csv & datetime – Native modules for parsing and formatting
•	pandas – Efficient data handling and transformation
•	matplotlib – Visualization of weather trends using line plots

Features:
•	End-to-end pipeline from raw .csv files to cleaned, enriched, and sliced datasets
•	Handling of missing and empty values with contextual replacement
•	Conversion of Fahrenheit to Celsius
•	Dynamic plotting of temperature trends by city
•	Visual comparison of temperature variation across cities
Output Visuals
The following plots are generated:
•	Daily High/Low Temperatures – Sanandaj (2025)
•	Daily High/Low Temperatures – Tehran (2025)
•	Daily High Comparison – Tehran vs. Sanandaj

Each figure is rendered with bmh style and includes formatted x-axis dates and Celsius labels.
 How to Run:
1.	Make sure you have Python and the following libraries installed
pip install pandas matplotlib 

2.	Place your raw data CSV files (weather_orginal_file.csv and city_tehran.csv) in the same directory.
3.	Run 1.py to generate cleaned and trimmed datasets.
4.	Execute 2.py to process Tehran data.
5.	Run 3.py, 4.py, and 5.py to generate visual charts.

Notes:
•	Dates are expected in ISO format (YYYY-MM-DD).
•	Temperature calculations assume standard Fahrenheit input.
•	Plots are set to display interactively. Ensure your environment supports GUI rendering or switch to plt.savefig() for static output.

