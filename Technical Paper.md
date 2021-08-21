# Caching

#### By  [Shubham Borke](https://github.com/shubhamborke7778)

#### Aug 9, 2021

## contents:

* Introduction
* Concept
* Problems
* Solution
* Resources

### Introduction
The cache is a process that copies data in a temporary system location and can be access to load a website or system faster. It ensures that websites or Systems do not need to download data every time. The process saves temporary data from Softwares, Servers, websites.

This data includes images, files, and scripts, Which automatically store on the device for the first time when the user opens an application or web page. This process helps users to load the system or website faster.


Generally, website owners want to pay for every visit of the user to the server. For every page to be download from servers, it will cost the website owner. If the cache data is collected by the system, Then no need to download additional data from a website everytime, so that the owner will save the amount of money. The users will encourage to revisit the website.


Nowadays, the cache concept is modified and simplest enough. Without storing additional data separately, systems save a copy of the page in a browser. In this way, web pages have read access faster.


### Concept

* The cache can save in two ways 
>
>1. Browser cache.
>2. Memory cache.

1. Memory caches store in a local computer on random access memory(RAM). The next time if similar result happens, resources pull data from RAM and helps things to load from RAM without loading all data.

2. The browser cache stores data in the browser, Which can access data to load the website with local computers RAM.

* The cache is saved with priorities like "Header" to sort the data and is easily accessible by memory to display without downloading additional data.

* Because of cache can not use a lot of memory to store files and low latency means to run application accessible faster.

### Problems

* If there is massive data to store in the cache memory then it causes the extra time to write data in RAM and lots of requests are in the queue.

* Code logic errors can affect writing cache data in memory and breaks in the formatting sequence of lines.

* Usually, We set a time limit for writing cache. After the expiration time database will delete the cache data and extends the performance time. It will cause the client to face user experience or system crashes.


### Solutions

* When there is no key to store empty data to write data in the cache, all requests hit the database. With the slight modification of code, it is possible to create keys for requests. Often requests results return null.

* Another solution with Bloomfilter is possible. Which creates barriers before the cache to store all keys exits in the current database. If the request key is not present then it will avoid chacking cache data and return null directly. If a key is present in the database, the matched key will go through the database. 

* We can use a lock mechanism for the cache. When the first request is initiated, the data in the cache will be locked. at this time other queries will not able to access data until a request to complete. After lock release, The waiting queries will be directly retrieved data from the cache.

### Resources

* [Introduction of caching](https://en.wikipedia.org/wiki/Cache_(computing)) 

* [What is chaching](https://www.fortinet.com/resources/cyberglossary/what-is-caching)

* [Improvement in internet performance](https://www.3pillarglobal.com/insights/blog-posts/how-web-caching-improves-internet-performance/)

* [Problems and solution on caching](https://medium.com/@mena.meseha/3-major-problems-and-solutions-in-the-cache-world-155ecae41d4f)