# Finding and Using Social Media Data

Have questions after the workshop? Get in touch with us at contact-cidr[at]stanford.edu

## Learning goals

By the end of this workshop, we hope you'll have a good sense of legal and ethical concerns when trying to collect and use social media data, along with strategies for finding existing data and collecting new data.

## Outline

- Fundamental questions and approaches
- Commonly requested sources
- An example analysis with Twitter data

## Fundamental questions and approaches

- Why don't we just scrape it?
  - Licensing
  - Terms of Service
  - What to look for in Licenses or Terms of Service pages
  - Ethical concerns regarding privacy
- Using existing data
  - There are social media datasets floating around reddit and other places with different amounts of documentation. You have to make a decision about whether they can be used or not based on your use case and discipline. You should absolutely be thinking about how the data was collected and whether use of that data violates legal or ethical concerns.
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

First, don't scrape Facebook. It's definitely against Terms of Service.

A lot of people are interested in collecting posts from public Facebook Groups. It used to be possible to use a Facebook API to collect this data. After the Cambridge Analytica scandal, Facebook is mostly locked down, though the Graph API is still around with significant limitations. At this point, access to data through the API is almost entirely dependent upon explicit approval by Facebook.

Existing data: you can find stray Facebook datasets on reddit, data.world, and other places on the internet. However, given the lack of clarity around how the data were collected and such, it's unlikely these could be used publishable research. You can also find occasional datasets released by people who own the Facebook data, such as cities who are providing information about their communications, though this data is often metadata rather the posts and comments themselves.

Collaboration: Facebook does accept proposals for research collaborations, though I don't know details (https://research.fb.com/programs/).

### Instagram

Instagram is owned by Facebook. When Facebook locked itself down, it locked down Instagram's API.

- https://www.instagram.com/developer/

And, of course, you can't scrape Instagram.

- https://help.instagram.com/581066165581870

> You can't attempt to create accounts or access or collect information in unauthorized ways.
> This includes creating accounts or collecting information in an automated way without our express permission.

### Twitter

Use the Twitter API:

- https://help.twitter.com/en/rules-and-policies/twitter-api
- https://developer.twitter.com/en/docs
- https://developer.twitter.com/en/products/products-overview
- https://developer.twitter.com/en/pricing

https://developer.twitter.com/en/docs/basics/things-every-developer-should-know:

> There are different API families

> The standard (free) Twitter APIs consist of REST APIs and Streaming APIs.

> The enterprise (paid subscription) APIs include filtered firehose, historical search and engagement APIs for deeper data analytics, listening and other enterprise business applications.

> The premium (pay as you go) APIs consist of reliable and affordable versions of enterprise APIs, allowing your business to grow with your usage.

> Additionally, there are some families of APIs (such as the Ads API) which require applications to be whitelisted in order to make use of them.

https://developer.twitter.com/en/developer-terms/agreement-and-policy#f-be-a-good-partner-to-twitter

https://gwu-libraries.github.io/sfm-ui/posts/2017-09-14-twitter-data

Existing Twitter datasets: https://www.docnow.io/catalog/

TweetSets: https://tweetsets.library.gwu.edu/

### Sino Weibo

Much like Twitter, Sino Weibo has an API that you can use directly or through different programming libraries or applications to create new datasets.

You can also use Social Feed Manager as a way to manage your API access.

### Yelp

Yelp makes a relatively large dataset available for educational and academic purposes: https://www.yelp.com/dataset

From the Yelp terms of service (https://www.yelp.com/static?p=tos):

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

## Industry offerings that might be useful

- Discovertext

## An example analysis with Twitter data
