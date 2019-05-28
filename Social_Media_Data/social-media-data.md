# Finding and Using Social Media Data

Have questions after the workshop? Get in touch with us at contact-cidr[at]stanford.edu

## Learning goals

By the end of this workshop, we hope you'll have a good sense of legal and ethical concerns when trying to collect and use social media data, along with strategies for finding existing data and collecting new data.

## Outline

- Fundamental questions and approaches
- Commonly requested sources (Facebook, Twitter, etc.)
- Examples analyses with Twitter data

## Fundamental questions and approaches

- What are "Social Media"?
- Why don't we just scrape it?
  - Licensing
  - Terms of Service
  - What to look for in Licenses or Terms of Service pages
    - Search for terms like data mining, scrape/scraping, robot, spider, crawl, automated, extract.
  - Ethical concerns regarding privacy
  - Many social media companies make it incredibly difficult to scrape their content, and code in ways to detect and prevent scraping attempts. When we say, as we will for many companies, don't scrape this company's content, we're indicating the legal and ethical issues, as well as the technical problematics.
- Using existing data
  - There are social media datasets floating around reddit and other places with different amounts of documentation. You have to make a decision about whether they can be used or not based on your use case and discipline. You should absolutely be thinking about how the data was collected and whether use of that data violates legal restrictions or ethical best practices.
  - There are a lot of repositories out there with documented data as well.
  - Many of the existing datasets will not match your particular research question, but you might be able to subset them to create a suitable dataset.
- Creating your own datasets
  - APIs and associated libraries for programming languages
    - An API is not necessarily a way to scrape data; it is often built for application developers to use, not for data collection.
  - Social Feed Manager
- Opportunities for working directly with companies

## Commonly requested sources

### Facebook

- https://newsroom.fb.com/news/2018/04/restricting-data-access/
- http://theconversation.com/facebooks-data-lockdown-is-a-disaster-for-academic-researchers-94533
- https://developers.facebook.com/docs/graph-api/

First, don't scrape Facebook. It's unlikely to work and it's definitely against the terms of service.

A lot of people are interested in collecting posts from public Facebook Groups. It used to be possible to use a Facebook API to collect this data. After the Cambridge Analytica scandal, Facebook is almost entirely locked down. While the Graph API is still around, you have to establish a Facebook Developer profile for yourself as a business (complete with official business documentation) that's providing services of some sort to users or other businesses to even access the most basic public information for pages.

Existing data: you can find stray Facebook datasets on reddit, data.world, and other places on the internet. However, given the lack of clarity around how the data were collected and such, it's unlikely these could be used for publishable research. You can also find occasional datasets released by people who own the Facebook data, such as cities who are providing information about their communications, though this data is often metadata rather the posts and comments themselves.

