# reddit_pusher

## Startup code
```python

import requests

response = requests.get('https://api.pushshift.io'+
                        '/reddit/search/comment/'+
                        '?q=science+math&subreddit=askscience&sort=desc&size=10&sort_type=created_utc')
response_json = response.json()['data'] # to get actual data

```

## To iterate through a list of results and get only the authors
```python
authors_list = []
for idx in range(10):
    authors_list.append(response_json[idx]['author']) # get author value of result at index idx
    print("")
```
