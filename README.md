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

2019-03-04: Used beautiful soup to get the director of this movie.

2019-03-06: Used beautiful soup to get the runtime of this movie.

Next: Generate a dataframe with these four information pieces of all 100 movies.

2019-03-07：Just figured out that the position of the runtime of the 100 movie in each html is different, that's why I have to rearange the beautifulsoup code 

2019-03-09: Finally found a solution, what makes it possible to collect the runtime data from the movies, even if the position is different.<br>
This peace of code made it possible: <br>
`runtime = soup.find_all('ul')[13].find_all('li')[5:8]`
`runtime = soup.find_all('time')[-1].get_text().strip()[:-len(' minutes')]`

2019-03-09: in addition to the ipynb and html files, I uploaded a csv file, what contains the collected information from the films.