Collaboration: Facebook periodically puts out RFPs for [research collaborations](https://research.fb.com/programs/). You can sign up for their mailing list to receive the RFPs, but they're focused on technical issues relevant to Facebook's own interests (including things like multilingual NLP, but not sociocultural phenomena).

### Instagram

Instagram is owned by Facebook. When Facebook locked itself down, it locked down Instagram's API.

- https://www.instagram.com/developer/

And, of course, you can't scrape Instagram.

- https://help.instagram.com/581066165581870

> You can't attempt to create accounts or access or collect information in unauthorized ways.
> This includes creating accounts or collecting information in an automated way without our express permission.

### Twitter

Don't scrape Twitter. Use the Twitter API:

- https://help.twitter.com/en/rules-and-policies/twitter-api
- https://developer.twitter.com/en/docs
- https://developer.twitter.com/en/products/products-overview
- https://developer.twitter.com/en/pricing

https://developer.twitter.com/en/docs/basics/things-every-developer-should-know.html

> There are different API families

> The standard (free) Twitter APIs consist of REST APIs and Streaming APIs.

> The enterprise (paid subscription) APIs include filtered firehose, historical search and engagement APIs for deeper data analytics, listening and other enterprise business applications.

> The premium (pay as you go) APIs consist of reliable and affordable versions of enterprise APIs, allowing your business to grow with your usage.

With the API, you can build up very large custom sets of tweets for your work, as long as you are following all of the requirements and terms. There is a key limitation for the publication or sharing of that data, though: Twitter's ToS do not allow you to publish collections of entire tweets, but only lists or sets of Tweet IDs. This is what is called "dehydrated" data. You can then "rehydrate" itself by hitting the Twitter API and retrieving that tweet based on the ID. This is in part because Twitter tries to respect when tweets are deleted by users. If a tweet is deleted, the API won't be able to obtain it.

Here's more of their documentation on "being a good partner" in using the Twitter API and collecting tweets: https://developer.twitter.com/en/developer-terms/agreement-and-policy#f-be-a-good-partner-to-twitter

For an overview that Justin Littman put together on finding existing data: https://gwu-libraries.github.io/sfm-ui/posts/2017-09-14-twitter-data. There are a few changes to recognize. Companies like DiscoverText that have traditionally provided paid access to historical Twitter data are not always able to provide such access anymore in the wake of Twitter becoming more careful with access.

There are existing datasets out and about including those linked at these two places:

- https://www.docnow.io/catalog/
- https://tweetsets.library.gwu.edu/

You should always check with your library's digital repository or data curator to determine whether your (or other libraries) have datasets.

You can also use Social Feed Manager to manage your own tweet harvesting.

### Sino Weibo

Much like Twitter, Sino Weibo has an API that you can use directly or through different programming libraries or applications to create new datasets.

You can also use Social Feed Manager as a way to manage your API access.

### Yelp

Yelp makes a relatively large dataset available for educational and academic purposes: https://www.yelp.com/dataset

Don't scrape Yelp. From the Yelp terms of service (https://www.yelp.com/static?p=tos):

> You also agree not to, and will not assist, encourage, or enable others to:

> Use any robot, spider, site search/retrieval application, or other automated device, process or means to access, retrieve, scrape, or index any portion of the Site or any Site Content;

### Reddit

Reddit has an API that you can use to gather Reddit data, and there are a number of libraries for different languages to assist with using the API.

There are also quite a few Reddit corpora floating around the internet. As always, make sure you understand what's contained in the data, how it was gathered, and so forth.

### Tumblr

Following the terms of service, you should also not scrape Tumblr - https://www.tumblr.com/policy/en/terms-of-service (see the "Limitations on Automated Use").

There is an API of limited usefulness. See limitations here - https://www.tumblr.com/docs/en/api_agreement - that include a provision wherein you cannot store Tumble data for more than 3 days.

And there are existing datasets out there, such as this interesting data on gifs with descriptions: https://www.kaggle.com/raingo/tumblr-gif-description-dataset.

## Places to search for data

- https://archive.ics.uci.edu/ml/index.php
- https://snap.stanford.edu/data/
- http://socialcomputing.asu.edu/pages/datasets
- https://aminer.org/data-sna
- https://www.kaggle.com/datasets
- https://toolbox.google.com/datasetsearch
- https://www.data.gov/
- https://www.docnow.io/catalog/
- http://files.pushshift.io

## An example analysis with Twitter data

This is a demo only, using tweets harvested with the Social Feed Manager as csv file.

```R
library(tidyverse)
library(leaflet)

cdmx <- read_csv("CDMX_tweets.csv") # read in the tweets

cdmx %>%
  filter(grepl("\U0001f602", text), # filter for a particular string
         !is.na(coordinates)) %>%  # remove records without coordinates
  separate(coordinates, c("lon", "lat"), sep = " ", convert = T) %>%  # turn into lat/lon
  leaflet() %>%
     addTiles() %>%  # Add default OpenStreetMap map tiles
     addMarkers(~lon, ~lat, popup = ~as.character(text),
             label = ~as.character("\U0001F602"),
             labelOptions = labelOptions(textsize = "30px"))

```

![Mexico City Tweets](img/cdmx_leaflet.png)

## Resources

SAGE handbook of social media research methods - https://searchworks.stanford.edu/view/11999820

Salganik, MJ (2018): _Bit by bit : social research in the digital age_ Princeton, New Jersey : Princeton University Press. https://searchworks.stanford.edu/view/12380521

Townsend, L and Wallace, C (2016): _Social Media Research: A Guide to Ethics._ http://dotrural.ac.uk/socialmediaresearchethics.pdf
