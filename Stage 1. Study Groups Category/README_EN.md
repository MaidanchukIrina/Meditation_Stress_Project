Description of the Analysis Stage: Creating a Gantt Chart for Study Duration and Frequency Analysis
At this stage, a Gantt chart was created to visualize the periods during which studies were conducted, allowing for a clear view of the chronological sequence and duration of each study. The primary goal of this analysis was to obtain a visual representation of the study timelines and identify periods of high research activity.

Key Steps and Functions Used for Visualization:
Data Preparation:

The data was loaded, and the columns S-START and S-END were converted to date format, ensuring correct calculations of study duration.
The duration in days for each study was calculated by subtracting the start date (S-START) from the end date (S-END). This allowed for the creation of the studyDurationDays variable, representing the duration of each study.
Data Sorting:

The data was sorted by the start date, providing a logical order of bars in the Gantt chart to illustrate the chronological progression of studies.
Building the Gantt Chart:

Using the ax.barh() function from the matplotlib library, horizontal bars were created for each study, where the start of the bar corresponds to the study’s start date, and the length reflects its duration.
The study_ID was displayed on the Y-axis to identify each study group.
Counting Studies per Year:

The year was extracted from the start date (S-START) to count the number of studies conducted each year.
The value_counts() function was used to calculate study frequency by year and identify the years with the highest research activity.
Information about the years with the most studies was added to the chart legend for quick reference.
Additional Analytical Calculations:

Minimum, maximum, and average study durations were calculated and included in the legend, providing insights into the overall distribution of study durations.
Key Analytical Findings:
Temporal Distribution of Studies: The Gantt chart shows how studies are distributed over time, visually highlighting periods with high research activity when multiple studies were conducted simultaneously, as well as relatively inactive periods.
Research Intensity in Specific Years: The information on years with the most studies helps identify peak research periods, potentially indicating external factors or trends in the field that spurred increased research activity.
Study Duration: The calculations of average, minimum, and maximum study durations provide additional insights into typical study lengths, which could be useful for forecasting future projects.
This visualization provides a comprehensive understanding of study patterns over time, allowing us to easily identify both the chronological sequence and intensity of activities across different years.

List of Python Functions Used in the Analysis
Here is a list of the main Python functions applied for analysis and Gantt chart creation:

pd.read_csv() – loads data from a CSV file into a DataFrame.

pd.to_datetime() – converts data to date format, enabling accurate date-based calculations.

DataFrame.sort_values() – sorts data by a specified column (in this case, S-START), which arranges studies in chronological order on the Gantt chart.

DataFrame['column'].dt.days – calculates study duration in days by subtracting S-START from S-END and outputs the result as a number of days.

DataFrame['column'].dt.year – extracts the year from the date, allowing for data grouping by year for further frequency analysis.

value_counts() – counts occurrences of studies in each year to determine periods of peak activity.

max() and min() – calculates the maximum and minimum study durations.

mean() – calculates the average study duration, giving a general idea of the typical study period.

matplotlib.pyplot.subplots() – creates a figure and axes for plotting the Gantt chart.

ax.barh() – creates horizontal bars on the Gantt chart, where each bar represents an individual study.

ax.set_yticks() and ax.set_yticklabels() – sets Y-axis labels to display study group numbers (study_ID) instead of indexes.

mdates.YearLocator() and mdates.DateFormatter() from matplotlib.dates – formats the X-axis to show only years, providing a more readable time series.

plt.text() – adds text information (legend) on the chart, including minimum, maximum, and average study durations as well as the years with the most studies.

plt.xticks(rotation=45) – rotates the X-axis labels for better readability.

plt.tight_layout() – optimizes the layout to ensure elements are properly spaced on the chart.

These functions facilitated a complete analysis workflow and the creation of a visualization that provides a clear view of the timing and duration of studies over time.