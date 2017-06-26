# hubot-rss-alerts
Hubot watches an RSS feed, announces when there are any new items

## Installation

Install the script using npm:

    npm install --save hubot-rss-alerts

Enable it by adding to your `external-scripts.json` file.

    [
      ...
      "hubot-rss-alerts",
      ...
    ]

## Configuration

There are two required settings:

* `HUBOT_ALERTS_RSS_FEED` - should contain the URL of the feed you want Hubot to monitor
* `HUBOT_ALERTS_RSS_ANNOUNCE_ROOM` - should contain the room name where Hubot will announce new feed items

There are some other optional settings you may want to change:
* `HUBOT_ALERTS_RSS_INTERVAL` - how often (in seconds) to check the RSS feed - default: 300 (5 minutes)
* `HUBOT_ALERTS_RSS_PREPEND` - text to prepend to alert messages - default: "RSS Alert"
* `HUBOT_ALERTS_RSS_BROKEN_TZ_ADJUSTMENT` - if a feed's timezone is broken set this to adjust it - default: 0
* `HUBOT_ALERTS_RSS_SKIP_FIRST` - skip any items when first checking the feed - default: true (set to false for debugging)

## Notes, Plans, etc.

Currently only handles one RSS feed -- I might work on fixing that next.
