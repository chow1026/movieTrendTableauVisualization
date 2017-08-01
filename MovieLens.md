
# Tableau Visualization - Movie Rating Dataset from MovieLens


This dataset is collected from a movie recommendation service called MovieLens.  It describes 5-star rating and free-text tagging activity collected from the site.  The dataset comes in 3 sizes: _Small_, _20M_, and _Full_.  For the purpose of visualization with Tableau and data exploratory, I had to use with _Small_, because of the limitations of Tableau.  

## About _Small_ Dataset      
It contains 100004 ratings and 1296 tag applications across 9125 movies. These data were created by 671 users between January 09, 1995 and October 16, 2016. This dataset was generated on October 17, 2016.  

Users were selected at random for inclusion. All selected users had rated at least 20 movies. No demographic information is included. Each user is represented by an id, and no other information is provided.

The data are contained in four files links.csv, movies.csv, ratings.csv and tags.csv.


## Version 0:   
The V0 Tableau Worksheet is generated for initial exploratory and brainstorming process.

### Design:  
a. [Movie by Genre Year ][0946e7b3]        
To see the overall trend of movie production over the years, I had chosen to plot a histogram  chart, with 5 year bin.  I used x axis to encode 5 year bin, y axis to encode count of titles, and colors to encode movie genre.     

b. [Ratings vs Genre][99349fc5]    
A bar chart is plotted to see if there is any correlation between average ratings and genres.  The plot shows there is no particular genre that has particular outstanding ratings.  I used x axis to encode genre, y axis and color (range) to encode average ratings.      

c. [Ratings for Genre Over Time][1bd98f06]      
A bar chart is plotted this to see if there is any genre that grew more popular by average ratings.  I applied dual axis on x-axis to encode 5 year bin, y axis to encode average ratings, and colors to encode genre.       

d. [Top Rated Movies][da5db654]     
This plot was plotted to show all the titles, its release year, the count of ratings it received, its average ratings.  It is a bubble plot using x axis to encode average ratings, y axis to encode movie release year, bubble size and color to encode the count of ratings.    

  [0946e7b3]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v1/MoviesProduction5YearBins "Movie Production 5 Year Bin"
  [99349fc5]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v0/RatingsvGenre "Ratings vs Genre"
  [1bd98f06]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v0/RatingsforGenreOverTime "Ratings for Genre Over Time"
  [da5db654]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v0/TopRatedMoviesShows "Top Rated Movies"



### Feedback:
The general feedback was that all the plots had shown basic/initial analysis of the dataset but had little/no elements of explanatory nor storytelling.  I was advised to step back and rethink about the questions I was trying to answer and then how I should extract and present the data.  

In addition, feedback received with respect to each individual plots are:

a. [Movie by Genre Year ][0946e7b3]      
While the trend of quantity produced over time was well represented, it is hard to decode/read the trends for genres over year.  

b. [Ratings vs Genre][99349fc5]    
Bar chart isn't great at showing correlations, even the bars mildly indicated no correlation between genre and ratings.    

c. [Ratings for Genre Over Time][1bd98f06]      
Dual axis made the plot particularly long.  Using Year as Dimension, also made it hard to see the trends.  It is also hard to compare trends among genres.  

d. [Top Rated Movies][da5db654]     
This plot generally looks good as it shows the cluttering patterns of average ratings for movies.  However, even with this small dataset, it is hard to identify movies with the most rated (highest count of ratings) and/or highest rated (highest average ratings).  
