---
layout: post
title:  "SDN-based Detection Method against DoS/DDoS attacks in an IoT environment"
date:   2022-01-10 14:19:31 +0900
categories: projects
---
<p style="color:gray;">
[<a target="_blank" href="/files/SDN_based_Detection_Method_against_DoS_DDoS_attacks_in_an_IoT_environment_Abdul_Adhim.pdf" title="" style="color:gray;">PAPER</a>]
[<a target="_blank" href="/files/SDN-based Detection Method against DoS.pdf" title="" style="color:gray;">SLIDES</a>]
</p>

### TL;DR

This project studies the approach of detecting [DoS/DDoS](https://en.wikipedia.org/wiki/Denial-of-service_attack) attacks using an entroy-based detection method. Experiments were conducted in an SDN environment, virtually using [Mininet](http://mininet.org/). Read the full paper <a target="_blank" href="/files/SDN_based_Detection_Method_against_DoS_DDoS_attacks_in_an_IoT_environment_Abdul_Adhim.pdf" title="">here</a>.

#### Keywords
IoT, SDN (Software Defined Network), DoS, DDoS, Entropy-based detection

### Goals

The key contributions in this paper are listed in the following:


* A real-time approach to detect DoS/DDoS attacks by calculating the entropy of the network traffic in the SDN architecture. A practical way to use entropy-based detection with the consideration of fast-response while the network traffic is being loaded. 

* The calculation of entropy is done with the help of sFlow-RT. (sFlow Monitoring Technology). Number of packets being analyzed do not effect the computational power of the main controller of SDN.

### Key technology/points

* SDN [(Software-Based Network)](https://opennetworking.org/sdn-definition/)
  * A network architecture that is realized by virtualizing its components. SDN is structured in a way that its network is centralized, and can be centrally controlled with software applications.
* Entropy-based detection

### Experimental Scenarios

### Result




You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.MARKUP`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. After that, include the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}
