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
  - Ethical concerns regarding privacy
- Using existing data
  - There are social media datasets floating around reddit and other places with different amounts of documentation. You have to make a decision about whether they can be used or not based on your use case and discipline. You should absolutely be thinking about how the data was collected and whether use of that data violates legal restrictions or ethical best practices.
  - There are a lot of repositories out there with documented data as well.
  - Many of the existing datasets will not match your particular research question, but you might be able to subset them to create a suitable dataset.
- Creating your own datasets
  - APIs
  - Social Feed Manager
- Opportunities for working directly with companies

## Commonly requested sources

### Facebook

- https://newsroom.fb.com/news/2018/04/restricting-data-access/
- http://theconversation.com/facebooks-data-lockdown-is-a-disaster-for-academic-researchers-94533
- https://developers.facebook.com/docs/graph-api/

First, don't try to scrape Facebook. It won't work and it's definitely against the terms of service. Facebook has put a lot of work into anti-scraping mesures in their page code, and the techniques change often enough that it's not worth investing in workarounds for what's currently in place.

A lot of people are interested in collecting posts from public Facebook Groups. It used to be possible to use a Facebook API to collect this data. After the Cambridge Analytica scandal, Facebook is almost entirely locked down. While the Graph API is still around, you have to establish a Facebook Developer profile for yourself as a business (complete with official business documentation) that's providing services of some sort to users or other businesses to even access the most basic public information for pages.

Existing data: you can find stray Facebook datasets on reddit, data.world, and other places on the internet. However, given the lack of clarity around how the data were collected and such, it's unlikely these could be used publishable research. You can also find occasional datasets released by people who own the Facebook data, such as cities who are providing information about their communications, though this data is often metadata rather the posts and comments themselves.

Collaboration: Facebook periodically puts out RFPs for [research collaborations](https://research.fb.com/programs/). You can sign up for their mailing list to receive the RFPs, but they're focused on technical issues relevant to Facebook's own interests (including things like multilingual NLP, but not sociocultural phenomena).

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

### Yelp

Yelp makes a relatively large dataset available for educational and academic purposes: https://www.yelp.com/dataset

From the Yelp terms of service (https://www.yelp.com/static?p=tos):

> You also agree not to, and will not assist, encourage, or enable others to:

> Use any robot, spider, site search/retrieval application, or other automated device, process or means to access, retrieve, scrape, or index any portion of the Site or any Site Content;

### Spotify (include this or not?)

## Places to search for data

- https://archive.ics.uci.edu/ml/index.php
- https://snap.stanford.edu/data/
- http://socialcomputing.asu.edu/pages/datasets

## An example analysis with Twitter data
