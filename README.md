## Campaign Finance Analysis Pilot Project
Proof of concept pilot analysis of the effect of campaign contributions and incumbency on the outcome of the 2016 House election

### Introduction

The simultaneous explosive increase in computational capacity and data accessibility in recent decades has driven increased academic interest in quantitative approaches to social science research, particularly in the field of political science. Throughout this burgeoning era of big data, the general public has displayed a keen interest in so-called 'data journalism,' pioneered by such online news outlets as FiveThirtyEight and Vox, which deliver coverage of current events and politics with a heavy emphasis on quantitative evidence in the form of statistical estimates and displays aimed at a non-specialist audience. Given that political datasets are often characterized by a relatively large number of observations and variables, this area of social science is replete with applications for a variety of machine learning approaches. The present analysis was undertaken in the spirit of popular data journalism with the aim of obtaining a clearer picture of a political issue of longstanding public concern, namely United States federal campaign finance, through the lens of conventional statistical methodology complemented by the use of several supervised machine learning algorithms. 

There is a widely held opinion among the American electorate that our federal elections are ‘sold to the highest bidder’ via exorbitant individual and corporate campaign contributions, and that our representatives in the legislative and executive branches may thus be regarded as ‘bought and paid for’ by these powerful entities. Among other advantages, it is clear that outsized campaign donations facilitate campaign outreach on a scale which is usually inaccessible to candidates who lack wealthy backers, which may be reasonably supposed to skew election outcomes in favor of those candidates with the most generous donors. However, it is conceivable that the many disparate non-financial (often non-quantifiable) factors which might determine whether or not a candidate wins or loses, e.g., candidate incumbency or personal charisma, exert a greater influence individually or in concert than campaign funding alone. Moreover, it stands to reason that greater campaign contributions will tend be invested in candidates who are, for one reason or another, perceived by potential donors as likely to win (re)election by virtue of such potentially confounding factors.

In an attempt to clarify these issues, an analysis was undertaken of the 2016 House of Representatives election cycle using campaign finance and electoral outcome data obtained from the Federal Election Commission. Following extensive processing of the raw data, several conventional statistical methods were employed to visually and quantitatively elucidate key relationships among the variables of interest (namely incumbency, total received campaign funds, and electoral outcome in the form of vote share and binary win/loss). Finally, following additional preprocessing, a handful of popular machine learning models were tuned and trained on the data to assess how predictive were the two chosen features. Armed with a more robust dataset consisting of similar data from prior election cycles, these parametric statistical methods and machine learning algorithms could be deployed to obtain greater insight into the extent to which our representatives are effectively elected by (and therefore accountable to) their donors as opposed to their constituents.

### Materials and Methods

Histograms, barplots, stripplots, boxplots, swarmplots, correlational analyses, group comparison tests, confidence intervals, one-way ANCOVA, contingency tables, and tests of independence were used to visualize and quantify the interrelationships among the three variables studied. To supplement these more conventional statistical analyses, six of the <span style="font-family:Courier">sklearn</span> Python package's machine learning algorithms were deployed, namely <span style="font-family:Courier">LogisticRegression</span>, <span style="font-family:Courier">KNeighborsClassifier</span>, <span style="font-family:Courier">SVC</span>, <span style="font-family:Courier">DecisionTreeClassifier</span>, and a triple-layer perceptron, to determine how readily one might predict election outcomes using each feature alone or combination. All models were tuned and cross-validated using sklearn's <span style="font-family:Courier">GridSearchCV</span>. 

Given the relatively small dataset and few features used in this project, it seemed clear a priori that any variation in learning algorithm performance was likely to be well within the noise, as was borne out by the analysis; however, the model comparisons were retained in the hope that this project might be scaled considerably in the near future with a greatly augmented dataset consisting of many additional election cycles.

Python libraries utilized in this project included NumPy, pandas, SciPy, Matplotlib, Seaborn, statsmodels, Pingouin, and scikit-learn. All code was typed and executed within the included Jupyter Notebook.

### Summary of Preliminary Results

Elementary statistical analyses of this limited datasetlargely bear out the foregoing hypotheses. In particular, total campaign contributions correlate strongly with incumbency and vote share, and appear to be determinative of electoral viability in that no candidate receiving less than a quarter million dollars won their respective race, i.e., those candidates receiving little or no financial support may as well be non-contenders. Perhaps surprisingly, however, a covariate-adjusted logistic regression model revealed a strong correlation between total received campaign contributions and electoral victory even after controlling for incumbency, indicating that incumbency alone does not suffice to confound the hypothesis that campaign contributions substantially influence election results. Finally, the various machine learning models trained on these data achieved high accuracy, precision, recall, and F1 scores, with k-Nearest Neighbor and a Multilayer Perceptron displaying both the best performance metrics and Logistic Regression and Decision Tree Classifier producing the most promising decision boundaries among the tested models, suggesting their implementation in future applications to larger datasets of the same kind.