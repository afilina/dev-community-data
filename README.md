# Community Data

[![Build Status](https://travis-ci.org/afilina/dev-community-data.svg?branch=master)](https://travis-ci.org/afilina/dev-community-data)

The goal is simple: collect all data about technology events, current and historical for anyone to use in their applications, in order to make a stronger developer community.

Feel free to add your own record for your conference or user group, fix erroneous data or add additional fields.

## User Groups

The file [/data/user-groups.json](https://github.com/afilina/dev-community-data/blob/master/data/user-groups.json) lists all user groups. Leave "last_meetup" blank if still active.

Tip: add your entry to the top of file to avoid merge conflicts.

**Required Fields:** `key` (unique), `name`, `first_event`, `tags` ([allowable tag values](https://github.com/afilina/dev-community-data/blob/master/data/tags.json)).

```json
{
    "key": "example",
    "name": "Full user group name",
    "tags": ["php", "js"],
    "first_event": "yyyy-mm-dd",
    "last_event": "yyyy-mm-dd", 
    "locations": [
        {
            "name": "City, State (if applies), Country",
            "first_meetup": "yyyy-mm-dd",
            "last_meetup": "yyyy-mm-dd"
        }
    ],
    "website": "http://example.com",
    "twitter": "@twitter_handle",
    "calendar_feed": "http://example.com/feed.ical"
}
```

## Conferences

The files under [/data/conferences](https://github.com/afilina/dev-community-data/blob/master/data/conferences) list the various conferences. Each file contains the list of events associated with that conference.

**Required Fields:** `name`, `first_event`, `tags` ([allowable tag values](https://github.com/afilina/dev-community-data/blob/master/data/tags.json)).

```json
{
    "name": "Full conference name",
    "website": "https://example.com",
    "languages": ["en"],
    "twitter": "@twitter_handle",
    "facebook": "https://www.facebook.com/page_name",
    "code_of_conduct": "https://example.com/coc",
    "accessibility": "https://example.com/accessible",
    "diversity_tickets": "https://example.com/diversitytix",
    "tags": ["ruby"],
    "first_event": "yyyy-mm-dd",
    "is_active": true,
    "speaker_kit": {
        "ticket_included": true,
        "hotel_included": true,
        "travel_included": true
    },
    "events": [
        {
            "name": "Name of specific edition",
            "location": {
                "name": "City, State (if applies), Country"
            },
            "event_start": "yyyy-mm-dd",
            "event_end": "yyyy-mm-dd",
            "cfp_start": "yyyy-mm-dd",
            "cfp_end": "yyyy-mm-dd",
            "cfp_url": "https://example.com/2016/cfp",
            "session_feed": "https://example.com/2016/sessions.json",
            "speaker_feed": "https://example.com/2016/speakers.json",
            "hashtag": "#hashtag",
            "youtube": "https://youtube.com/playlist",
            "organizers": [
                {
                    "name": "Organizer Name",
                    "twitter": "@twitter_handle"
                }
            ]
        }
    ]
}
```
