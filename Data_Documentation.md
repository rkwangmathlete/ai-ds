Data Documentation
Source

This dataset comes from Kaggle: "Finishers Boston Marathon 2015, 2016 & 2017", uploaded by user rojour, containing official individual race results originally compiled from the Boston Athletic Association's public results. This project combines the three separate yearly CSV files into one file (data.csv), adding a Year column so each row records which year's race it came from.

Size

Combining all three years, the dataset contains approximately 79,000 rows (about 26,000-27,000 finishers per year) and 9 columns.

Features
Column	Description
Bib	Runner's bib number (unique identifier for that race)
Age	Runner's age on race day
Gender	Runner's gender (M or F)
Country	Runner's home country
5K, 10K, Half, 30K, 40K	Cumulative time (hh:mm:ss) at each checkpoint distance, used to calculate pacing throughout the race
Official Time	Runner's final official race finish time
Year	The race year (2015, 2016, or 2017), added when combining the three original files
Potential Issues
Missing values: A small number of rows have missing checkpoint times for runners who did not register a chip time at every mat along the course.
Data type formatting: All time columns are stored as text (hh:mm:ss) rather than numbers, so they need to be converted to total seconds or minutes before any calculations or modeling can be done.
Duplicate or reassigned bibs: A small number of bib numbers may appear more than once across the combined years if a bib was reused or reassigned.
Selection bias: The Boston Marathon requires runners to meet a qualifying time to enter, so this dataset only represents relatively experienced, competitive runners and is not representative of casual or first-time marathoners.
DNS/DNF exclusion: The dataset only includes runners who finished the race. Runners who started but dropped out (potentially the ones most affected by "hitting the wall") are not included, which could cause the analysis to underestimate how common or severe the effect really is.
Year-to-year differences: Course conditions (weather, temperature) differed across 2015, 2016, and 2017, which is not captured in this dataset and could be a confounding factor behind any year-to-year differences in pacing patterns.
