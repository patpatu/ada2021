---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Let’s rewind climate history 
---

*A data story*

## Abstract

Since 2015 and the Paris Agreements following the COP21, states and citizens are taking the issue of **climate change** more and more seriously. This has led to strong political movements like the climate strikes initiated by Swedish activist Greta Thunberg. The goal of our project is to rewind the story of climate change through the quotes of multiple newspapers. 

We will first be interested in identifying what the quotes reveal about the important events related to climate change. Then we will dig into the actors behind the quotes. We will ask ourseleves if the important newspapers talking about climate change are mostly for a sustainable change or are rather climate sceptics.  A focus will be made also on the most important political parties of the speakers in the quotes. Are the speakers mostly democrats or republicans ? Finally, these analyses will allow us to have a global overview of how and about what Quotebank quotes talk about regarding climate change.

## A little overview

We can first see the distribution of the number of occurrences of climate quotes through the years of 2015 to 2020. The distribution presents an irregular pattern, we can see that some months have a lot of quotes, mostly due to very famous ones like the one of President Donald Trump in august 2017 when he responded to North Korea’s nuclear threats saying that the regime

> "will be met with fire, fury and frankly power, the likes of which the world has never seen before."

In 2016 there are only a few quotes due to the fact that the original dataset had fewer quotes this year. 

{% include histogram_quotes.html %}

## The quotes’ story of climate change 

We can now try to retrace the history of climate change viewed by the quotes. To do so, a typical language processing task will be solved :  **topic detection**. We represented the topic of each month in word clouds of 20 words and then tried to connect these words to an event that happened that month. The size of the word is proportional to the degree to which the month’s quotes represent that particular topic. The timeline below shows the results of our unsupervised learning. 

{% include timeline.html %}

It is interesting to see that we can retrace most of the important events that happened through the years thanks to only 20 words. It is pretty remarkable, for the years with low data how we can reconstitute a sentence that corresponds to a specific event that happened that month, like for example the photo of the signature of the Paris Agreement's pact on a friday in april. However, the more the quotes the more difficult it is to connect a specific event to the month’s quotes as the topic is getting more general.

We can see that the word ‘Trump’ appear a lot in the word clouds. This is naturally due to the fact that President Donald Trump is very publicized and cited a lot in the quotes. The word clouds reveal also that the Paris Agreement has an important media coverage in the english newspapers.  We were also a little surprised by the fact that Greta Thunberg does not appear once in the word clouds as we think she became important in the figth for action for climate change these past few years. This means that she is maybe not as cited as we thought in the quotes. Naturally, a lot of general words like 'people', 'like', 'world' , 'time' appear a lot in the word clouds and make the analysis a bit harder. When the word cloud has mostly general words it is pretty impossible to retrace a specific event and there are many possibilities.

Also, a lot of the events that we were able to extract from the word clouds are related to big climate protests or climate disasters which are very publicized events related to climate change. 


## Who tells the story ?

### The types of newspapers 

We can now wonder which newspapers are behind the climate quotes. A lot of sources with an important share of climate quotes are websites that convey articles. These types of newspapers mostly convey articles about trendy topics from other newspapers. This emphasises the fact that climate change became very trendy these past few years. Two american newspapers that stand out by their number of climate quotes are Breitbart and InsideClimateNews. We found out that these two websites had 2 opposite points of view about climate change and thought it was interesting to compare these two. Breitbart is fully against climate change actions whereas InsideClimateNews is pro. The tables below show the top 10 

Breitbart
| Websites          | Number of shared quotes |
|---------------------|-------|
| yahoo.com           | 5180 |
| msn.com             | 4691 |
| news12.com          | 4370 |
| kdhnews.com         | 4183 |
| seattletimes.com    | 3817 |
| sfgate.com          | 3810 |
| startribune.com     | 3623 |
| washingtontimes.com | 3609 |
| wftv.com            | 3524 |
| wtop.com            | 3338 |

InsideClimateNews
| Websites            | count |
|---------------------|-------|
| environmentalhealthnews.org   | 2675 |
| dailyclimate.org              | 2644 |
| nytimes.com                   | 1864 |
| msn.com                       | 1807 |
| yahoo.com                     | 1230 |
| thehill.com                   | 1142 |
| startribune.com                | 914 |
| seattletimes.com               | 820 |
| breitbart.com                  | 805 |
| sfgate.com                     | 804 |

