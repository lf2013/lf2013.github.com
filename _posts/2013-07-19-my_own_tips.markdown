---
layout: post
title: "My Little Tips"
date: 2013-07-19 16:09
comments: true
categories: [Note]
---
###1.How to copy between two terminals using vim?
1.open file a
2.copy the items (using yy)
3.close file a (Main point)
4.open file b
5.paste the items
6.save and exist file b

###2.How to open a url in python 
{% highlight python %}
url = urllib2.quote(url.encode("utf8"))
{% endhighlight %}
###3.How to load json in python 
{% highlight python %}
f = urllib2.urlopen(url)
ff = f.read()
jdata = simplejson.loads(ff)
{% endhighlight %}
Or
{% highlight python %}
f = urllib2.urlopen(url)
jdata = simplejson.load(f)
{% endhighlight %}
###4.How to reverse a Hash table in ruby
1.convert the Hash to an Array
2.reverse the Array 
3.convert the Array to a Hash 
{% highlight ruby %}
reversed_h = Hash[h.to_a.reverse]
{% endhighlight %}
###5.How to view the System version
{% highlight sh %}
cat /etc/issue
{% endhighlight %}
###6.How to unzip xx.tar.bz2 file
{% highlight sh %}
unzip xx.tar.bz2
bzip2 -d xx.tar.bz2 ===> xx.tar
tar -xvf  xx.tar ===> xx
{% endhighlight %}
