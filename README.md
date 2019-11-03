# Equipos Nacionales Ranking 
Here I use Python to extract data from 2 sources in order to perform an analysis that tries to explain Bolivia National Football Team long history (25+ years) of bad results. To do so, I compare (i) Bolivia's football team and (ii) all national teams from CONMEBOL performance on the pitch (approximated by the team Elo ranking position) vs the degree of internationalization of its players. We define internationalization in this context by the fact of a national player playing for a club in a country different from its own. 

The main assumption is that a higher degree of internationalization of players in a national football team will have a positive impact in the team's performance (approximated by the country Elo ranking position).

## Files
* 1_equipos_nacionales_webscraping.ipynb: web scraping process to extract data from the site https://www.footballdatabase.eu. The data extracted is about which players play in their national teams (from all 10 countries in CONMEBOL) and where do they play (in which clubs).
* 2_equipos_nacionales_df.ipynb: we complete the dataset build in the last step by adding a an important variable: the country of the club where each player belongs. This allows to measure the degree of internationalization of each country national football team.
* 3_ranking_elo_webscraping.ipynb: web scraping process to extract data from the site https://eloratings.net/. The data extracted is about Elo ranking position evolution of every national football team. 
* 4_analisis_relacion_elo_IJE.ipynb: here we perform the data exploration and analysis to explain the relationship between a team's performance on the pitch (approximated by its Elo ranking position) and the degree of internationalization of its players.

## Datasets
If you're not intersted in the web scraping process (by the way I use BeautifulSoup and Selenium) and want to jump straight to data, you have at your disposal the following datasets:
* 1_equiposnac: año (year), equiponac (national team), jugador (player's name) and club (club where he was playing at the end of the year).
* 2_equiposnac2: the same columns as 1_equiposnac, including pais_club (country of the club).
* 3_elo_agg: equiponac (national team), año (year) and rank (ranking positon. It's calculated using the arithmetic mean of all the ranking positions available).
* 4_Elo_IJE: año (year), equiponac (national team), IJE (degree of internationalization of a national team's players in a given year. It's calculated as follows: IJE = number of players of the national team playing abroad / total number of national team players) and rank.



