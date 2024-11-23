# project1_movieratings
DuVoe Readme notes: 
Used google’s gemini to search for specific ways to manipulate columns. I also got help from my group when we were deciding on ways to filter the data to run through our for loop. I also received help from Jordan to extract the rotten tomatoes scores from the ratings column. 

Data Cleaning Process:

Steps taken:

1.) Download the title.basics.tsv and title.ratings.tsv files from imdb developer page

2.) Load path to files in pandas

3.) Combine the data into a single dataframe on “tconst” (imdb id)

4.) Rename columns to make it easier to look at data

5.) Run initial count

6.) Drop NA’s from dataframe

7.) Remove values with no value in “startyear” column

8.) Convert “startyear” to integer to then filter titles from time frame (2010-2019)

9.) Drop rows in “Runtime” with no value

10.) Convert “Runtime” values to integer

11.) Remove short films by runtime 60-240 min

12.) Filter out values from “Type” to only have movies

13.) Filter list by number of votes. Must have at least 1000 votes

14.) Export filtered list to CSV to more easily run code next time

15.) Run list of movie titles though OMDB API in for loop

16.) Save responses as csv to more easily run code for future use

17.) Put data in dataframe

18.) Drop DVD, Website, totalSeasons columns

19.) Filter out non movies by type

20.) Fill NA values in metascore with 0 in “Metascore” column and then convert Metascores to 10 point scale

21.) Convert “Year” column to integer

22.) Filter again by year to remove years outside of time frame

23.) Isolate rotten tomatoes score in ratings column to its own column by using code I got from Jordan. Imported “ast” and then extracted Rotten Tomatoes score from Ratings

24.) Rename “rotten_tomatoes_score" to "Rotten Tomatoes"

25.) Fill NA Rotten tomatoes scores to 0 and convert to 10 point scale

26.) Replace 13+ rating to PG-13

27.) Remove the word “min” from “Runtime”

28.) Remove TV ratings

29.) Create new Dataframe

30.) Export to CSV for visualizations and analysis


Movie Runtime
I used Xpert Learning assistant to fix my code and to generate my bar graphs. 
I also used it to fix and edit my code for running a linear regression on the ratings for each minute. 
It also helped me with my code for counting and sorting my bar graph for amount of movies in each runtime group.
I used chat GPT to debug and tweak code for separating runtimes by length.
My group also helped me with tweaking my box plot code and fixing my images that were blank when generated.
The analysis for my graphs and project are in the ipynb titled zach_code. 
To run the code, you need to read in the csv from Output, without that file it cannot run. 
The folder titled “zach_images” in the repo are where 5 of my visualizations are saved and I ended up using 3 of them for the project itself. 



James: I completed the analysis between MPAA ratings and IMDB scores. I recieved debugging help from DuVoe Moua and also the Xpert learning assistant.

Ethan Donoho:
Created the time_of_year.ipynb notebook. 
This notebook explores to answer the question: Does the time of the year of a film’s release affect its ratings. 
The first section of code, “Data Cleaning”, narrows down the csv file from output for my specific use. I created “Day, Month, Year, Day of Year, Quarter” columns. These give information on the release time of each film. 
The next section of code “Visualizations” creates many visualizations to help find any correlations between the data. 
The bar graphs simply show the number of films that fall into each quarter, month, and day of the year for each film. 
The box plots show the spread of the imdb ratings for each time period. An anova test was run on each of these plots as well, and the results are displayed above each plot. 
The scatter plots much more clearly show the average IMDB rating per time period. For each plot, a  regression line is plotted, along with its equation. The correlation coefficients are displayed above each plot. 
The last section of the notebook, “Analysis”, analyzes the box plots and scatter plots while summarizing the results altogether. 
Xpert Learning Assistant was used for syntax help while running anova tests. Stack overflow was used for help with pd.date_time conversion and spontaneously for help throughout the notebook. No chunks of code were copied. Worked collaboratively with all other members in the group. 

Makenna Vick:
