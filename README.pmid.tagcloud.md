## Quick wordclouds from PubMed abstracts - using PMID lists in R

<span style="color:#18334e">
Wordclouds are one of the most visually straightforward, compelling ways of displaying text info in a graph.

Of course, we have a lot of web [pages](http://www.techlearning.com/default.aspx?tabid=100&entryid=364) (and even [apps](https://ictevangelist.com/top-six-apps-for-creating-word-clouds/)) that, given an input text, will plot you some nice tagclouds. However, when you need reproducible results, or getting done complex tasks -like combined wordclouds from several files-, a programming environment may be the best option.

In R, there are (as always), several alternatives to get this done, such as [tagcloud](https://logfc.wordpress.com/2014/11/05/tagcloud-creating-tag-word-clouds/) and [wordcloud](https://cran.r-project.org/web/packages/wordcloud/wordcloud.pdf).

For this script I used the following packages:

- `RCurl` to retrieve a PMID list, stored in this GitHub account as a **.csv** file.
- `RefManageR` and `plyr` to retrieve and arrange PM records. To fetch the info from the inets, we'll be using the [PubMed API](https://www.ncbi.nlm.nih.gov/home/develop/api.shtml) (free version, with some limitations). 
- Finally, `tm`, `SnowballC` to prepare the data and `wordcloud` to plot the wordcloud. This part of the script is based on this from [Georeferenced](https://georeferenced.wordpress.com/2013/01/15/rwordcloud/).

One of the advantages of using RefManageR is that you can easily change the field which you are importing from, and it usually works flawlessly with the PubMed API.

My biggest problem sources when running this script: download caps, busy hours, and firewalls!.

At the beginning of the gist, there is also a handy function that automagically downloads all needed packages for you.

To source the script, simply type in the R console:

This script creates two directories in your working directory: 'corpus1' for the abstracts file, and 'wordcloud' to store the plot.

<pre><code>
library(devtools)
source_url("https://github.com/aurora-mareviv/idis-devel/blob/master/pmid.tagcloud.R")
</code></pre>

</span>