Most cited websites 
| Websites            | count |
|---------------------|-------|
| msn.com             | 1106632 |
| investing.com        | 475852 |
| jdsupra.com          | 319747 |
| wokv.com             | 215855 |
| krmg.com             | 192553 |
| news965.com          | 174527 |
| wsbradio.com         | 157839 |
| independent.co.uk     | 58124 |
| yahoo.com             | 57526 |
| salon.com             | 57224 |

### Breitbart VS InsideClimateNews

| | Breitbart | InsideClimateNews |
|-|-----------|-------------|
| Number of quotes | 40'102 | 21'202 |
| Number of unique quotes | 23'185 (~58%) | 19'973 (~94) |

First, we can see that about **42%** of Breitbart quotes are reused in different Breitbart articles whereas only around **6%** of CarbonBrief quotes are reused by them. This lights out that sources and quotes are more **diversified** for InsideClimateNews than Breitbart. Breitbart articles rely on the same quotes to argue their point of view while InsideClimateNews tries to use different quotes to support their opinions.  

### The newspapers in clusters 

An interesting analysis could be to see how the newspapers are linked together. 

{% include cluster_graph.html %}

- We can see in the node graph three clusters. If two nodes are linked this means that they share some same quotes. The distance between two nodes is for Breitbart the total number of quotes in Breitbart's articles divided by the number of quotes shared between Breitbart and  50 other newspapers. The same applies for InsideClimateNews.

- At first sight, this graph points out the fact that Breitbart and InsideClimateNews do not share a lot of quotes, only **30%** of the total number of quotes are shared between these two newspapers. This is interesting as it demonstrates the fact that their articles that have the same main topic which is climate change have different quotes. The newspapers that share the same quotes between Breitbart and InsideClimateNews are mostly websites that convey articles like Yahoo or ExpressNews. This same cluster is at the same distance from Breitbart than from InsideClimateNews, this means that the newspapers in this cluster relay the same amount of quotes from the pro climate newspaper as from the climate sceptik one. 

- We can see that websites associated with Breitbart represented inside the cluster are for the most climate skeptics newspapers like FoxNews or other newspapers that belongs to FowNews like Fox23 or NewsAdvance. Likewise, most of the websites associated with InsideClimateNews are pro-climate like WashingtonPost or the NyTimes. Also, we can see that the distances between the nodes connected to Breitbart are closer than the ones connected to InsideClimateNews. That means that Breitbart shares a lot of quotes with other websites. As pointed out before, this confirms the fact that the newspapers related to Breitbart and Breitbart do not diversify their sources and use the same quotes.


### Inside Breitbart and InsideClimateNews' quotes

We then try to differentiate those two newspapers by analysing their quotes. Is there a different content, a different sentimental score ? The sentimental analysis of positive and negative scores of both journals is not significant, they have quite the same results of score, mean, variance, even median. However we computed the TF-IDF matrix for both journals each year and we obtained the following results. The TF-IDF matrix gives a score for each word reflecting the rarity of a word. A word with a high score is used a lot in a quote but not in all the quotes. So a high score for a word represents his significance. You can see above a list of top scored words for all the quotations of Breibart and InsideClimateNews from 2015 to 2020. 


## What about their speakers ? 

Now, we can have a review about speakers in Breitbart and InsideClimateNews quotes. Thanks to the wikidata data set, we made a link between the quotes' speakers and their political orientation. It’s important to take into account the fact that some people have changed their political orientation, so on, some people can be affiliated to more than one political orientation. 

{% include pie_breitbart_final.html %}
{% include pie_inside_final.html %}
 
- We can first notice that Breitbart and InsideClimateNews both have the same percentage of speakers for which we identified a political party, 69% for Breitbart and 62% for InsideClimateNews. This illustrates how politicized is the subject of climate change.  

- Both newspapers' speakers are for the majority from the two important political parties of the USA, the Republican and the Democratic parties. This shows the importance of these political parties in these two american newspapers. It is interesting, but not very surprising to notice that Breitbart is the only newspaper that has the Independent Party of America represented which is a party that is openly against climate change.

- Breitbart has more than 41% of their quotes' speakers that belong to american’s political parties whereas InsideClimateNews only has 21% that does. In the category other parties, political parties from many countries are represented like the english Conservative party or the french one La République en Marche. This shows that even though the two newspapers are american, one diversifies more his speakers than the other. InsideClimateNews gives a more global overview of climate change referring speakers from all over the world in his articles than Breitbart. 


