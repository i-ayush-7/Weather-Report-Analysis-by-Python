# Weather Report Analysis by Python

This Jupyter Notebook presents an **Exploratory Data Analysis (EDA)** of a **Weather Report Dataset**, which is a time-series dataset containing per-hour weather information for a particular location.

---

## Data Summary

The initial data exploration reveals the following:

* **Dataset Size:** The dataset has **8,784 rows** and **8 columns**. This suggests the data covers every hour of a full year ($24 \text{ hours} \times 365 \text{ days} = 8,760$ hours, so the dataset may contain data for a leap year or a slightly longer period).
* **Columns:** The original columns are 'Date/Time', 'Temp\_C', 'Dew Point Temp\_C', 'Rel Hum\_%', 'Wind Speed\_km/h', 'Visibility\_km', 'Press\_kPa', and 'Weather'.
* **Data Types and Missing Values:** The `Date/Time` column has been successfully converted to a datetime type. Crucially, **there are no missing values (nulls)** in the original columns.
* **Feature Engineering:** A new column, **'Month\_Name'**, was added for time-based analysis. A **'Season'** column was also created to group the data into Fall, Spring, Summer, and Winter.

---

## Key Analysis Findings

The exploratory analysis answered several key questions about the weather data:

### 1. Average Temperature by Month
The analysis shows the monthly average temperature, clearly indicating the seasonal temperature cycle:

| Month | Average Temperature ($^\circ\text{C}$) |
| :--- | :--- |
| **January** | **-7.37** |
| **February** | **-4.23** |
| **July** | **22.79** |
| **August** | **22.28** |

January is the coldest month with an average temperature of $-7.37^\circ\text{C}$, and July is the warmest with an average of $22.79^\circ\text{C}$.

### 2. Temperature Over Time
A **line plot** of 'Temp\_C' over the entire 'Date/Time' index visually confirms the temperature fluctuations throughout the year, with clear peaks in the summer months and troughs in the winter months.

### 3. Average Weather Conditions by Season
The seasonal summary provides a broad overview of conditions:

| Season | Average Temperature ($^\circ\text{C}$) | Average Relative Humidity ($\%$) | Average Wind Speed ($\text{km/h}$) |
| :--- | :--- | :--- | :--- |
| **Fall** | 9.47 | 72.33 | 14.53 |
| **Spring** | 8.81 | 60.98 | 14.88 |
| **Summer** | 21.75 | 63.57 | 13.49 |
| **Winter** | -4.98 | 72.97 | **16.90** |

**Winter** is the coldest and windiest season, while **Summer** is the warmest and has the lowest average humidity.

### 4. Average Temperature vs. Humidity by Weather Condition
A **bar chart** compares the average temperature and relative humidity for different weather types:
* Weather conditions like **'Fog'**, **'Freezing Drizzle, Fog'**, and **'Snow, Fog'** are associated with the highest average relative humidity (above 90%), which is consistent with the presence of fog.
* The highest average temperatures are associated with conditions like **'Clear'** and **'Mainly Clear'** and the lowest with conditions like **'Snow'** and **'Freezing Rain'**.

## Project By: Ayush Shukla

### 5. Hottest Hour of the Day
A **line plot** of the average temperature by hour shows a diurnal cycle:
* The temperature is lowest around **4 AM**.
* The temperature is highest, meaning the **hottest hour**, around **3 PM (15:00)**.

### 6. Day vs. Night Temperature Analysis
A **bar chart** comparing average temperature during 'Day' (6 AM to 6 PM) and 'Night' (6 PM to 6 AM) clearly shows that the **Daytime** average temperature is higher than the Nighttime average.

---

## Project Conclusion

The analysis effectively leverages the time-series nature of the data to provide a comprehensive look at the local weather patterns, successfully quantifying and visualizing how **temperature, humidity, wind speed, and visibility** vary over months, seasons, and hours of the day. The findings confirm expected seasonal and diurnal cycles and provide specific metrics for various weather phenomena.
