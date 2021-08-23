# Caching

#### By  [Shubham Borke](https://github.com/shubhamborke7778)

#### Aug 9, 2021
<HR>


### Introduction
<hr>

The cache is a process that copies data in a temporary system location and can be applied to load a website or system faster. It ensures that websites or systems do not need to download data regularly. The process saves temporary data from software, servers, websites, etc.

Web caching is also known as the strategy of improving performance for web-based systems. The web caching mechanism is implemented in three ways: client level, proxy level, and original server level. The cache is the core of web cashing, which takes places cache mechanisms, storing strategies, cache replacement, etc. 


Cache storing mechanisms have limited space to use for the cache storing process. Here an intelligence mechanism takes place to manage web content efficiently. What web-cache should store and what web-object should be replaced to make the best use of available cache space, help to improve the performance of the system.

Nowadays, the cache concept is modified and simple enough. Without storing additional data separately, systems save a copy of the page in a browser. In this way, web pages can be read faster.





### Web Cache
<hr>

Web-cache is one of the most successful solutions for improving the performance of web-based systems. In the concept of caching, the repeated objects are kept in a position closer to the client machine or proxy servers. Those, web caching reduces extra timeout taken from websites.

There are three types of fundamentals in web-caching to store the cache.
1. Browser cache
2. Proxy server cache
3. Original server cache

#### 1. Browser Cache

The browser cache is located near the client system. The client can observe it in internet browsers. The cache is useful when the client revisits the page. To store cache for each page is separated with a key of that page key name.

#### 2. Proxy Server Cache

Proxy server cache is found in proxy servers where clients accessing data from. It helps to serve data faster from the web and client also. When the rapid request arrives at the proxy server will check further for the cache. If a cache key is found, then similar contents will served to the client or similar checks for the web to receive it.

#### 3. Original Server Cache


Original server cache is saved on server-site to reduce redundancy of repeat requests from proxy servers. Server load will be reduced if cache stored exists in server-site.

>Generally, scaling and processing issues happen with Browser cache, Proxy server cache, and original server cache departments.

### Algoritham
<hr>

Cache has an algorithm to store our store out. As the cache has a limited size to store. If cache memory is full of storing objects, there will be an amount of data loss happen if there is no space reserved for the cache. Hence the cache algorithm takes place. The cache should evict the data to allow space for the new object.

In the industry, there are a lot of algorithms for storing cache. The most commonly used algorithm is Least-Recently-Used (LRL). It removes least used objects until require space for writing cache data. The least-recently-used method is easy to implement and simpler accessible for uniform-size objects or data. Hence the cache is populated with a small object's size for availability to store the extra amount of data.

When cache space is occupied and removed the least frequent data storing a new object, the algorithm is used here as a formula describe down.

![Formula for cache calculation](Capture.png)

### Scaling
<hr>

Scaling problems generally occur in databases. When servers request lots of requests in a second, then the system freezes. For processing and smoothing requests from clients or servers, systems need to resolve processing techniques.

If the server is loaded with dozens of requests pending then the server's processing time will convert to waiting time. Hence the client can face issues with a timeout from the server.

Scaling and Processing issues usually occur when load happens on the server. Scaling is related to keys per request and processing is related to the processing time of that process.

### Limitations 

* Repeated requests from the client and server will affect the database and trouble storing data. There will be some memory issues for storing keys to cache or cache data.

* Sometimes there are existing keys located with different cache data. To realize which data to take and which to drop matters. Hence some techniques are used to store cache data. Explains inside solutions.

* Generally, processing of the request is caused by reaching out to the network, no proper network, etc. Hence Bloom-filter, Lock-mechanism used here to resolve runtime problems.

### Solutions
<hr>

* When there is no key to store empty data to write data in the cache, all requests hit the database. With the slight modification of code, it is possible to create keys for requests. Often requests results returned null.

* Another solution with the "Bloom filter" is possible. Which creates barriers before the cache to store all keys exists in the current database. If the request key is not present, then it will avoid checking cache data and return null directly. If a key is present in the database, the matched key will go through the database. 

* We can use a lock mechanism for the cache. When the first request is initiated, the data in the cache will be locked. At this time other queries will not be able to access data until a request is complete. After locking release, the waiting queries will be directly retrieved data from the cache. 

* To avoid scaling issues from the original server to the proxy server, the recently reserved request should be stored in cache and a copy of the process also should be kept by the original server. The same thing happens with a proxy server to a client-server. Hence, the original server and proxy server can check for the existing key. If exist, will redirect that data. else, create a copy of process data.

### Resources
<hr>

* [Introduction of caching](https://en.wikipedia.org/wiki/Cache_(computing)) 

* [What is chaching](https://www.fortinet.com/resources/cyberglossary/what-is-caching)

* [Improvement in internet performance](https://www.3pillarglobal.com/insights/blog-posts/how-web-caching-improves-internet-performance/)

* [Problems and solution on caching](https://medium.com/@mena.meseha/3-major-problems-and-solutions-in-the-cache-world-155ecae41d4f)

* [Algoritham study](https://www.researchgate.net/publication/265986051_A_Survey_of_Web_Caching_and_Prefetching_A_Survey_of_Web_Caching_and_Prefetching)