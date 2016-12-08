https://www.arangodb.com/why-arangodb/multi-model/
https://www.arangodb.com/performance/

# ArangoDB - a native multi-model database

ArangoDB is a native multi-model database. You can store your data as key/value pairs, graphs or documents and access all your data with one declarative query language. You can also combine the different models in one query. Due to it’s native multi-model approach you can build high-performance applications and scale horizontally with all three data models.

Many vendors call themselfs “multi-model” but there is an important difference between putting just e.g. a graph layer on top of your key/value or document store and ArangoDB’s native multi model approach. Find all the details to our approach and a brief list about the core advantages a native multi-model like ArangoDB provides for you.
## What is a native multi-model database?

A native multi-model database like ArangoDB uses the same core and the same query language for all data models. Thereby users are able to combine different models and their features in one query. ArangoDB doesn’t “switch” between the models behind the scenes and doesn’t shovel data from a to b all the time in order to execute queries. This leads to strong performance advantages compared to “layer-approaches” and ArangoDB’s suitability for high performance needs.
## How does ArangoDB provide its multi-model capabilities?

Key/Value
Every document consists of a unique key and contains values to certain attributes. If you store one value in a document then ArangoDB serves as a classic, highly scalable key/value store which you might need for e.g. temporarily storing products in a user shopping-cart of an ecommerce platform or sensoric data in IoT applications and so on.
Document
You can store as many attributes in a document as you like (default size of a document is 32MB, but configurable to your needs). ArangoDB has a wide feature-set for querying and working with documents like joins, secondary indexes or acid transactions. You can horizontally scale join usage to the technically possible.
Graph
ArangoDB provides also the full featureset of a mature graph store (e.g. pattern matching, shortest path, full blown traversals) and due to a little magic it can perform graph queries very fast compared to many other leading graph solutions. Strongly simplified, here is how we do it:

When building a graph with ArangoDB a special type of document is created to represent edges and vertices. These documents contain a _to and _from attribute pointing to the connected document(s). By creating and using an edge-index on those relationships graph queries can be processed with high performance.

A unique characteristic of ArangoDB’s approach is that those edges and vertices can contain complex data (nested properties) and all graph functions are deeply integrated into our query language AQL. Both characteristics allow ArangoDB to at least compete with other graph solutions concerning performance. With ArangoDB you have also the possibility to distribute your graph to a cluster.
## The beauty of a native multi-model database

Native multi-model databases shine particularly in three situations.

**You want to stay flexible when developing new ideas**. Especially in situations when developing a new product or service you might not know which requirements will occur along the way. Changes in your product or the need for new features lead to changes of your data model. With a multi-model database you are able to easily react to those changes. You can apply your knowledge of one technology to several use cases and requirements. No need to learn a new technology and build a new tech-stack.

**Teamwork is key to modern software development**. ArangoDB enables teams to cooperate across use cases. One team starts with e.g. a document case, learns tips and tricks about the usage of ArangoDB and can transfer their experience to another team who might start working on a graph case. Both teams can then exchange their experiences about ArangoDB and optimize their usage. This shortens the learning curve, deepens teamwork and reduces the time to get your solutions live.

But the real power of ArangoDB is **the possibility to combine different data models in one query**. No need to build up two or three tech stacks, create risky connections between different single model databases or learn different DB-technologies from scratch. ArangoDB is designed to make developing modular applications much easier.
## 7 reasons why a native multi-model db makes sense

**Consolidation**
A multi-model database is capable of being a suitable fit for many use cases. Thereby, this technology minimizes the components which have to be maintained at that low level within the backend. This leads to a lower total cost of ownership, increases flexibility and consolidates your overall tech stack needs.

**Simplified Performance Scaling**
Applications mature and grow along the way. With ArangoDB you can decouple the query language from the underlying data store to allow different components within the architecture to scale independently. You can scale ArangoDB vertically and horizontally to meet your current needs. And if your need for performance to decrease you can scale down your backend system and save on hardware costs and operational efforts.

**Reduced Operational Complexity**
The goal of polyglot persistence is to use the best tool for the job. By implementing single model DBs you will run into difficult operational challenges. Integrating those solutions is a complex task itself but trying to create a large cohesive system with data consistency and fault tolerance might even be impossible. In terms of data polyglot persistence it’s more about choosing the right data model for the right job. A native multi-model DB enables you to have polyglot data (the right data model for the right job) without the complexity but with data consistency and a fault tolerant system. You can run individual instances for your data models (mixed services). This is why we focussed ArangoDB 3.0 on zero-maintenance.

**Strong Data Consistency**
If you have no higher-level transaction functionality built into your application then there is no support for transactions across different database systems. Thus, maintaining strong consistency among different models is very difficult if not bound to prohibitive efforts. With a single backend managing your different data models you can use ACID transactions with ease. ArangoDB provides strong consistency on a single instance and atomic operations in cluster mode. With 3.x ArangoDB will provide strong consistency for cluster usage as well. You can run individual instances for your data models (mixed services). This is why we focussed ArangoDB 3.0 on zero-maintenance.

**Fault Tolerance**
Building a fault-tolerant system with many components is a challenging task itself. In a cluster setup it gets even more difficult. The deployment and maintenance of such systems one needs deep expertise of different technologies and technology stacks. Putting together multiple sub-systems which were designed to run independently imposes significant engineering and operational costs. With a multi-model database and a consolidated tech-stack these challenges are solved. That’s why ArangoDB is designed to enable modern, modular architectures with different data models running and is suitable for cluster usage as well.

**Lower Total Cost of Ownership**
Using different database technologies increases cost based on hardware, software, and operational needs associated with the system. Each database technology needs ongoing maintenance, patches, bug fixes and other modifications delivered by the vendor. Each new update has to be tested by a specialized team member and tested for their overall fit into the current system. With a multi-model database technology, you can implement all your different databases using just one technology. With ArangoDB you can do this in a modern and modular way.

**Transactions**
It´s a real challenge to provide transactional guarantees over multiple machines and almost all NoSQL databases do not provide those guarantees. A native multi-model database such as ArangoDB requires transactions to ensure that data is stored consistently in the database. ArangoDB provides strong consistency on a single instance and atomic single document operations in cluster mode. With 3.x ArangoDB will provide transactions for clusters too.