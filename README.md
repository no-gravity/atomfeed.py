A simple RSS atomfeed generator in Python.

I use it to provide an RSS feed for https://www.gibney.org

Usage example:

```python
import atomfeed

feed_data = {
    "title": "The blog of Lumina Glitzer",
    "id": "https://...",
    "subtitle": "Notes from the most intuitive mouse in the universe",
    "link_web": "https://...",
    "link_feed": "https://.../feed",
    "updated": None,  # Use most recent entry time
    "author_name": "Lumina Glitzer",
    "author_mail": "lumina@...",
    "entries": [
        {
            "title": "The Intuition of a Mouse",
            "link": "https://...",
            "updated": "2025-09-16T02:11:00Z",
            "summary": "From 0 to 1 via intuition",
            "content": "One day I ...",
        },
        {
            "title": "Moonlight Between Floorboards",
            "link": "https://...",
            "updated": "2025-09-18T06:03:00Z",
            "summary": "A breadcrumb becomes a galaxy",
            "content": "Some other day I ..."
        },
    ]
}

print(atomfeed.generate(feed_data))
```
