# CeneoScraperIK
https://www.ceneo.pl/84514582#tab=reviews_scroll
## Ceneo scraping algorithm
1. Analysis if the structure of the website
2. Sending HTTP request to access first page with opinions
3. Cheking the code of HTTP responce 
4. Parse the HTML code of first page with opinions 
5. Extract requiered data from pursed code
6. If there are more pages, move to the next page and repeat steps 2-6 for it 
7. Save extracted data

## Analysis of the structure of the webpage
|Component|Selector|Variable|
|---------|--------|--------|
|Opinion |div.js_product-review| 
|Opinion ID |[data-entry-id]|  
|Author |span.user-post__author-name| 
|Recommendation |span.user-post__author-recomendation > em| |recomendation|
|Number of stars |span.user-post__score-count|stars|
|Content of opinion |div.user-post__text|content|
|List of advantages |div.review-feature_item--positive|pros|
|List of disadvatages |div.review-feature_item--negative|cons|
|For how many helpful |button.vote-yes[data-total-vote]|vote_yes|
|For how many unhelpful |button.vote-no > span|vote_no|
|Publishing date  |span.user-post__published > time:nth-child(1)[datetime]|published|
|Purchase date |span.user-post__published > time:nth-child(2)[datetime]|purchased|
