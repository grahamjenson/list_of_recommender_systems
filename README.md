# List of Recommender Systems

Recommender systems (or recommendation engines) are useful and interesting pieces of software. I wanted to compare recommender systems to each other but could not find a decent list, so here is the one I created. Please help me keep this post up-to-date by submitting corrections and additions via pull-request, or tweet me [@grahamjenson](https://twitter.com/grahamjenson).

## Software as a Service Recommender Systems

SaaS Recommender systems have many challenges to their development including having to handle multi-tenancy, store and process a massive amount of data and other softer concerns like keeping a clients sensitive data safe on remote servers.

The benefits to using a SaaS recommender system is that you can pay for value with a low overhead rather than having a large upfront investment, they generally have a clear integration path for you to use, and they provide continual development and improvement while you use it.

The SaaS recommender systems are:

1. [Rcmmndr](http://www.rcmmndr.com/) which is a [Heroku add-on](https://devcenter.heroku.com/articles/rcmmndr). It is based on **Hadoop** but seems to be based *abandoned*
2. [Mortar Recommendation Engine](https://www.mortardata.com/recommendation-engine) is a kind of do-it-yourself recommender system, where by using their PaaS [Mortar](https://www.mortardata.com) and MongoDB there are instructions to create a recommender system.
3. [Peerius](http://www.peerius.com/) closed, product and e-commerce focused for live and email recommendations. Active and seems very interesting, although little information about the actual product and how it works is available.
4. [Strands](http://recommender.strands.com/) is a closed, product and e-commerce focused system. I think it works by including tracking scripts (a la Google Analytics) on the website, and recommendations widgets. What I really like about Strands is their publishing of case-studies e.g. [Wireless Emporium](http://retail.strands.com/customers/wireless-emporium-case-study/) and white papers like [The Big promise of recommender systems](http://www.aaai.org/ojs/index.php/aimagazine/article/viewFile/2360/2232). Although these do not discuss the exact solutions provided, they give a good overview of their vision and goals of providing recommendations.
5. [SLI Systems Recommender](http://www.sli-systems.com/) A closed recommender system focused on e-commerce, search and mobile.
6. [Google Cloud Prediction API](https://cloud.google.com/prediction/docs) Googles offering of cloud computed prediction API
7. [Using Hadoop on Google Cloud](http://googlecloudplatform.blogspot.co.nz/2014/01/performance-advantages-of-the-new-google-cloud-storage-connector-for-hadoop.html) an example use of Google cloud with benchmarks from recommender system.
8. [ParallelDots](http://www.paralleldots.com/) tool to relate published content
9. [Amazon Machine Learning](http://aws.amazon.com/machine-learning/) machine learning platform to model data and create predictions
10. [Azure ML](http://azure.microsoft.com/en-us/services/machine-learning/) machine learning platform to model data and create predictions
11. [Gravity R&D](http://www.gravityrd.com/) is a company built by some of the winners from the 2009 Netflix prize. They offer a solution that provides targeted, customized recommendations to users of websites. They have some pretty big clients including [DailyMotion](http://www.gravityrd.com/projects#block-views-block-key-partners-key-partners) and a [technology page](http://www.gravityrd.com/technology) which describes their architecture, algorithms, and a list of publications. (suggested by [Marton Vetes](https://www.linkedin.com/in/martonvertes))
12. [GraphFlow](http://graphflow.com/) provides is a user event analytics and recommendations API, with [integration](http://docs.woothemes.com/document/woocommerce-graphflow/) into the [WooCommerce WordPress store](http://www.woothemes.com/woocommerce/) plugin.
13. [Dressipi Style Advisor](http://partners.dressipi.com/style-adviser.html) is a clothing specific recommendations service. It incorporates both expert domain knowledge and machine learning to find outfits for occasions or moods.
14. [Sajari](https://www.sajari.com/recommend) is a search, recommendation and matching (e.g. dating website) service. On their site, they also have aggregated a bunch of useful [data-sets](https://www.sajari.com/public-data).
15. [IBM Watson](http://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/) is available through Watson Developer Cloud, which provides REST APIs ([Watson APIs on Bluemix](http://www.ibm.com/cloud-computing/bluemix/watson/)) and SDKs that use cognitive computing to solve complex problems.

## Open Source Recommender Systems

Most of the non-SaaS recommender systems that are open-source. This may have been because recommender systems are more tailored to clients so not easily made into a product.

The open-source recommender systems are:

1. [PredictionIO](http://prediction.io/) is built on technologies [Apache Spark](https://spark.apache.org/), [Apache HBase](http://hbase.apache.org/) and [Spray](http://spray.io/). It is a machine learning server that can be used to create a recommender system. The source can be located on [github](https://github.com/PredictionIO/PredictionIO) and it looks very active.
2. [Racoon Recommendation Engine](https://www.npmjs.org/package/raccoon) is an open source Node.js based collaborative filter that uses Redis as a store. It is effectively abandoned.
3. [HapiGER](http://www.hapiger.com/) is an open source Node.js collaborative filtering engine, which can use in-memory, [PostgreSQL](http://www.postgresql.org/) or [rethinkdb](http://rethinkdb.com/). Reasonably active development (when I have time :)
4. [EasyRec](http://easyrec.org/) Java and Rest based recommendations. Abandoned
5. [Mahout](http://mahout.apache.org/) Hadoop/linear algebra based data mining
6. [Seldon](http://www.seldon.io) is a Java based prediction engine built on technologies like [Apache Spark](https://spark.apache.org/). It provides a demo movie recommendations application [here](http://www.seldon.io/movie-demo/).
7. [LensKit](http://lenskit.org/) is a Java based research recommender system designed for small-to-medium scale.
8. [Oryx](https://github.com/cloudera/oryx) [v2](https://github.com/OryxProject/oryx) a large scale architecture for machine learning and prediction (suggested by [Lorand](https://disqus.com/by/disqus_V9tbLHpUxp/))
9. [RecDB](http://www-users.cs.umn.edu/~sarwat/RecDB/) is a PostgreSQL extension to add recommendation algorithms like collaborative filtering directly into the database.
10. [Crab](http://muricoca.github.io/crab/) a python recommender based on the popular packages NumPy, SciPy, matplotlib. The main repository seems to be *abandoned*.
11. [predictor](https://github.com/Pathgather/predictor)is a ruby recommender gem. This uses Jaccard or Sorenson-Dice coefficient to priovide both item centric e.g. "Users that read this book also read ..." and user centric e.g. "You read these 10 books, so you might also like to read ..." recommendations. Looks a bit neglected.

## Non-SaaS Product Recommender Systems

Not very many Non-SaaS Non-OpenSource recommender systems seem to exist. Below is a list:

1. [Dato](http://dato.com/) is a company that provides a python package and servers for business machine learning including many predictive algorithms for recommendations. They also integrate with [Apache Spark](http://blog.dato.com/using-apache-spark-with-graphlab-create) and have great blog posts like **[Why is building custom recommender systems hard? Does it have to be?](http://blog.dato.com/why-is-building-custom-recommender-systems-hard-does-it-have-to-be)**. Their customers include Pandora and StumbleUpon, must be a good product.

## Academic Recommender Systems

Recommender systems are a very active area of research in academia, though few of the generated systems make it out of the lab. Here are a few I have found that did:

1. [Duine Framework](http://sourceforge.net/projects/duine/) a Java based recommendation system that has been abandoned
2. [MyMediaLite](https://github.com/zenogantner/MyMediaLite) C# based in-memory recommender system that has been abandoned
3. **Bonus:** [List of Recommender System Dissertations](http://www.recsyswiki.com/wiki/List_of_recommender_system_dissertations), a useful list to keep up with the current state of recommendations systems in academia
4. [LibRec](http://www.librec.net/) A Java based Recommendations engine with loads of implemented algorithms (suggested by [Saúl Vargas](http://www.dcs.gla.ac.uk/~saul/))
5. [RankSys](http://ir-uam.github.io/RankSys/) Java Recommendation system for novelty and diversity created by [Saúl Vargas](http://www.dcs.gla.ac.uk/~saul/))

## Benchmarking Recommender Systems

It is very difficult to benchmark recommender systems, not only because getting good datasets is hard, but different methods and algorithms have different advantages and disadvantages that are difficult to expose.

Here is a list of some benchmarking tools:

1. [TagRec](https://github.com/learning-layers/TagRec) Tag Recommender Benchmarking Framework
2. [RiVaL](http://rival.recommenders.net/) an open source toolkit for recommender system evaluation. Some results are posted [here](http://alans.se/blog/2014/rival/).
3. [Idomaar](http://rf.crowdrec.eu/) is a reference framework for recommender algorithm testing. It is developed in the framework of the [CrowdRec](http://crowdrec.eu) project.

## Media Recommendation Applications

In addition to generic recommender systems, I decided to add a list of applications where recommendations are a core offering, specifically in the domain of media recommendations:

1. [Yeah, Nah](http://yeahnah.maori.geek.nz/) Movie recommendations site based on [GER](https://github.com/grahamjenson/ger) *[source](https://github.com/grahamjenson/yeahnah)*
1. [Jinni](http://www.jinni.com/) Movie recommendations site
1. [Gyde](http://gyde.tv/) Streaming media recommendations
1. [TasteKid](http://www.tastekid.com/) movies, books, music recommendations. *sent to me by [thelinuxlich](https://github.com/thelinuxlich)*
1. [Gnoosic](http://www.gnoosic.com/) music based on bands. *sent to me by [thelinuxlich](https://github.com/thelinuxlich)*
1. [Pandora](http://www.pandora.com/) music recommendations based on likes and dislikes or songs


## Books

1. [Practical Recommender Systems](https://manning.com/books/practical-recommender-systems-cx) by Kim Falk (Manning Publications). [Chapter 1](https://manning.com/books/practical-recommender-systems-cx#downloads)
