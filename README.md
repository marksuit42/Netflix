# Netflix
**Overview:** Analyzing the IMDb Movies and Shows data for the last 70 years. The data contains the ratings and the votes of movies and shows along with the release year and the runtime. Your task is to do basic cleaning and manipulation and then visualize the dataset to understand trends around ratings and runtime and to identify the top movies and shows.

**Dataset:**
Dataset - Netflix

The dataset consists of Movies and Shows data including details like runtime, description, rating, votes and release year. The dataset has 5283 records and data for both movies and shows.

* **Id:** A unique count of this id would be useful while calculating and understanding trends. Example: number of movies released in 2020 would simply be a unique count of the id field.

* **Release year:** At the outset, it seems that it includes movies from 1953 to 2022, i.e. 70 years of data. But on closer inspection we notice that some years are missing e.g. 1955, 1957.

* **Title:** The dataset becomes very interesting as many of the titles can be recognized.

* **Type:** If we use the filter option in Excel to see the multiple types that are there, we will see two: MOVIE and SHOW.

* **Description:** Although for our analysis description may not be very important but we can extract keywords out of it and use machine learning to extract information like the genre of the movie/show.
* **Age\_certification:** something to note here is that in many cases age certification is missing. We may want to handle missing values separately in some cases, but here since there is no effective way to substitute this missing information we will leave it as is for our analysis.

* **Runtime:** Although it is not mentioned, it is clear that runtime is in minutes. One should see the range of values, visualize the distribution and if required, handle outliers in this field.

* **IMDb\_Score:** This is the IMDb rating of the movie/show. This tells us how well the movie was rated by the voters.

* **IMDb\_votes:** This is the number of people who voted on IMDb for a movie or show. It is important to recognize that this leads to a lot of subjectivity because if very few people have voted for a movie/show its imdb\_score will not be very reliable.

**Tasks to do:**

1.  Create a new column in Power Query Editor: Score x Votes

2.  Create a new column runtime\_hrs using DAX. For this column convert runtime to hours.

3.  Create slicers for runtime\_hrs, release year and type
    1.  runtime\_hrs: Style should be "Between"
    2.  release year: Style should be "Tiles"
    3.  type: Style should be "Dropdown"
       
4. Create a donut chart for number of movies released in each year and a pie chart for number of shows released in each year. Both these charts should be filtered for movies/shows released after 2010

5. Depicting using an appropriate chart how average of rating*votes varies with runtime

6. How many movies were released in each age certification bucket since 2000? Create a bar chart for the same.

7. How does score*votes vary with age certification? On the same graph depict how age Certification vary with the average runtime_hrs

8. Create a card for title and a multi row card for description
