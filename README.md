# Archive Subreddit Posts

Archives every post & every comment in every post in a given subreddit into the data format of the Pushshift API.

Build the project (or just use the prebuilt version in the ./_build/ folder), specify the subreddit, output directory, and the "after this date" / "before this date" in appsettings.json & then run reddit_scraper.exe!

It outputs one JSON file per day in the range, where each is a list of posts for that day, where each post has a list of ever comment on the post. No data is omitted from what the API returns (so you could re-create the entire subreddit if you wanted).

Project was built in Visual Studio 2019 with .NET Core 3.1 & C# 8.0

![Usage](https://i.imgur.com/y7wIAQ0.png)

### Note:
The bottleneck in speed of archiving is the rate that pushshift limits you to. Will look at what ways there are around this at some point but in the meantime your best bet for faster archiving would be to run this in some # of containers or vms.
