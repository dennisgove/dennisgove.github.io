---
layout: post
title:  "Solr Streaming Expressions"
categories: solr streaming expressions
---
Streaming Expressions were _technically_ added to Solr in v5.2 with [SOLR-7377][SOLR-7377] but in reality weren't all that useful until the release of v6.0 when a whole host of functionality was added. A full listing of the functionality available at the time of writing can be found in the official [Apache Solr Reference Guide][ref-guide].

The definition found on the guide describes Streaming Expressions as providing

> a simple yet powerful stream processing language for SolrCloud. They are a suite of functions that can be combined to perform many different parallel computing tasks.

Alright. So there you go.

I like to think about them like this. Solr Streams are a pipeline of tasks performed on sets of tuples. Streaming Expressions describe those pipelines. 

Streams are started with what's called a _Source Stream_ which sources data from from _Datastore_. From there the pipeline can be built upon using _Stream Decorators_, which are used to modify tuples as they pass through the pipeline.

The following examples make use of this legend.

![Legend](/images/solr-streaming-expressions/legend.png)

And now the examples,

![Owner's Pets and their ages](/images/solr-streaming-expressions/exampleA.gif){:class="img-responsive"}


[ref-guide]:  https://cwiki.apache.org/confluence/display/solr/Streaming+Expressions
[SOLR-7377]:  https://issues.apache.org/jira/browse/SOLR-7377

<!-- You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: http://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
 -->
