---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Let's rewind climate news history
---

*A data story*

## Abstract

Since 2015 and the Paris Agreements following the COP21, states and citizens are taking the issue of climate change more and more seriously. This has led to strong political movements like the climate strikes initiated by Swedish activist Greta Thunberg. The goal of our project is to rewind the story of climate change through the quotes of multiple newspapers. We will first be interested in identifying what the quotes reveal about the important events related to climate change. Then we will dig into the actors behind the quotes, what type of newspapers have the most quotes and what does this tell us. Are the important newspapers talking about climate change mostly for a sustainable change or rather climate sceptics ?  A focus will be made also on the most important political parties of the speakers in the quotes. Are the speakers mostly democrats or republicans ? Which party is the most represented in the newspapers about climate change ? Finally, these analyses will allow us to have a global overview of how and about what Quotebank quotes talk about regarding climate change. 

# Intro

{% include histogram_quotes.html %}

We can first see the distribution of the number of occurrences of climate quotes through the years of 2015 to 2020. The distribution presents an irregular pattern, we can see that some months have a lot of quotes, mostly due to very famous ones like the one of President Donald Trump in august 2017 when he responded to North Korea’s nuclear threats saying the regime > "will be met with fire, fury and frankly power, the likes of which the world has never seen before.". In 2016 there are only a few quotes due to the fact that the original dataset had fewer quotes this year. 

{% include timeline.html %}



Once those clouds of words generated we can see that some words appear and disapear throughout the years.
Those are particularly nterrested and an be link with events that took places.

For example, in septembre 2019, we can see the word `Greta` and also `child`.

It's impressive 

TODO:Timiline
- Février 2019
  Green deal -> Occasio cortez
- Greta  2019

- Mai 2019
  Rapport IPBES
- August 2019
  Hights 
- Septembre 2019
  Tweet 

- PARIS Agreement missing afor a long time ...

topics détection → 20-30 mots qui décrivent l’ensemble des quotes par mois 
événements qui peuvent ressortir de ca 
liste adjectifs liés aux topics

## Journal analysis

In this second section, we will focus on the newspaper which published those journals. To do so, we analysed who the authors where 



type de journaux : relayeurs d’informations et non pas journaux 
orientation des journaux 
utilisation des citations dans les journaux 

## Who tells the story

We can now wonder which newspapers are behind the climate articles. A lot of sources are websites that convey articles. Two newspapers about climate change that stand out are Breitbart and CarbonBrief. We found out that these two websites had 2 opposite points of view about climate change. Breitbart is fully against climate change awareness whereas CarbonBrief is pro. Let’s summarize the datas about these two newspapers. 

TODO: BREITBART VS CARBON BRIEF

| | Breitbart | CarbonBrief |
|-|-----------|-------------|
| Number of quotes | 40'102 | 8574 |
| Number of unique quotes | 23'185 (~58%) | 8'371 (~98) |

First, we can see that about 40% of Breitbart quotes are reused in different Breitbart articles whereas only around 2% of CarbonBrief quotes are reused by them. This lights out that sources and quotes are more diversified for the Carbon Brief cluster than the one of Breitbart. Breitbart articles rely on the same quotes to argue their point of view while Carbonbrief tries to use different quotes to support their opinions.  

We can make a further analysis between these two newspapers and see if their types of quotes are different or not. 

TODO: CLUSTERS 

Analysis cluster … 

{% include cluster_graph.html %}

We can see in the node graph 3 clusters. The distance between two nodes is the total number of quotes in Breitbart or CarbonBrief articles divided by the number of quotes shared between Breitbart or CarbonBrief and other newspapers.  ~~On one side, one containing Breitbart, on the other side, one containing Carbonbrief and a last one between those two clusters.~~ The Breitbart cluster contains all main quotes exchanged between this website and 50 others. We can see that websites associated with Breitbart represented inside the cluster are for the most climate skeptics newspapers SOURCES. Likewise, most of the websites associated with CarbonBrief are pro-climate websites SOURCES. Also, we can see that the distances between the nodes connected to Breitbart are closer than the ones connected to CarbonBrief. That means that Breitbart shares a lot of quotes with other websites. As pointed out before, this confirms the fact that the newspapers related to Breitbart and Breitbart do not diversify their sources and use the same quotes. For both clusters, we can see newspapers well known as the NewYorkTimes because all newspapers relate important declarations or political decisions. ~~For instance, Paris Agreements or a declaration of the Republic’s president.~~ Finally, the last cluster between those two is corresponding to websites that only relay information like MSN or Yahoo. We can see that Breitbart is more relayed by those types of websites. It can be explained by the twisted choice of articles on those websites made by employees between 2015 and 2020. Since may 2020 for instance, artificial intelligence decides MSN articles. Perhaps, since this reform, information reliability will be more equally distributed between those two newspapers.  


## What about their speakers ? 

Now, we can have a review about speakers in Breitbart and CarbonBrief quotes. Thanks to the wikidata data set, we made a link between quotation speakers and their political orientation. It’s important to take in account that some people have changed their political orientation, so on, some people can be affiliated to more than 1 political orientations. 

HISTOGRAM POLITICAL PARTY SPEAKERS 

{% include pie_breitbart_final.html %}
{% include pie_inside_final.html %}
 
Observing this graph, we can make some analysis. First, Breitbart is more using political personalities than CarbonBrief (Over 80% for Breitbart and only 60% for CarbonBrief). 
Both are using speakers of 2 majors political parts of UK ( Conservative and labour) and USA (Republican and democratic)
Besides, quotations which are related only by Breitbart are 3 times bigger than quotations related only by CarbonBrief.

# Notes










Répartition du nombre de citations par parti politique
Ratio = 27’700 (democrate) VS 15’445 (republicain) = 1.79 VS proportion dans la vraie vie => 34% (democrate) VS 33% (republicain) ~= 1.0
https://news.gallup.com/poll/15370/party-affiliation.aspx
