# News Articles Scrapping API
Flask Based API to get the News Articles been scrapped using the News Source URL and get data in JSON format as Output.
This API is based on the structure based on a simple python project to get NEWS Articled Scrapped [NEWS PAPER SCRAPPING using Python](https://github.com/imakashsahu/News-Article-Scrapping)

## Required Python Libraries
```
- newspaper3k
- news-fetch
- flask
```

# Fields Fetched
```
'headline': news.headline, 
'author': news.authors, 
'publish_date': news.date_publish, 
'modify_date': news.date_modify,
'download_date': news.date_download,
'image_url': news.image_url,
'filename': news.filename,
'description': news.description,
'publication': news.publication,
'category': news.category,
'source_domain': news.source_domain,
'article': news.article,
'summary': news.summary,
'keyword': news.keywords,
'title_page': news.title_page,
'title_rss': news.title_rss,
'url': news.uri
```

## How to Run the API 
```
Run the ***app.py*** file from the command after which we can use the below HTTP GET url get the source scrapped
*http://localhost:5000/?source_url=*
*http://localhost:5000/?source_url=www.website.com*
```


## Tweak to made fulfill your needs
1. The Code is developed fetch the news article from the source for the past 24 hrs by default but can be changed in ***get_all_article.py***
   - **difference_day == 0:**
   - 0 - If you want to fetch all article from Today
   - 1 - If you want to fetch all article from yesterday
   - Increase number accordingly to fetch the respective date

2. The code uses the memoize feature in order to fetch only the new fetch when run rather than unnecessarily fetching all articles on every run
   - **news_paper = newspaper3k.build('http://www.cnn.com/', memoize_articles=True)**
   - *memoize_articles=TRUE* turns memoize ON
   - *memoize_articles=FALSE* turns memoize OFF
