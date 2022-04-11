---
layout: post
title:  "Entropy-based Detection Method against DoS/DDoS attacks in an SDN-IoT environment"
date:   2022-01-10 14:19:31 +0900
categories: projects
---
<p style="color:gray;">
[<a target="_blank" href="/files/SDN_based_Detection_Method_against_DoS_DDoS_attacks_in_an_IoT_environment_Abdul_Adhim.pdf" title="" style="color:gray;">PAPER</a>]
[<a target="_blank" href="/files/SDN-based Detection Method against DoS.pdf" title="" style="color:gray;">SLIDES</a>]
</p>

### TL;DR

This project studies the approach of detecting [DoS/DDoS](https://en.wikipedia.org/wiki/Denial-of-service_attack) attacks using an entroy-based detection method. Experiments were conducted in an SDN environment, virtually using [Mininet](http://mininet.org/). Below is a snipet of the work. Please read the full paper <a target="_blank" href="/files/SDN_based_Detection_Method_against_DoS_DDoS_attacks_in_an_IoT_environment_Abdul_Adhim.pdf" title="">here</a>.

#### Keywords
IoT, SDN (Software-Defined Network), DoS, DDoS, Entropy-based detection

### Goals

The key contributions in this paper are listed in the following:


* A real-time approach to detect DoS/DDoS attacks by calculating the entropy of the network traffic in the SDN architecture. A practical way to use entropy-based detection with the consideration of fast-response while the network traffic is being loaded. 

* The calculation of entropy is done with the help of sFlow-RT. (sFlow Monitoring Technology). Number of packets being analyzed do not effect the computational power of the main controller of SDN.

### Key technology/points

<ins>SDN [(Software-Defined Network)](https://opennetworking.org/sdn-definition/)</ins>

A network architecture that is realized by virtualizing its components. SDN is structured in a way that its network is centralized, and can be centrally controlled with software applications.

<ins>Entropy-based detection</ins>

In information theory, entropy can be used to measure the uncertainty of information. In the context of detecting a heavy incoming traffic, entropy would measure the randomness in the incoming packets in the network. This calculation can be done with Shannon entropy. Shannon entropy can be defined as : 

<!-- H = - \sum_{i=1}^{n} p_i \log _{2} p_i -->

<img src="https://latex.codecogs.com/svg.latex?\Large&space;H = - \sum_{i=1}^{n} p_i \log _{2} p_i" title="\Large H = - \sum_{i=1}^{n} p_i \log _{2} p_i" />


Where there is an information source, `n` is the independent symbols, `p_i` is the probability of each `n`, and `H` would be entropy value.

During a DoS/DDoS attack, the changes in network traffic distribution fluctuates drastically. When this happens, the entropy calculation could measure that and trigger alert about the state of the traffic.

To judge whether the calculated entropy is anomalous or not, it is necessary to set a 'threshold'. If the calculate entropy drops below the threshold, then the traffic can be considered as an attack.

<ins>Threshold Setting Method</ins>

The threshold setting method used here is derived from [7]. This mitigation method was chosen because of its adaptive threshold algorithm. Where the threshold of the detection is updated according to the state of the traffic. It is suitable for detecting small and stealthy attack.

The flow of the threshold setting method can be summarized as below:

<img src="/images/sdn/flowc4.png" title="" />


Where `H` is the current entropy value, `µ` and `σ` are the mean and standard deviation of flow count during a particular time interval , `D` is the difference between the mean value µ and the entropy, and `β` the threshold multiplication factor.


### Experimental Scenarios

<ins>DoS Scenario</ins>

To test the detection in a DoS scenario, a network like in figure below was set up. The red node (h1) represents the attacker and the green node (h4) represents the target. The bandwitdh of each connection is set to be 1Mbits/sec. So any flow that goes beyond 1Mbits/sec would make the connected device inaccessible. The traffic is being monitored from the Control Plane. The attacking machines are sending packets as fast as possible to the target machine until it goes beyond the
bandwidth.

<img src="/images/sdn/sdnDos.png" title="" width="55%"/>

<ins>DDoS Scenario</ins>

In the DDoS scenario, the network architecture that was set up is similar to the one in DoS scenario. Instead this time 9 hosts and 4 switches were used connected in a tree topology. Multiple attacking hosts (h1-h4) are set to attack a single target (h9). The attacking 5 machines are also sending packets as fast as possible to the target machine.

<img src="/images/sdn/sdnDDos.png" title="" width="75%"/>

### Experimental Method

<ins>Method flowchart</ins>

<img src="/images/sdn/flowc5.png" title=""/>


### Result (Detection Speed)

<ins>DoS Scenario</ins>

<img src="/images/sdn/dosG1.png" title="" width="60%"/>
<img src="/images/sdn/dosG22.png" title="" width="60%"/>

<img src="/images/sdn/dos-h1-h42.png" title="" width="60%"/>

<ins>DDoS Scenario</ins>

<img src="/images/sdn/ddosG1.png" title="" width="60%"/>
<img src="/images/sdn/ddosG2.png" title="" width="60%"/>

<img src="/images/sdn/ddos-sflow22.png" title="" width="60%"/>


<!-- You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

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
{% endhighlight %} -->
