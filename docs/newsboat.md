---
layout: default
title: Newsboat
---


# Newsboat

Newsboat is a simple command-line-based software that
handles RSS Feeds. This is ideal for staying up-to-date
with current research.

[Newsboat Documentation](https://newsboat.org/releases/2.27/docs/newsboat.html)

You will need two files, a config file that contains a specific
set of command definition and a a file that contains
URLs

<details>

<summary> <code>.newsboat/config</code> </summary>

<code>
browser "open -a safari '%u'"
<code>

</details>


<details>

<summary> <code>.newsboat/urls</code> </summary>

<code>
https://academic.oup.com/rss/site_5282/3148.xml
http://feeds.nature.com/nature/rss/current
http://feeds.nature.com/ncomms/rss/current
http://feeds.nature.com/ngeo/rss/current
http://feeds.nature.com/natecolevol/rss/current
https://www.science.org/action/showFeed?type=etoc&feed=rss&jc=sciadv
https://www.science.org/action/showFeed?type=etoc&feed=rss&jc=science
https://agupubs.onlinelibrary.wiley.com/feed/21699011/most-recent
https://agupubs.onlinelibrary.wiley.com/feed/21699356/most-recent
https://agupubs.onlinelibrary.wiley.com/feed/21698961/most-recent
https://agupubs.onlinelibrary.wiley.com/feed/21699291/most-recent
https://agupubs.onlinelibrary.wiley.com/feed/19448007/most-recent
https://pubs.geoscienceworld.org/rss/site_69/advanceAccess_35.xml
https://pubs.geoscienceworld.org/rss/site_69/35.xml
https://pubs.geoscienceworld.org/rss/site_65/advanceAccess_33.xml
https://pubs.geoscienceworld.org/rss/site_65/33.xml
https://www.cambridge.org/core/rss/product/id/277295E1DFDC1E4700796E746AE514CC
https://www.cambridge.org/core/rss/product/id/56B1B6F705BBEC4F8958383925A06535
https://onlinelibrary.wiley.com/feed/14754983/most-recent
https://www.cambridge.org/core/rss/product/id/A8663E6BE4FB448BB17B22761D7932B9
https://pubs.geoscienceworld.org/rss/site_135/68.xml
https://www.pnas.org/action/showFeed?type=etoc&feed=rss&jc=PNAS
https://academic.oup.com/rss/site_6448/4114.xml
https://academic.oup.com/rss/site_6448/advanceAccess_4114.xml
https://onlinelibrary.wiley.com/feed/15585646/most-recent
https://www.mdpi.com/rss/journal/remotesensing~
</code>

</details>


