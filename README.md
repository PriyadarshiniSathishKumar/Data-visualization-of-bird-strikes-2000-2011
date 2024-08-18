# Data-visualization-of-bird-strikes-2000-2011
This Python code analyzes a dataset presumably containing information about bird strikes involving airplanes. Here's a breakdown of the steps involved:

# 1. Import Libraries:

pandas: Used for data manipulation and analysis.
numpy: Used for numerical operations (potentially for error handling).
matplotlib.pyplot: Used for creating basic plots.
seaborn: A library built on top of matplotlib for creating more visually appealing statistical graphics.

# 2. Data Loading and Cleaning:

Reads the Excel file "Bird Strikes data.xlsx - Bird Strikes.csv" using pd.read_csv.
Creates a pandas DataFrame named df from the loaded data.
Prints the first few rows of the data using df.head().

# 3. Bird Strikes Over the Years:

Converts the 'FlightDate' column to datetime format using pd.to_datetime to enable time-based analysis.
Extracts the year from the 'FlightDate' column and creates a new column named 'Year'.
Creates a bar chart using plt.bar to visualize the total number of bird strikes for each year.

# 4. Yearly Bird Strikes in the US (Excluding Non-US States):

Filters the data to exclude rows where the 'Origin State' is in a list of non-US states and territories using df[~df['Origin State'].isin(non_us_states)].
Creates a count plot using seaborn.countplot to visualize the number of bird strikes in the US for each year, categorized by the origin state.

# 5. Top 10 US Airlines with Most Bird Strikes:

Filters the data to include only rows with a valid airline name in the 'Aircraft: Airline/Operator' column (presumably containing airlines) using .notna() and string filtering.
Identifies the top 10 US airlines with the most bird strikes by counting occurrences in the filtered data and selecting the n largest using .value_counts().nlargest(10).
Creates a bar chart using seaborn.barplot to visualize the results.

# 6. Top 50 Airports with Most Bird Strikes:

Counts the occurrences of bird strikes at each airport name in the 'Airport: Name' column using .value_counts().
Selects the top 50 airports with the most bird strikes using .nlargest(50).
Creates a bar chart using seaborn.barplot to visualize the results.

# 7. Yearly Cost of Bird Strikes:

Creates a line plot using seaborn.lineplot to visualize the total cost incurred due to bird strikes for each year.
Uses the sum estimator to calculate the total cost for each year and disables confidence intervals with ci=None.
Applies a logarithmic scale on the y-axis using plt.yscale('log') to better represent potentially large variations in cost.

# 8. Bird Strikes Across Flight Phases:

Creates a count plot using seaborn.countplot to visualize the distribution of bird strikes across different flight phases (e.g., takeoff, landing, etc.) based on the 'When: Phase of flight' column.
Orders the categories based on their frequency using .value_counts().index.
Rotates the x-axis labels for better readability using plt.xticks(rotation=45, ha='right').

# 9. Altitude of Airplanes at Bird Strike:

Converts the 'Feet above ground' column to numeric format using pd.to_numeric (handling potential errors with errors='coerce').
Creates a bar chart using plt.bar to visualize the number of bird strikes at different altitudes.

# 10. Bird Strikes by Flight Phase and Altitude:

Creates a box plot using seaborn.boxplot to visualize the average altitude of airplanes in different flight phases at the time of the bird strike.
Uses hue to categorize the box plots by flight phase.

# 11. Effect of Bird Strikes on Flights:

Creates a count plot using seaborn.countplot to visualize the number of bird strikes categorized by the impact on the flight based on the 'Effect: Impact to flight' column.
Orders the categories based on their frequency.

# 12. Effect of Bird Strikes at Different Altitudes:

Creates a count plot using seaborn.countplot to visualize the distribution of bird strikes categorized by the impact on the flight, but without separating them by flight phase.

# 13. Effect of Bird Strikes and Pilot Warning:

Creates a count plot using seaborn.countplot

# Colab Link
https://colab.research.google.com/drive/1Qqd0ZYz0w7cgFe7g3xl9iQ0Hib0WqL8h?usp=sharing

![image](https://github.com/user-attachments/assets/d9917542-4d56-4cd1-8862-472ac2c57a2c)

![image](https://github.com/user-attachments/assets/0ec8aa34-c7d1-48db-a09b-e1761a4eab0e)

![image](https://github.com/user-attachments/assets/720e91b8-5522-411d-b3f8-07bec25737e9)

![image](https://github.com/user-attachments/assets/913d9f0c-c950-4082-8fc4-b3d2170f5dac)

![image](https://github.com/user-attachments/assets/4fe913ef-d92e-4f26-81b2-cc34ce9b0c86)

![image](https://github.com/user-attachments/assets/311f3f86-d1c5-464c-8cc8-3a44fe16c193)





