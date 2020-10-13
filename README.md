# Movie hype curve duration predition
The original goal of this project was to collect enough weekly data for movies with budgets to define the initiation of a "hype" and then target engineer the end of a "hype cycle" for a given genre. This could be thought of as determining the value of an investment for a film studio over a short term (2-3years) - Think Blair Witch Project, the Scream sequels, pre-2000 comic book hero reboots. If the general trend (in the following years) since a breakout film can be predicted reliably, the impact comes in when we can define where a film studio's near-term finite budget can be allocated per genre.

# Pivot project: Box office calendar gross for movies from 1977 to 2019
I made the decision to pivot the project late in the timeline when I wasn't able to scrape the requisite data quickly enough. The aim of the submitted project was to use web scraping and linear regression to predict outcomes for calendar gross for movies, scraped from boxofficemojo. The notebooks within provide a step-wise guide that I took to acquire data, curating (processing) it, through linear regression.

### Features, and Target Variables
- My target is Calendar Gross (gross box office of a movie for the year in which it was released). I chose this metric as opposed to total domestic gross or total worldwide gross because I believed it to be a more reasonable indicator for the expected gross of a movie, without a myriad of additional metrics to better understand the impacts of re-releases or worldwide audience behaviors. An alternative approach would have been to limit the data to movies that have not been re-released, and look at total domestic gross.
- I started out with 83 features, but I settled on 5 for prediction: Budget, Max Number of theaters, IMDB Rating, Number of Votes per IMDB rated movie, Week 1 Gross

### Datasets and Tools
- Data sources scraped/used are from BoxOfficeMojo (movie statistics), IMDB (ratings and votes), and Statista (average movie ticket price per year)
- Tools (modules) include: Beautiful Soup, Selenium, Seaborn, Statsmodels, and Sci-kit Learn
