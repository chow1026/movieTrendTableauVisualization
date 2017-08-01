
# Tableau Visualization - Movie Rating Dataset from MovieLens


This dataset is collected from a movie recommendation service called MovieLens.  It describes 5-star rating and free-text tagging activity collected from the site.  The dataset comes in 3 sizes: _Small_, _20M_, and _Full_.  For the purpose of visualization with Tableau and data exploratory, I had to use with _Small_, because of the limitations of Tableau.  

## About _Small_ Dataset      
It contains 100004 ratings and 1296 tag applications across 9125 movies. These data were created by 671 users between January 09, 1995 and October 16, 2016. This dataset was generated on October 17, 2016.  

Users were selected at random for inclusion. All selected users had rated at least 20 movies. No demographic information is included. Each user is represented by an id, and no other information is provided.

The data are contained in four files links.csv, movies.csv, ratings.csv and tags.csv.


## Version 0:   

#### [View on Tableau Public](https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v0/TopRatedMoviesShows)

The V0 Tableau Worksheet is generated for initial exploratory and brainstorming process.

### Version 0 Design:  

**WORKSHEETS**    

a. [Movie by Genre Year ][0946e7b3]        
To see the overall trend of movie production over the years, I had chosen to plot a histogram  chart, with 5 year bin.  I used x axis to encode 5 year bin, y axis to encode count of titles, and color hues to encode movie genre.     

b. [Ratings vs Genre][99349fc5]    
A bar chart is plotted to see if there is any correlation between average ratings and genres.  The plot shows there is no particular genre that has particular outstanding ratings.  I used x axis to encode genre, y axis and color saturations to encode average ratings.      

c. [Ratings for Genre Over Time][1bd98f06]      
A bar chart is plotted this to see if there is any genre that grew more popular by average ratings.  I applied dual axis on x-axis to encode 5 year bin, y axis to encode average ratings, and color hues to encode genre.       

d. [Top Rated Movies][da5db654]     
This plot was plotted to show all the titles, its release year, the count of ratings it received, its average ratings.  It is a bubble plot using x axis to encode average ratings, y axis to encode movie release year, bubble size and color saturations to encode the count of ratings.    

  [0946e7b3]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v1/MoviesProduction5YearBins "Movie Production 5 Year Bin"
  [99349fc5]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v0/RatingsvGenre "Ratings vs Genre"
  [1bd98f06]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v0/RatingsforGenreOverTime "Ratings for Genre Over Time"
  [da5db654]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v0/TopRatedMoviesShows "Top Rated Movies"



### Version 0 Feedback:
The general feedback was that all the plots had shown basic/initial analysis of the dataset but had little/no elements of explanatory nor storytelling.  I was advised to step back and rethink about the questions I was trying to answer and then how I should extract and present the data.  

In addition, feedback received with respect to each individual plots are:

**WORKSHEETS**  

a. [Movie by Genre Year ][0946e7b3]      
While the trend of quantity produced over time was well represented, it is hard to decode/read the trends for genres over year.  

b. [Ratings vs Genre][99349fc5]    
Bar chart isn't great at showing correlations, even the bars mildly indicated no correlation between genre and ratings.    

c. [Ratings for Genre Over Time][1bd98f06]      
Dual axis made the plot particularly long.  Using Year as Dimension, also made it hard to see the trends.  It is also hard to compare trends among genres.  

d. [Top Rated Movies][da5db654]     
This plot generally looks good as it shows the cluttering patterns of average ratings for movies.  However, even with this small dataset, it is hard to identify movies with the most rated (highest count of ratings) and/or highest rated (highest average ratings).  





## Version 1:   

#### [View on Tableau Public](https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v1/MovieLensMovieRatings)

The V1 Tableau Worksheet is generated incorporate more explanatory and storytelling.  A few dashboards and a storyboard were also added.  

### Version 1 Design:      

**WORKSHEETS**      

a. [Movie Production (5 Year Bins)][8bcac020]    
This is the same as [Version 0 Plot a][0946e7b3].    

  [8bcac020]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v1/MoviesProduction5YearBins "Movie Production (5 Year Bins)"

b. [Movie Production by Genre Over Time][4826bc79]
A line chart is plotted to show trends of movie production by genre.  I used x axis to encode year, y axis to encode count of titles, and color hues to encode genre.  

  [4826bc79]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v1/MovieProductionbyGenreoverTime "Movie Production by Genre Over Time"

c. [Ratings vs Genres][55ebc0a3]       
This plot is used in replacement of [Version 0 Plot b][1bd98f06].  A combination of bubble and scatter plot were used to show an overview of which genre is most rated and which is highest rated (highest average ratings).  I applied dual axis on y axis to encode average ratings and count of ratings, x axis and colors to encode genre, y axis and bubble size to encode count of ratings, y axis, shape and color saturation to encode average ratings.    

  [55ebc0a3]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v1/RatingsvGenres "Ratings vs Genres"

d. [Yearly Average Ratings by Genre (1995 - 2016)][8791c08a]     
This plot is used in replacement of [Version 0 Plot c][1bd98f06].  Color hues and shapes were used to encode genre, bubble size used to encode count of ratings, x axis used to encode release year and y axis used to encode average ratings.    

  [8791c08a]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v1/YearlyAvgRatingsbyGenre "Yearly Average Ratings by Genre"   

