# campaign_finance_house_2015-2016
Analysis of the effect of campaign contributions and incumbency on the outcome of the 2015-2016 House election cycle

## Introduction

The simultaneous explosive increase in computational capacity and data accessibility in recent decades has driven increased interest in quantitative social sciences in general, and quantitative approaches to political science in particular. Throughout this burgeoning era of Big Data, the general public has shown increasing interest in so-called 'data journalism,' pioneered by such online news outlets as FiveThirtyEight and Vox, which deliver coverage of current events and politics with a heavy emphasis on quantitative evidence in the form of statistical estimates and displays aimed at a non-specialist audience. Given that political datasets are often characterized by a relatively large number of variables (features) and observations, this area of social science is replete with potential applications for a variety of machine learning approaches. The present analysis was undertaken in the spirit of the aforementioned publications with the aim of obtaining a clearer picture of a political issue of longstanding public interest, namely USA federal campaign finance, through the lens of conventional statistical methodology complemented by the use of several supervised machine learning algorithms.

There is a widly held opinion among the American electorate that our federal elections are ‘sold to the highest bidder’ via exorbitant individual and corporate campaign contributions, and that our representatives in the legislative and executive branches may thus be regarded as ‘bought and paid for’ by these powerful entities. Among other advantages, it is clear that outsized campaign donations facilitate promotion and outreach on a scale which is usually inaccessible to candidates who lack wealthy backers, which may be reasonably supposed to skew election outcomes in favor of those candidates with the most generous donors. However, it is conceivable that any among the numerous disparate, non-financial (indeed, often non-quantifiable) factors which might determine whether or not a candidate wins or loses, e.g., voter demography or incumbency, exert a greater influence individually or in concert than campaign funds alone. Moreover, the existence of a strong correlation need not imply causal influence: It stands to reason that greater campaign contributions will tend be invested in candidates who are, for one reason or another, perceived by potential donors as likely to win (re)election. 

In an attempt to clarify these issues, an analysis was undertaken of the 2015-2016 House of Representatives election cycle using data obtained from the Federal Election Commission (FEC). Following extensive processing of the raw data, several traditional statistical methods were employed to visually and quantitatively elucidate key relationships among the variables of interest (particularly incumbency, total received campaign funds, and electoral outcome). Finally, following additional preprocessing, a handful of popular machine learning models were tuned and trained on the data to assess how predictive were the two chosen features.
