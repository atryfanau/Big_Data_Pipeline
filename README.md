# Big_Data_Pipeline
**The goal is to find the top 100 keywords of Hacker News posts in 2014**


The data we will use comes from a Hacker News (HN) API that returns JSON data of the top stories in 2014. 
If you're unfamiliar with Hacker News, it's a link aggregator website that users vote up stories that are interesting to the community. 
It is similar to Reddit, but the community only revolves around on computer science and entrepreneurship posts.

The JSON file contains a single key `stories`, which contains a list of stories (posts). 
Each post has a set of keys, but we will deal only with the following keys:

`created_at`: A timestamp of the story's creation time.

`created_at_i`: A unix epoch timestamp.

`url`: The URL of the story link.

`objectID`: The ID of the story.

`author`: The story's author (username on HN).

`points`: The number of upvotes the story had.

`title`: The headline of the post.

`num_comments`: The number of a comments a post has.


Here's an example of the full list of keys in a story:
```
{
    "story_text": "",
    "created_at": "2014-05-29T08:23:46Z",
    "story_title": null,
    "story_id": null,
    "comment_text": null,
    "created_at_i": 1401351826,
    "url": "http://bits.blogs.nytimes.com/2014/05/28/making-twitter-easier-to-use/",
    "parent_id": null,
    "objectID": "7815285",
    "author": "Leynos",
    "points": 1,
    "title": "Making Twitter Easier to Use",
    "_tags": [
        "story",
        "author_Leynos",
        "story_7815285"
    ],
    "num_comments": 0,
    "_highlightResult": {
        "story_text": {
            "matchedWords": [],
            "value": "",
            "matchLevel": "none"
        },
        "author": {
            "matchedWords": [],
            "value": "Leynos",
            "matchLevel": "none"
        },
        "url": {
            "matchedWords": [],
            "value": "http://bits.blogs.nytimes.com/2014/05/28/making-twitter-easier-to-use/",
            "matchLevel": "none"
        },
        "title": {
            "matchedWords": [],
            "value": "Making Twitter Easier to Use",
            "matchLevel": "none"
        }
    },
    "story_url": null
}
```

