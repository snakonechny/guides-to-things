# Data Science Resources and Guides - reworked (2021)

_This is my stock answer to "I'd like to do data science. Where do I start?" My answer here is biased, broad, and probably boring, but it should be enough to get one going in the right direction._

To me, doing data science means a few different things. For starters, it means being able to _write programs_ that manipulate data; "manipulating" in this case translates into _moving data_ from point A to point B, from one state/format to another, via _data store_ X to _database_ Y. It also means interpreting these data through _visuals and summaries_. Finally, it will likely involve some form of _statistical modeling_ (fitting a math function that explains your current dataset and using it to project over some previously unseen data). I will follow these tasks points as my guides in this writeup.

For everything that follows, a "*" means I read/attempted to finish/finished that particular resource and can recommend it first hand. "**" means I really liked it.

## Writing programs

This is a prerequisite. I don't think one can do data science without knowing how to code. I don't think one needs to have formal computer science training to start, though that would definitely help. I do think a novice programmer can start fiddling with just about any tool here, but they should be prepared for frustration and learning pains.

In this domain, there are two dominant programming languages, [R](https://www.r-project.org/about.html) and [Python](https://www.python.org/). There are a few second-string options: [Julia](https://julialang.org/), [Matlab](https://www.mathworks.com/products/matlab.html), etc. I will stick to the dominant ones here.

_How to learn this?_

Online classes: On Udemy, [Tim Buchalka's Python Masterclass](https://www.udemy.com/course/python-the-complete-python-developer-course/)**, [Jose Portilla's Python Bookcamp](https://www.udemy.com/course/complete-python-bootcamp/)**, [Kiril Eremenko's R A through Z](https://www.udemy.com/course/machinelearning/)

Online classes: Other learning providers, [Udacity's Programming for Data Science with R](https://www.udacity.com/course/programming-for-data-science-nanodegree-with-R--nd118), [edX's Intro to Python](https://www.edx.org/course/introduction-to-python-for-data-science-2)

Intro Books: [Python the Hard Way](https://www.amazon.com/Learn-Python-Hard-Way-Introduction/dp/0134692888/)**, [Learning Python](https://www.amazon.com/Learning-Python-5th-Mark-Lutz/dp/1449355730/), [The Book of R](https://www.amazon.com/Book-First-Course-Programming-Statistics/dp/1593276516/), [R for Data Science](https://www.amazon.com/Data-Science-Transform-Visualize-Model/dp/1491910399/)

Advanced Books: [Python Cookbook](https://www.amazon.com/Python-Cookbook-Third-David-Beazley/dp/1449340377/), [Advanced R](https://www.amazon.com/gp/product/0815384572/)**

If you've never taken a formal computer science class, you need to read these: [The Self-Taught Programmer](https://www.amazon.com/Self-Taught-Programmer-Definitive-Programming-Professionally/dp/0999685902/), [Computer Science Distilled](https://www.amazon.com/Computer-Science-Distilled-Computational-Problems/dp/0997316020/)**, [Grokking Algorithms](https://www.amazon.com/Grokking-Algorithms-illustrated-programmers-curious/dp/1617292230/)** and watch this [Missing CS Semester](https://www.youtube.com/c/MissingSemester)

If you've never taken a formal computer science class and have a lot of time on your hands, you must watch [these](https://www.youtube.com/c/cs50)

When you're bored and ready to give up on this shit: [Cesar Hidalgo's TED talk](https://www.youtube.com/watch?v=CyGWML6cI_k), [Dylan Beattle's coolness](https://www.youtube.com/watch?v=gdSlcxxYAA8)

_How to not learn this?_

An expensive bootcamp (I have strong opinions about those - come talk to me if you'd like); a rando on YouTube promising an all-inclusive tutorial.

## Data inputting, wrangling, and outputting (read, clean, write, or 90% of what I do)

Very broadly speaking, data come in two different flavors - structured and unstructured. Structured = predictable, consistent, reproducible format. Unstructured = a sheet of scanned A4 page, an audio file, a digital image.

Across these two flavors, data may come from a web page, a digital document (Excel doc), a machine-friendly file format (think .csv), or a database. Yes yes, I know there's more, but I think these are the most common sources.

_To interact with web pages:_

In Python - `requests` [library](https://realpython.com/python-requests/), `urllib3` [library](https://docs.python.org/3/library/urllib.html), `aiohttp` [library](https://docs.aiohttp.org/en/v3.0.1/)

In R - `request` [library](https://www.rdocumentation.org/packages/request/versions/0.1.0)

_To interact with digital documents:_

(This is difficult as there are so many different types of digital docs. I'll stick, again, to the most common ones)

In Python, _tabular data_ - `pandas` [library](https://pandas.pydata.org/pandas-docs/stable/), `dask` [library](https://dask.org/)

In R, _tabular data_ - `dplyr` [library](https://dplyr.tidyverse.org/), `data.table` [library](https://cran.r-project.org/web/packages/data.table/vignettes/datatable-intro.html)

In Python/R, _other files on disk_ - it's complicated, but look at [`Tika`](https://tika.apache.org/)

## Databases

There are books written on this, and I'd recommend the following:

* for general overview of what's out there, [Seven Databases in Seven Weeks](https://www.amazon.com/Seven-Databases-Weeks-Modern-Movement/dp/1680502530/)**, [Designing Data-Intensive Applications](https://www.amazon.com/Designing-Data-Intensive-Applications-Reliable-Maintainable/dp/1449373321/)**
* SQL, [Jose Protilla's Complete SQL Bootcamp](https://www.udemy.com/course/the-complete-sql-bootcamp/)*
* MongoDB, [Max's Complete MongoDB Guide](https://www.udemy.com/course/mongodb-the-complete-developers-guide/)*
* Graph databases, [Graph Fundamentals with Neo4j and Cypher](https://www.udemy.com/course/neo4j-foundations/)
* Hipster stuff, [Complete Guide to Elasticsearch](https://www.udemy.com/course/elasticsearch-complete-guide/)**

## Data visualization

Another massive topic; this is the sexy stuff everyone wants to do but few do well.

_Before learning how to draw a line graph in R:_

* read [Tufte's Visual Display of Quantitative Information](https://www.amazon.com/Visual-Display-Quantitative-Information/dp/0961392142/)**and [Beautiful Evidence](https://www.amazon.com/Beautiful-Evidence-Edward-R-Tufte/dp/0961392177/2)**. These are just fantastic books
* read [Fundamentals of Data Visualization](https://www.amazon.com/Fundamentals-Data-Visualization-Informative-Compelling/dp/1492031089/)*
* scroll through this [website](https://bost.ocks.org/mike/). Some fantastic examples of data visualizations

_Once you read Tufte:_

* I think data visualization tools are more mature in R than in Python, so start there
* [`ggplot`](https://ggplot2.tidyverse.org/index.html) is one of the best data science tools out there; it's beautifully documented and allows you to do just about anything as long as it's a line or a point
* [`shiny`](https://shiny.rstudio.com/) is what Tableau wants to be. Be better than Tableau and use Shiny

## AI/Machine learning/the sexy sexy stuff

Again, everyone wants to do this. Can a complete novice pick up a machine learning library and do some damage with it? Yes. Should they? I don't know. It's hard to do machine learning well, and it's even harder to find good guides/courses out there. Here's what I'd recommend:

* first class - [Machine Learning on Coursera](https://www.coursera.org/learn/machine-learning)
* then, [AI for Everyone on Coursera](https://www.coursera.org/learn/ai-for-everyone)
* then, [Machine Learning A-Z with Kiril Eremenko](https://www.udemy.com/course/machinelearning/)
* eventually maybe, [Neural Networks and Deep Learning](https://www.coursera.org/learn/neural-networks-deep-learning)

If you want more math, [anything by this guy](https://www.udemy.com/user/lazy-programmer/)

If you want something that just works, take a look at [spaCy](https://spacy.io/). This is what a good transfer learning library should look like.

Separate from this Coursera/Udemy family of courses, [Jeremy Howard](https://www.fast.ai/about/) has been working on series of data science curricula. These are completely free and _very_, _very high quality_. The downside is that they use his own proprietary machine learning library called _fastai_. Still, if you're starting from clean slate, I'd actually consider passively watching [this class](https://course.fast.ai/).

Separate separate from the above, there is a paid platform called [AlgoExpert](https://www.algoexpert.io/). For $150, you can get three things: (1) high quality, detailed overviews of common machine learning algorithms, (2) expert advice on real world applications, and (3) test and interview practice. I think it's well worth it.**

Books:

* [One Hundred Page Machine Learning Book](https://www.amazon.com/Hundred-Page-Machine-Learning-Book/dp/199957950X/)**
* [Hands-On Machine Learning](https://www.amazon.com/Hands-Machine-Learning-Scikit-Learn-TensorFlow/dp/1492032646/)**
* [Machine Learning with R](https://www.amazon.com/Machine-Learning-techniques-predictive-modeling/dp/1788295862/)

## In general

This stuff is hard, everyone wants to do it, but no one really knows how to. To find out if this is for you, try the cheapest path forward (Udemy courses, a free Coursera class, etc.) Do not start with a $10,000 bootcamp.

Find a dataset that seems interesting. [This](https://www.transtats.bts.gov/DL_SelectFields.asp?Table_ID=236) was my first dataset. Fiddle with it, break a few things, get frustrated, repeat. Have someone take a look at your code and give you feedback (I'm happy to do it).

Read as many [Medium](https://medium.com/) posts about machine learning, data science, data engineering, etc. as you can suffer through. I particularly recommend [this one](https://kozyrkov.medium.com/). Watch as much of this [channel](https://www.youtube.com/channel/UCtxCXg-UvSnTKPOzLH4wJaQ) as you can. Go to local meetups and socialize with other people interested in this stuff - that's the best way to learn.

Again, this stuff is hard to do. Frustration, anger, anxiety come included. Not knowing how to do something is my daily state of existence but it's also where I learn the most. Here is what works for me for mitigating said frustration/anger/anxiety:

* break down the larger problem into smallest possible pieces. For example, "analyzing massive dataset from some remote database" can be broken into "starting a notebook", "connecting to a database", "reading a tiny sample of the database", "reading a larger sample", etc.

* Google but don't start your queries with "How to ..."; instead, describe the problem you're facing - you'll likely get a tutorial back instead of a random angry Stackoverflow post that's lacking context and direction

* ask for help, though attempt to get to _some_ solution on your own; it may be incomplete and inefficient, but it's something you can iterate on

* do not do this for more than 1.5-2 hours in a single sitting
