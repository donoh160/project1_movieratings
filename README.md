# project1_movieratings

## Project: Movie Ratings
How do certain factors impact a movie's average IMDB rating?
Namely,
* Box Office
* Runtime
* MPAA Rating
* Time of Year

All code is nested within *group_project*.

## Data Cleaning Process (DuVoe Moua):
Used google’s gemini to search for specific ways to manipulate columns. I also got help from my group when we were deciding on ways to filter the data to run through our for loop. I also received help from Jordan to extract the rotten tomatoes scores from the ratings column. 

Steps taken:
First I downloaded the tsv files from the imdb developer page and loaded the path to my jupyter notebook. I then combined both tsv files into a dataframe on “tconst” which is the imdb id. Once everything is loaded I filtered the columns by removing NA’s and converting “startyear” to an integer. Then I filtered the start years to fit our time frame of 2010-2019. I continued by dropping rows with no value in “Runtime” and then converted “Runtime” values to integers and removed values outside of 60-240 minutes. After that I filtered out non movie types from “Type” and filtered out “nuVotes” to be at least 1000 votes. Once the initial filtering is done, we ran the remaining titles through the OMDB API in a for loop. (In order to pull more than 1,000 titles, I had to donate $1 to OMDB.) We then saved the responses as a csv to make it easier to run code later since it took about 8 hours for the titles to run through the API.

 Put the data in a dataframe. Once the data was in the dataframe I dropped columns DVD, Website and totalSeasons and filtered out non movie types again. Ultimately, we ended up not using Metascore and Rotten tomatoes scores but we did convert them to 10 point scales. I converted the “Year” column to an integer and again removed titles outside of our range 2010-2019. I also removed TV ratings and replaced ratings with “13+” to PG-13 and removed the word “min” from “Runtime”. Once finished I created a new dataframe and then exported it to a csv for the visualization and analysis portions. 

## Box Office (Makenna Vick):
In *box_office*, we compare a movie’s domestic box office — measured in gross USD — to its average IMDB rating. Movies that made less than a reasonable amount (arbitrarily chosen as ~$10k) were dropped. We then split the data into 20 quantiles and plotted accordingly; see *box_office_binned* in *Images*. Notes & conclusions can be found within the jupyter notebook.

Thank you to Ethan Donoho and the rest of my group for helping me with my portion of the project. Stack Exchange & Google’s Gemini also came to the rescue with miscellaneous questions regarding syntax.

## Movie Runtime (Zach Rehfuss)
I used Xpert Learning assistant to fix my code and to generate my bar graphs. 
I also used it to fix and edit my code for running a linear regression on the ratings for each minute. 
It also helped me with my code for counting and sorting my bar graph for amount of movies in each runtime group.
I used chat GPT to debug and tweak code for separating runtimes by length.
My group also helped me with tweaking my box plot code and fixing my images that were blank when generated.
The analysis for my graphs and project are in the ipynb titled zach_code. 
To run the code, you need to read in the csv from Output, without that file it cannot run. 
The folder titled “zach_images” in the repo are where 5 of my visualizations are saved and I ended up using 3 of them for the project itself. 

## MPAA Ratings (James Elander): 
I completed the analysis between MPAA ratings and IMDB scores. I recieved debugging help from DuVoe Moua and also the Xpert learning assistant.

## Time of Year (Ethan Donoho):
Created the time_of_year.ipynb notebook. 
This notebook explores to answer the question: Does the time of the year of a film’s release affect its ratings. 
The first section of code, “Data Cleaning”, narrows down the csv file from output for my specific use. I created “Day, Month, Year, Day of Year, Quarter” columns. These give information on the release time of each film. 
The next section of code “Visualizations” creates many visualizations to help find any correlations between the data. 
The bar graphs simply show the number of films that fall into each quarter, month, and day of the year for each film. 
The box plots show the spread of the imdb ratings for each time period. An anova test was run on each of these plots as well, and the results are displayed above each plot. 
The scatter plots much more clearly show the average IMDB rating per time period. For each plot, a regression line is plotted, along with its equation. The correlation coefficients are displayed above each plot. 
The last section of the notebook, “Analysis”, analyzes the box plots and scatter plots while summarizing the results altogether. 
Xpert Learning Assistant was used for syntax help while running anova tests. Stack overflow was used for help with pd.date_time conversion and spontaneously for help throughout the notebook. No chunks of code were copied. Worked collaboratively with all other members in the group. 