e. [Yearly Average Ratings by Genre Crosstab (1995 - 2016)][c1283914]        
This crosstab table is added to supplement plot d [Yearly Average Ratings by Genre (1995 - 2016)][8791c08a].   

  [c1283914]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v1/YearlyAvgRatingsbyGenreCrosstab "Yearly Average Ratings by Genre Crosstab"    

f. [Movie Ratings][2bb1bf08]     
This is same as [Version 0 plot d][da5db654], but retitled.     

  [2bb1bf08]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v1/MovieRatings "Movie Ratings"

g. [Most Rated and Highest Rated Movies][9fe7e2bf]      
This is a combination of bar chart and point chart to zoom into detailed view of most rated and highest rated movies.  Dual axis applied on x axis to encode average ratings and count of ratings, y axis to encode title with release year.  Chart can be sorted by average ratings or count of ratings to easily identify top ranked movies.      

  [9fe7e2bf]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v1/MostRatedandHighestRatedMovies "Most Rated and Highest Rated Movies"


**DASHBOARDS**     

h. [Trends of Yearly Movie Production][2e3f7ba6]
Dashboard built with Sheet a and Sheet b.  

  [2e3f7ba6]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v1/YearlyTrendsofMovieProductions "Yearly Trends of Movie Production"

i. [Most Rated and Highest Rated Genre][07db28f5]     
Dashboard built with Sheet c.

  [07db28f5]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v1/MostRatedandHighestRatedGenres "Most Rated and Highest Rated Genre"     

j. [[Trends of Yearly Average Ratings by Genre][6d35feb1]]     
Dashboard built with Sheet d and Sheet e (crosstab of d).  

  [6d35feb1]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v1/TrendsofYearlyAvgRatingsbyGenre "Trends of Yearly Average Ratings by Genre"

k. [Most Rated and Highest Rated Movies Dashboard][a773ebb6]
Dashboard built with Sheet g.  

  [a773ebb6]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v1/MostRatedandHighestRatedMoviesDB "Most Rated and Highest Rated Movies Dashboard"


**STORYBOARD**     

l. [MovieLens Movie Ratings][535356b3]        
Storyboard built with dashboard h, i, j, k.      

  [535356b3]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_v1/MovieLensMovieRatings "MovieLens Movie Ratings"


### Version 1 Feedback:     

**Positive Feedbacks**:     
- A good improvement from Version 0.  
- This version is more explanatory.  
- Good combination of sheets to build dashboards.  
- Chart d was still hard to read.  

**Negative feedbacks**:    
- Titles and labels were not consistent across sheets and were a bit confusing.  
- Layouts and views of dashboards on the final storyboard were not consistently responsive to viewport.  
- The flow of the storyboard wasn't entirely smooth.  I was encouraged to write more in the caption box to guide users the flow of thoughts.

On top of this, here are some **sheet/dashboard specific feedback**:   

c. [Ratings vs Genres][55ebc0a3]  
Hard to differentiate bubble size.  

d. [Yearly Average Ratings by Genre (1995 - 2016)][8791c08a]    
Chart a bit hard to read due to overlapping data point.  Also hard to see trends.  



## Final Version:     

#### [View on Tableau Public](https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_final/MovieLensMovieRatings)

In general these are the modifications made on Final Version:    
- Checked and edited Titles and labels
- Checked and made sure layouts and viewports across dashboards are consistent and responsive.  


### Final Version Design (Listing Only Modifications):      

**WORKSHEETS**      

c. [Ratings vs Genres][e4602554]
- Made bubble size bigger.  

  [e4602554]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_final/RatingsvGenres "Ratings vs Genres"

d. [Yearly Average Ratings by Genre (1995 - 2016)][7fbe1537]     
- Edited y-axis range to cover 2.0 to 5.0.   
- Made shape size slightly bigger so genre with lower count of ratings could still be seen.  

  [7fbe1537]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_final/YearlyAvgRatingsbyGenre "Yearly Average Ratings by Genre"

**DASHBOARDS**     
m. [Movie Ratings Dashboard][d8b54404]    
Added this dashboard to help the flow of story.  This dashboard shows the cluster patterns of movie ratings.  

  [d8b54404]: https://public.tableau.com/profile/yoong.shin.chow#!/vizhome/TableauProject_ml-latest-small_final/MovieRatingsDashboard "Movie Ratings Dashboard"



**STORYBOARD**     

l. [MovieLens Movie Ratings][4c6a280b]    
- Added elaboration in caption for each dashboard.  
- Reworked layout to make storyboard more consistent.  


##References:     
- [https://grouplens.org/datasets/movielens/](https://grouplens.org/datasets/movielens/)     
- [https://movielens.org/](https://movielens.org/)
- [https://www.tableau.com/learn/training](https://www.tableau.com/learn/training)     
- [https://discussions.udacity.com/c/nd002-data-visualization-with-tableau](https://discussions.udacity.com/c/nd002-data-visualization-with-tableau)
- [https://community.tableau.com/welcome](https://community.tableau.com/welcome)
