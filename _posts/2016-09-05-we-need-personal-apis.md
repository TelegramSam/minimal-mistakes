---
layout: post
published: true
title: We Need Personal APIs
---
![citylights.jpg]({{site.baseurl}}/media/citylights.jpg)

Imagine a world where only businesses had phone numbers. You can call any business you like, but connecting a phone call to *another person* requires that you ask a business to help you. Businesses can't call us either, so the only way to have phone calls is to stay on the line with a business in case somebody wants to talk. If both you and I are connected on the phone to the same business, we can ask to be connected, and *then* we can talk. The business may place restrictions on our phone call, including which words we can speak and the length of the call. They may even regularly interrupt the call with advertisements to 'enhance our experience.'

This scenario might sound completely ludicrous, but we are all living in a reality that functions just this way. We all have apps on our phones that stay connected to Facebook, Snapchat, and Instagram. We get our updates through the app. Our contacts are all maintained in the app, and our communication is required to fit the requirements of the apps that we use.

**Imagine if your phone calls were 'algorithmically rearranged' for your convenience.**

None of us would put up with our voice calls being interfered with in this manner, but we don't think twice about allowing our other forms of communication to exist in such a perverse way.

## We Need Phone Numbers
To solve this problem, we need a way to communicate **directly** in all forms of our communication. Software talks to other software via APIs, allowing systems to coordinate, automate, and share data. APIs already exist all over the internet, but only businesses have them. Your Facebook app on your phone calls a Facebook API on Facebook's servers to load information. Businesses communicate with other businesses with APIs. I use a Business called IFTTT to repost my Instagram Posts to Facebook.

The existence and use of all these Business APIs is **great**. The Internet is a much better place with these APIs in use. What we need is a way for businesses (and other people) to call us, to call *our* API.

**In order to be first class citizens in the api economy, we must have APIs ourselves.**

Remaining in our current state will only further cement our position as 'assets' to the business who sell access to our eyeballs and tightly control the data behind their APIs.

## A Loose Beginning to Personal APIs
The first blog post that I read mentioning Personal APIs was written in 2013 by Foursquare co-founder Naveen Selvadurai. He wrote about [tracking personal metrics][naveen] in one place, and posted the start of a [personal data aggregation api][naveenapi] that appears to no longer work. Naveen's work demonstrates the value of an aggregated Personal API. A user of his API does not need to know where the data originated, leaving Naveen in control of the interaction. Indeed the backend host of the data could change without changing the API interface in any way.

This was followed up a few months later with a post on ReadWrite titled [Want To Reach Me? Call My API][rw]. Naveen's API was read only, but ReadWrite author Brian Proffitt expanded the concept from data sharing to a request for interaction. Having a read/write API allows for conversations and transactions to occur that extend far beyond the concept of data sharing.

There has been other related work which I will address in future posts, but for now, I want to focus on these two main points: an aggregated api, and the ability to have conversations. While data sharing is valuable, I believe the ability to have conversations is the greatest of these two.

**Personal APIs are NOT about data, they are about conversations. Even if those conversations are about data.**

Much work has gone into data sharing and authorization and delegation protocols. This is valuable work. Personal APIs have the potential to move beyond data sharing and synchronization and into a world where regular API conversations occur from businesses to people, and between people directly. 

Brian highlighted a perfect example of such an exchange in [his post][rw] when he dreams about coordinated personal communication. I can envision a future where an API exchange happens prior to placing a phone call. It might look something like this, in a conversation between my phone and my friend Kurtis's Personal API:

	MyPhone: Hey KurtisAPI, Sam wants to talk on the phone.
    //KurtisAPI does some status checking for Kurtis's personal location, phone status, and preferences.
    KurtisAPI: Now's not great, but Kurtis should be available in the next half hour.
    //MyPhone asks me if sometime in the next half hour would work. I say yes.
    MyPhone: Please register a low-priority request for a call back within the next hour.
    KurtisAPI: Request received.
    //MyPhone displays a message to me that a callback request has been made.
    
I took some liberties for the sake of brevity, but I believe the main idea is clear. Consider the advantages of this approach:

- Kurtis was not directly interrupted during this exchange.
- None of Kurtis's private information such as location or phone call state was shared.
- This exchange was faster than actually talking with Kurtis and coordinating the same thing.
- Kurtis now can be automatically notified of the call request when his own systems determine the appropriate time to interrupt him.
- This exchange didn't require the cooperation of any 3rd party apps or businesses.

There are many scenarios that describe the value of Personal APIs, and I hope to explore them in future posts. I will also explore the complexities and challenges of Personal API implementation. I hope you will join in this conversation with me as we explore and develop the possibilities.

Thanks to [Phil Windley][pjw] and [Kurtis Welch][kw], whose conversations have contributed significantly to clarity in thinking.

[naveen]: http://x.naveen.com/post/51808692792/a-personal-api
[naveenapi]: http://api.naveen.com/
[rw]: http://readwrite.com/2013/08/23/building-personal-api/
[kw]: https://twitter.com/hclewk_
[pjw]: http://www.windley.com/
