# System Design 

![from The System Design Primer](https://i.imgur.com/i9kphdZ.png)

> Everything is a trade-off.

## Why？

> Learning how to design scalable systems will help you become a better engineer.

## What?

### Key words

- Load Balancing 
- Caching 
- Sharding or Data Partitioning 
- Indexes
- Proxies
- Queues
- Reducndancy and Replication
- SQL vs. NoSQL
- CAP Theorem
- Consistent Hashing 
- Long-Polling vs WebSockets vs Server-Sent Events

## How？

* Step 1: **Requirements clarifications**: Design questions are mostly open-ended, and they don’t have **ONE** correct answer, that’s why clarifying ambiguities early in the interview becomes critical.
	* Will users of our service be able to post tweets and follow other people?
	* Should we also design to create and display user’s timeline?

 
* Step 2: System **interface** **definition**: Define what **APIs** are expected from the system. This would not only establish the exact contract expected from the system but would also ensure if you haven’t gotten any requirements wrong.
* Step 3: Back-of-the-envelope **estimation**: It’s always a good idea to estimate the scale of the system you’re going to design. This would also help later when you’ll be focusing on **scaling**, **partitioning**, **load balancing** and **caching**
	* What scale is expected from the system (e.g., number of new tweets, number of tweet views, how many timeline generations per sec., etc.)?
 
* Step 4: **Defining data model**: Defining the data model early will clarify how data will flow among different components of the system. Later, it will guide towards data partitioning and management. Candidate should be able to identify various entities of the system, how they will interact with each other and different aspect of data management like storage, transportation, encryption, etc.
	* User: UserID, Name, Email, DoB, CreationData, LastLogin, etc.
	* Tweet: TweetID, Content, TweetLocation, NumberOfLikes, TimeStamp, etc.
	* Which database system should we use? Would NoSQL like Cassandra best fits our needs, or we should use MySQL-like solution. What kind of block storage should we use to store photos and videos?

* Step 5: **High-level design**: Draw a block diagram with 5-6 boxes representing core **components** of your system. You should identify enough components that are needed to solve the actual problem from end-to-end.
* Step 6: **Detailed design**: Dig deeper into 2-3 components; interviewers feedback should always guide you towards which parts of the system she wants you to explain further. You should be able to provide ***different approaches, their pros and cons***, and ***why would you choose one***? Remember there is no single answer, the only thing important is to consider tradeoffs between different options while keeping system constraints in mind.
	* Since we’ll be storing a huge amount of data, how should we partition our data to distribute it to multiple databases? Should we try to store all the data of a user on the same database? What issue can it cause?
 
* Step 7: Identifying and resolving **bottlenecks**: Try to discuss as many bottlenecks as possible and different approaches to mitigate them.
	* Is there any single point of failure in our system? What are we doing to mitigate it?
	* Do we’ve enough replicas of the data so that if we lose a few servers, we can still serve our users?

 
### Exmaple

- [Designing a URL Shortening service like TinyURL](https://www.educative.io/collection/page/5668639101419520/5649050225344512/5668600916475904)

### Story

- [为什么超音速电动飞机不太可能出现？](https://i.imgur.com/DtqQjQu.jpg) : 结合现实的分析，就是System Design。


## More 

* **入门**：[system-design-primer](https://github.com/donnemartin/system-design-primer)
* **面试**：[Grokking System Design](https://www.educative.io/collection/5668639101419520/5649050225344512): 相关课程及笔记
* 模拟：[Pramp](https://www.pramp.com/): 模拟面试
* 实战：[Designing Data-Intensive Applications](https://book.douban.com/subject/26197294/): 时间宽裕的话看，内容很详尽，理解会更深。