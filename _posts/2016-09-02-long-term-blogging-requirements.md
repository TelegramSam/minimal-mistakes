---
layout: post
published: true
title: Long Term Blogging Requirements
---
I've maintained the code for a blog before, which led me use a hosted solution. That hosted solution was shuttered following an acquisition. I'm now attempting to navigate the gap between inventing my own and leaving myself vulnerable to service shutdown. Here are some of my thoughts on how to navigate this gap.

## Fail Open

The frustrating shutdown of a service would be made nicer if the existing content remained in place, rendered statically and available for the future. This sort of happened with the Posterous service. A site called PostHaven popped up immediately that would import Posterous sites. It is still live, and they have adopted the 'forever' principle into their [current operations][posterous]. **If the software that generates the site fails or is no longer maintained, the site should exist in it's current state.** Forever if possible.

## Cheap and Easy
If I want my content to last forever, it has to be cheap, and it has to be easy. Our [family adventure blog][cw] runs on hosted WordPress, but it's an active site that is worth having on a more capable platform. My personal blog will receive much less attention, and needs to not be a financial burden. It must also not consume undue amounts of time to maintain. I don't mind the occasional fix, but I don't want to spend lots of time to keep it up. Installing security patches or having the blog compromised is a painful time-suck.

## Future Friendly
The single most important requirement here is to have long-lived URLs. Changing URLs breaks things, and that must not happen if the host or tools change.

My first blog stored content in a relational database, which is both unnecessarily complicated and unnecessary. **Simple data storage** means it can be easily used by **multiple tools**. **Low host requirements** make it easy to move the blog to a new host if necessary. Finally, I want **low client-side requirements** for any software needed to update the blog. Ideally, only a browser would be the only required client-side tool.

## Jekyll: Almost good enough
Anybody familiar with the [Jekyll] static site generator will realize that it fills many of my requirements. Indeed, Jekyll is closer to my ideals than anything else I can find. It does fail spectacularly in the client-requirements requirement however, with poor Windows support and locally installed Ruby with a collection of Ruby libraries.

Where Jekyll really shines is the format used for storing blog posts. Meaningful filenames in various markup languages annotated with frontmatter. The site can be generated from these files, a few config options, and a few template files. I consider this format to be extremely **future friendly**, and plan for it to be part of my long term solution.

## Now
I'm using Github pages, which has built in Jekyll support without a local Jekyll install. I'm using a custom domain to allow moving the content to another host in the future. I'm using [prose.io][prose] as an editing tool for the content on GitHub. Prose.io has a great file editor, draft automation, and even media upload. For now, this is a good-enough solution that reserves plenty of flexibility for the future.

## Later
I have a vision in my mind (and even a bit of code) of a Chrome extension that maintains a Jekyll blog hosted on S3. This would keep the client requirements low, use the same future friendly file format, and be cheap and trouble free to maintain. This would be a javascript port, and so could not maintain perfect Jekyll compatibility. It would be much easier to use than jekyll but have more full featured options than allowed by GitHub Pages. This vision would allow migration from my current situation when the project reaches sufficient maturity. Timeline? No idea, but it heavily depends on the comfort of my current setup.

[posterous]: https://posthaven.com/our_pledge
[cw]: http://www.currentlywandering.com
[jekyll]: https://jekyllrb.com/
[prose]: http://prose.io/
