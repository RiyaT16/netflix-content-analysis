# netflix-content-analysis
Analysis of Netflix’s movies and TV shows dataset, exploring content trends, genres, release patterns, and duration to uncover insights about catalog growth and audience preferences.

**Objective:** The objective of this project is to apply advanced analytics to a Netflix’s dataset of movies and TV shows. By performing in-depth data exploration, visualization, and trend analysis, the project aims to uncover actionable insights into content distribution, genre popularity, release timing, and audience preferences. 

**Dataset:** The following dataset was used for the analysis - https://www.kaggle.com/datasets/shivamb/netflix-shows

**Data Pre-Processing:** The analysis began with a exploration and cleaning of the dataset. Missing values were identified and addressed using appropriate imputation techniques, such as replacing empty entries with the most frequent value (mode) or categorizing them as "NA" where necessary. Irrelevant columns, such as director and cast, were excluded from the dashboard to maintain clarity and focus.

Categorical variables were standardized, and date fields were formatted for consistency. For missing dates, the first day of the release year was used as a proxy. The cleaned dataset was then analyzed using Power BI, enabling interactive visualizations to uncover trends in content type, genre distribution, release patterns, and duration.
Below is a summary of the columns present in the dataset, their characteristics pre-processing steps -

| Column Name  | Description                         | Type of Column             | Distinct Values | Number of Missing Values | Solution Employed                                                                 |
|--------------|-------------------------------------|----------------------------|-----------------|-------------------------|----------------------------------------------------------------------------------|
| show_id      | Unique Identifier                   | Incremental Values         | 8,807           | 0                       | Not Required                                                                     |
| type         | Type of the row                     | Categorical                | 2               | 0                       | Not Required <br>Movies (70%)<br>TV Shows (30%)                                  |
| title        | Title of the movie/show             | Descriptive                | 8,807           | 0                       | Not Required                                                                     |
| director     | Director of the movie/show          | Descriptive                | 4,526           | 2,634                   | Not used in the dashboard                                                        |
| cast         | Cast of the movie/show              | Comma Separated Values     | 7,692           | 825                     | Not used in the dashboard                                                        |
| country      | Country of Release                  | Comma Separated Values     | 123             | 831                     | Categorized as "NA"                                                              |
| date_added   | Date on which the movie was added   | Date                       | 1,761           | 10                      | Replaced with 1st Jan of the release year                                        |
| release_year | Year in which the movie was released| Year                       | 74              | 0                       | Not Required                                                                     |
| rating       | Viewership Rating                   | Categorical                | 18              | 4                       | Blanks and Misc (3) considered as NA                                             |
| duration     | Duration of the movie/show          | Numerical                  | 220             | 3                       | Empty entries were substituted with the mode of the time values                  |
| listed_in    | Genre of the movie/show             | Categorical                | 514             | 0                       | Not Required                                                                     |
| description  | Description of the movie            | Descriptive                | 8,775           | 0                       | Not Required                                                                     |

**Views:**

**1. Total Titles, Movies, TV Shows, Countries, Genres**
This section gives a snapshot of Netflix’s vast library, showing the total number of titles, split between movies and TV shows, as well as the number of countries and genres represented.

**2. Total Titles by Year**
The chart tracks how many new movies and TV shows were added each year, highlighting growth trends and any fluctuations in Netflix’s annual content additions.

**3. Titles by Ratings**
This bar chart summarizes the maturity ratings of available content, revealing Netflix’s emphasis on teen and adult programming.

**4. Time Lag Between Release Year and Year Added**
Most titles are added to Netflix within a decade of their original release, indicating a focus on relatively recent content.

**5. Titles by Country**
A world map visualizes the global reach and diversity of Netflix’s content, with strong representation across multiple continents.

**6. YoY Distribution Across Show Times**
This chart displays how the runtime of Netflix titles has evolved, showing a trend towards longer content in recent years.
