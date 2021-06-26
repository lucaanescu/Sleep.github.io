---
layout: post
title: Genetics and Religion correlation
subtitle: Are genetics and religious belief connected in their aproval rates?
tags: python, other
---

Is genetic research being held back by religion?

In recent times, humans have been editing the genetics of their children to varying effects to prevent certain hereditary medical conditions such as blindness, AIDS, and even cancer.
However, despite the progress of modern medicine there are still many moral implications to scenarios such as this. The idea of genetically altering oneself to have improved genetics did not strike accord with many individuals.

The question remained of which individuals are most opposed to the idea. The statistics will aim to test whether religious beliefs are more inclined to make individuals less accepting of genetic modification.
Historically, religious groups have been opposed to certain scientific experimentation. This could be something they would widely be opposed to. The data is recorded of those who are religious and if they would approve of genetic modification.

Data was pulled from Pewresearch.org among Global media surveys and Public views to discover percentages of population that correlated with the assigned attributes. The data is split between nations that the sources had data taken from.

H0 : µ = There is a correlation between religious groups and their willingness to genetically modify their children
Ha : µ ≠ There is no correlation between religious groups and their willingness to modify their children generically

A T test was performed to find the median of both Yes and No from these groups.
Around 12,000 responses with an estimate of 1,000 for each major country / region.

1,000 USA
1,000 UK
1,000 France
1,000 Germany
1,000 India
1,000 Canada
1,000 South Korea
1,000 Taiwan
1,000 Italy
1,000 Brazil
1,000 Sweden
1,000 Spain

Next are rough estimates of survey takers split of approval rates in using genetic modification:

   Good							Bad
   
USA: 560            240

UK: 340             580

France: 160         750

Germany: 280        680

India: 560          240

Canada: 300         620

South Korea: 470    480

Taiwan: 440         470

Italy: 210          680

Brazil: 250         660

Sweden: 290         630

Spain: 320          570

A more compiled median of the data on a box plot.

![relNo](https://user-images.githubusercontent.com/48320567/110399131-4395ff80-8043-11eb-9164-260e2d8de0bd.PNG)

The data is the consolidated in means within the numbers of approvals and disapprovals.

Bad: 550.0

Good: 348.3

Religious: 282.5

ReligiousNS: 702.5

Median of more educated that approve: 683.333333

Median of less educated that approve: 755.833333

Median age or younger approve: 780.0

Older than median approve  -  658.333333

Looking through the results of the means, it appears that some opinions on average are much more prevalent than others. Those who see genetic modification as a good thing are much lower on average than those who see it as a bad thing. While on average, those of a younger age are much more supportive of the idea than those of an older age.
These results are likely to influence the charts of the crosstab examination.
Next is the percentages of religious beliefs separated by nations. The numbers display if an individual is both religious and believes that humans evolved over time.

   Religious						Non-Religious
   
USA: 210                     790

UK: 270                      730

France: 160                  840

Germany: 250                 750

India: 570                   250

Canada: 230                  770

South Korea: 390             610

Taiwan: 390                  610

Italy: 180                   820

Brazil: 240                  760

Sweden: 210                  790

Spain: 290                   710



Means:

Bad: 550.0

Good: 348.3

Religious: 282.5

ReligiousNS: 702.5

T test category:

Good/Bad T test: pvalue=0.0032

Religious / Religious T test: pvalue=2.2310e-07

Religious/ Bad T test: pvalue=0.0316

Good / Non-Religious T test: pvalue=0.2054

Bad / Non-Religious T test: pvalue=0.0002

Good / Religious T test: pvalue=5.6002e-06

The P value of the combined good and bad graphs is quite low showing the connection between the two. The more interesting values are that of the Bad / Religious groups with such a small connection that it seems nearly evident the graphs are connected. Mean while the values for approving of genetic modification and being religious are quite high, showing a very weak connection.

The issue that arises here is that the data is a bit too generalized and it would be clearer how the two are connected via a Chi square test to examine the categorical data more clearly.
Crosstabing the values of the charts, we can see a few things in the fact that both Good / Religious and Bad / Non-Religious share a similar value due to what is likely the fact religious individuals dislike the idea of genetic modification as the value is lower than those who do not approve of it and are religious.

Good / Religious: 24.2
Good / Non-Religious: 30.4
Bad / Religious: 30.4
Bad / Non-Religious: 24.2


![download - 2021-03-08T035219 830](https://user-images.githubusercontent.com/48320567/110390319-cfa02b00-8033-11eb-9849-fefed2d3e0aa.png)


The Chi-square test allowed for much clearer results and a more concrete correlation to the idea that religious groups reject the idea of genetic modification.

On further Examination of the Confidence intervals, it is revealed that with a confidence interval of 95% the results deviate a bit.


Good lower: 280.49213 Good upper: 416.174536
Bad lower: 464.09964 Bad lower: 635.90036
Religious lower: 222.441917 Religious upper: 342.558083
Non-Religious lower: 619.665854 Non-Religious upper: 785.334146

The final steps were to ensure the multiple linear regressions yeilded relevant values. As they were examined, they have been shown to hold values close to one and higher than 0.


Non-Religious and Good = 0.435

Religious and Good = 0.449

Religious and Bad = 0.513

Non-Religious and Bad = 0.423


-
In Conclusion
-

With this information, we fail to reject the null hypothesis as we have proven that religious groups are more inclined to disapprove of genetic modification than non-religious groups.

There is deffinetively a connection between religious groups and the genetic modification of the young due to high R values and relevant means associated with their respective values.
