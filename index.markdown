---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: EQuotes, vision of climate change through quotes
---

*A data story*

## Abstract

Since 2015 and the Paris Agreements following the COP21, states and citizens are taking the issue of **climate change** more and more seriously. This has led to strong political movements like the climate strikes initiated by Swedish activist Greta Thunberg. The goal of our project is to rewind the story of climate change through the quotes of multiple newspapers. 

We will first be interested in identifying what the quotes reveal about the important events related to climate change. Then we will dig into the actors behind the quotes. We will ask ourseleves if the important newspapers talking about climate change are mostly for a sustainable change or are rather climate sceptics.  A focus will be made also on the most important political parties of the speakers in the quotes. Are the speakers mostly democrats or republicans ? Finally, these analyses will allow us to have a global overview of how and about what Quotebank quotes talk about regarding climate change.

## A little overview

We can first see the distribution of the number of occurrences of climate quotes through the years of 2015 to 2020. The distribution presents an irregular pattern, we can see that some months have a lot of quotes, mostly due to very famous ones like the one of President Donald Trump in august 2017 when he responded to North Korea’s nuclear threats saying the regime > "will be met with fire, fury and frankly power, the likes of which the world has never seen before.". In 2016 there are only a few quotes due to the fact that the original dataset had fewer quotes this year. 

{% include histogram_quotes.html %}

## The quotes’ story of climate change 

We can now try to retrace the history of climate change viewed by the quotes. To do so, a typical language processing task will be solved :  **topic detection** . Multiple Python libraries like spacy, nltk, gensim and sklearn were used to tokenize the words in the quotes, lemmatize the tokens and remove the stop words. Latent Dirichlet Allocation will be used as the topic model to split each month of every year as a topic represented by 20 key words. We represented the topic of each month in word clouds, the size of the word being proportional to the degree to which the month’s quotes represent that particular topic. The timeline below shows the results of our unsupervised learning. 

{% include timeline.html %}

It is interesting to see that we can retrace most of the important events that happened through the years. However, the more there are quotes the more difficult it is to connect a specific event to the month’s quotes as the topic is getting more general. We can see that the words ‘Trump’ and ‘Paris Agreement’ appear a lot in the word clouds. This can be explained by the fact that President Donald Trump is very publicized as well as the Paris Agreement. Also, a lot of the events that we were able to extract from the topics are related to big protests or climate disasters.  

## Who tells the story ?

### Which type of newspaper is telling the story ?

We can now wonder which newspapers are behind the climate quotes. A lot of sources are websites that convey articles. Two american newspapers that stand out by their number of climate quotes are Breitbart and InsideClimateNews. We found out that these two websites had 2 opposite points of view about climate change and thought it was interesting to compare these two. Breitbart is fully against climate change actions whereas InsideClimateNews is pro.

### Breitbart VS InsideClimateNews

| | Breitbart | InsideClimateNews |
|-|-----------|-------------|
| Number of quotes | 40'102 | 21'202 |
| Number of unique quotes | 23'185 (~58%) | 19'973 (~94) |

First, we can see that about **42%** of Breitbart quotes are reused in different Breitbart articles whereas only around **6%** of CarbonBrief quotes are reused by them. This lights out that sources and quotes are more *diversified* for the InsideClimateNews cluster than the one of Breitbart. Breitbart articles rely on the same quotes to argue their point of view while InsideClimateNews tries to use different quotes to support their opinions.  

### The newspapers in clusters 

An interesting analysis could be to see how the newspapers are linked together. 

{% include cluster_graph.html %}

We can see in the node graph three clusters. The distance between two nodes is the total number of quotes in Breitbart or InsideClimateNews’ articles divided by the number of quotes shared between Breitbart or InsideClimateNews and other newspapers. If two nodes are linked this means that they share quotes. The Breitbart cluster contains all main quotes exchanged between his website and 50 others. The same applies for InsideClimateNews.At first sight, this graph points out the fact that Breitbart and InsideClimateNews do not share a lot of quotes. We can see that websites associated with Breitbart represented inside the cluster are for the most climate skeptics newspapers. Likewise, most of the websites associated with InsideClimateNews are pro-climate. Also, we can see that the distances between the nodes connected to Breitbart are closer than the ones connected to InsideClimateNews. That means that Breitbart shares a lot of quotes with other websites. As pointed out before, this confirms the fact that the newspapers related to Breitbart and Breitbart do not diversify their sources and use the same quotes. About the newspapers shared by both clusters, we can see that they are well known like the ny daily news because all newspapers relate important declarations or political decisions.


### Inside Breitbart and InsideClimateNews' quotes

We then try to differentiate those two newspapers by analysing their quotes. Is there a different content, a different sentimental score ? The sentimental analysis of positive and negative scores of both journals is not significant, they have quite the same results of score, mean, variance, even median. However we computed the TF-IDF matrix for both journals each year and we obtained the following results. The TF-IDF matrix gives a score for each word reflecting the rarity of a word. A word with a high score is used a lot in a quote but not in all the quotes. So a high score for a word represents his significance. You can see above a list of top scored words for all the quotations of Breibart and InsideClimateNews from 2015 to 2020. 


## What about their speakers ? 

Now, we can have a review about speakers in Breitbart and InsideClimateNews quotes. Thanks to the wikidata data set, we made a link between the quotes' speakers and their political orientation. It’s important to take in account that some people have changed their political orientation, so on, some people can be affiliated to more than 1 political orientation. 

{% include pie_breitbart_final.html %}
{% include pie_inside_final.html %}
 
- First, Breitbart is using political opinions the same as InsideClimateNews ( 69% for Breitbart and 62% for InsideClimateNews). This means that every speaker who has been identified into the data set can be affiliated to political opinions. No speakers can be either random people in the street or personality quotations which can not be identified. Those political identifications have been made for every political party or opinions everywhere in the world. 

- Both newspapers are using speakers of 2 major political parts of the USA (Republican and democratic). This choice represents the importance of those two political parties into American society. They are the most representative at the United States Congress. But Breitbart is the only newspaper exposure for the Independent Party of America which is openly against climate change. In total, 

- In total, Breitbart allocates more than 41% of their speakers' quotations to Americain’s political opinions while InsideClimateNews allocates only 21% looks more open minded on word opinions. We effectively ascertain that they use more quotations about people affiliated at foreign parties (more than 40%). Instead, Breitbart is only using 27% of those. InsideClimateNews looks to give a global world vision of Global Warming political debate whereas Breitbart is giving for the most an american vision of this debate.



