---
layout: post
title: To Report or Not to Report?
subtitle: That is a tough question
categories: blog
author: Vlad Styran
excerpt_separator: <!-- more -->
---
Recently we were discussing a pentest report with one of our new customers when suddenly the client's Authorized Single Point of Contact, or SPoC as we usually call those folks, has stopped in the middle of the phrase and asked:

> Guys, why are you reporting only the *serious* stuff?…

<!-- more -->

Frankly, it took me a second or two to react. I do pentesting for quite a while now, but this was the first time I've been asked a question like that. The client had some experience with other pentesters before us, and when I kindly asked to clarify the question, he explained that previously they had much longer reports containing mostly SSL-related issues.

As a pentester and a former auditor, I've done a lot of reporting in my life and I've seen many reports written by others. I won't describe the emotions caused by reading through an 8-page results of a full scope pentest report of a major cellular carrier, or 300+ pages of an application security audit for an Android app. Let's just say that the effect may vary. And that the choice of which issues to report and to what detail can be made poorly.

Regarding the "short" reports that basically don't contain anything beyond "we've done this and that and here is the result", there's actually nothing to say: the lack of methodology results in poor reporting. Googling for default credentials is deemed an advanced technique in this case. So let's just leave it behind.

The other case, the one our client has apparently been a victim to, results from the pentester's access to a variety of automated vulnerability enumeration tools and his desire to include *all* vulnerabilities into the report. If you are a pentester who does a bit more than reformatting vulnerability scanner reports, you know that feeling: there is always one too many issues. Normally some aggregation saves the day. But for someone who knows some script-fu and likes to automate as much as possible, this might be less of a problem. As a result, in the end of the day everything finds its rightful place in the pentest report, marked by different level of "certainty" according to whether a human being actually got the hands on issue validation.

So should we exclude certain issues from the report? And if yes, how do we decide on what to report and what not? The short answer is: it depends on the  context, but I'm sure you won't be satisfied by that.

During my career, I have developed a set of criteria which are based on the Threat Model that is created somewhere along the recon and enumeration activities and the gut feeling that I assume while playing around the system or application at hand. But one thing is constant: there are plenty of "standard" issues that are getting too much of attention. There is absolutely no need to cover all SSL misconfigurations, weak ciphers, and outdated versions one by one, covering as much paper with that as possible. These things shall be aggregated and only client-specific vulnerabilities shall be described in big detail while supporting the well-known issues by referring to public sources of information.

At least, this is how we do it. This could be hard, especially when the client has its own *understanding* of how the report should look like. In such cases arguing is not the right way to go: we prefer to either do it the client's way, or, if the situation demands that, create two reports to clearly articulate the "serious stuff".

…And by the way, we are not alone there. There is a list of Common "Non-qualifying" Submission Types in the [Bugcrowd's Standard Disclosure Terms](https://bugcrowd.com/resources/standard-disclosure-terms), I bet other bounty brokers may also have something similar.
