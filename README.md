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


James: I completed the analysis between MPAA ratings and IMDB scores. I recieved debugging help from DuVoe Moua and also the Xpert learning assistant.
