# rotten-tomatoes2
use beautifulsoup and directly scrape data from the page rottentomatoes.com

Based on a data gathering task at udacity.com and the repo "rotten-tomatoes1", I try to practice data scraping skills with BeautifulSoup.<br>
From the page [Top 100 Movies of 2018](https://www.rottentomatoes.com/top/bestofrt/?year=2018) I use jupyter notebook to create a dataframe, what finally should contain the following information of these films:
* Movie title 
* Genre 
* Director 
* runtime (mins) 

The html and ipynd files represent the status of this project. 

2019-03-02: Already managed it to create a list from the page [Top 100 Movies of 2018](https://www.rottentomatoes.com/top/bestofrt/?year=2018), what contains the url's to the top 100 movies of 2018.

2019-03-03: Used `request` to get html content of the webpage of the first movie in df_list. Used beautiful soup to get the title and the genre of this movie.

Next: Try to get the director and the runtime of the movie.
