---
title: "Using school-household networks to understand transmission dynamics"
layout: post
date: 2024-05-13
tag: jekyll
image: false
headerImage: false
projects: true
hidden: true # don't count this post in blog pagination
description: "Using school-household networks to understand transmission dynamics"
category: project
author: jamesmunday
externalLink: false
---

## Background
To evaluate the risk of transmission between school populations, we constructed a network of schools as linked through households. Each edge on the network is weighted by the number of unique contacts between schools that occur through shared households, for example: In household x, 2 children attend school A and 2 children attend school B, there are therefore 4 unique contacts between school A and school B. The sum of all households that form such a link gives the total number of unique contacts between schools A and B, we denote this as $C_{ij}$. 

![alt text](../Figures/NetworkSchematic.jpg "Title")
<br>
*A network of schools linked by households A) A network of schools constructed such that schools are connected when contact is made between pupils of different schools within a household. B) The strength of contact between schools is quantified by calculating the number of unique contact pairs (one child in each school). The number of pairs per household is the product of the number of children who attend school a and the number of children who attend school b. The total number of unique pairs is the sum of unique pairs in each household with children attend both school a and b.*

From this network we can estimate the probability of transmission between schools and simulate outbreaks on this network by sampling instances of 'binary transmission networks', where transmission between each pair of schools either occurs (edge weight of 1) of does not occur (edge weight 0). The network final outbreak size is calculated for an outbreak seeded by each school by finding the connected component of the binary transmission network. 

## Evaluating school closures/ Reopening 
During the COVID-19 pandemic we used this framework to evaluate risk of reopening particular school years to the overall transmission risk across the network. This work revealed the relative importance of secondary school pupils in providing routes of transmission between schools. We found that reopening primary schools would likely have a limited impact on transmission beyond local outbreaks within schools, however reopening secondary schools was capable of providing long range chains of transmission which could stretch actross the country. See our paper in [*Nature Comminications*](https://doi.org/10.1038/s41467-021-22213-0).


![alt text](../Figures/SchoolClosure.jpg "Title")
<br>
*The number of households with children attending a school in each largest connected component of the binary transmission networks (estimated potential outbreak cluster size) generated from transmission probability networks for school reopening scenarios. The points show the median and error bars show the 90% credible intervals for 1000 realisations of binary outbreak networks. The green dashed line shows the total number of households in the school system (4,927,163 households).*

### Measels in the Netherlands
We also applied the method to study Measles in the Netherlands, where unvaccinated children cluster strongly within schools, particularly those with an affiliation to Anthroposophic and Orthodox Protestant communities. We showed that dispite very high uptake in the rest of the population, school and household contacts are sufficient to explain differences between the large outbreak observed in 2013/14 vs smaller outbreaks in previous years based on the school that the outbreak was initiated. See our preprint in [*MedRXiv*](https://www.medrxiv.org/content/10.1101/2024.02.20.24302866v1.article-info).


![alt text](../Figures/GiantComponent.jpg "Title") 
<br>


