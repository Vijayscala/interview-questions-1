# Full Stack Interview Questions

These are a collection of specific and general interview questions focusing on Full Stack positions.

## Table of Contents

  1. [Architecture](#architecture)
  1. [WEB](#web)
  1. [SQL](#sql)
  1. [NoSQL](#nosql)
  1. [Transactions](#transcations)
  1. [Scalability](#scalability)
  1. [Load balancing](#load-balancing)
  1. [Cloud computing](#cloud-computing)
  1. [Distributed](#distributed)
  1. [Cache](#cache)
  1. [Concurrency](#concurrency)
  1. [Networking](#networking)
  1. [Operating system](#os)
  1. [Java](#java)
  1. [Javascript](#javascript)
  1. [Python](#python)
  1. [C++](#cpp)
  1. [Code writing](#codewriting)
  1. [Functional programming](#functional-programming)
  1. [Reactive programming](#reactive-programming)
  1. [Git](#git)
  1. [DevOps](#devOps)
  1. [QA](#qa)
  1. [Agile, Scrum, XP](#agile)
  1. [Algorithms](#algorithms)
  1. [UML](#uml)
  1. [Other](#other)
  1. [Machine learning](#machine-learning)
  1. [Big Data](#big-data)
  1. [Image processing](#image-processing)
  1. [Cryptography](#cryptography)
  1. [Android](#android)

#### [[⬆]](#table-of-contents) Architecture: 
* *Design principles*. (SOLID, DRY, KISS, YAGNI, Worse is better, convention over configuration, separation of concerns, principle of least knowledge, tourist principle, single source of truth, single version of the truth)
* Drawbacks of not using *separation of concerns*
  * Adding new features will take an order of magnitude longer
  * Impossible to optimize
  * Extremely difficult to test
  * Fixing and debugging can be a nightmare (fixing something in one place can lead to something else breaking that seems completely unrelated).
* *Microservices* are a style of software architecture that involves delivering systems as a set of very small, granular, independent collaborating services. 
* Pros of *microservices* (The services are easy to replace, Services can be implemented using different programming languages, databases, hardware and software environment, depending on what fits best)
* *The Twelve-Factor App* (http://12factor.net)
* What is *SOLID*?

|Rule|Description|
|:--|:--|
|**S**ingle responsibility principle|A class should have one and only one task/responsibility. If class is performing more than one task, it leads to confusion.|
|**O**pen/closed principle|The developers should focus more on extending the software entities rather than modifying them.|
|**L**iskov substitution principle|It should be possible to substitute the derived class with base class.|
|**I**nterface segregation principle|It’s like Single Responsibility Principle but applicable to interfaces. Each interface should be responsible for a specific task. The developers should need to implement methods which he/she doesn’t need.|
|**D**ependency inversion principle|Depend upon Abstractions but not on concretions. This means that each module should be separated from other using an abstract layer which binds them together.|

* *Design patterns*. (Creational:Builder,Object Pool,Factory Method,Signleton,Multiton,Prototype,Abstract Factory.Structural:Adapter,Bridge,Composite,Decorator,Facade,Flyweight,Proxy.Behavioral:Chain of Responsibility,Command,Interpreter,Iterator,Mediator,Memento,Observer,State,Strategy,Template Method,Visitor.)
* *Integration patterns*, SOA patterns.
* 3-tier architecture? (Presentation tier, Application tier, Data tier)
* 3-layer architecture? (DAO (Repository), Business (Service) layer, Controller)
* What is REST?
EST is acronym for REpresentational State Transfer. It is architectural style for distributed hypermedia systems ans was first presented by Roy Fielding in 2000 in his famous dissertation.

Like any other architectural style, REST also does have it’s own 6 guiding constraints which must be satisfied if an interface needs to be referred as RESTful. These principles are listed below.

Guiding Principles of REST

Client–server – By separating the user interface concerns from the data storage concerns, we improve the portability of the user interface across multiple platforms and improve scalability by simplifying the server components.
Stateless – Each request from client to server must contain all of the information necessary to understand the request, and cannot take advantage of any stored context on the server. Session state is therefore kept entirely on the client.
Cacheable – Cache constraints require that the data within a response to a request be implicitly or explicitly labeled as cacheable or non-cacheable. If a response is cacheable, then a client cache is given the right to reuse that response data for later, equivalent requests.
Uniform interface – By applying the software engineering principle of generality to the component interface, the overall system architecture is simplified and the visibility of interactions is improved. In order to obtain a uniform interface, multiple architectural constraints are needed to guide the behavior of components. REST is defined by four interface constraints: identification of resources; manipulation of resources through representations; self-descriptive messages; and, hypermedia as the engine of application state.
Layered system – The layered system style allows an architecture to be composed of hierarchical layers by constraining component behavior such that each component cannot “see” beyond the immediate layer with which they are interacting.
Code on demand (optional) – REST allows client functionality to be extended by downloading and executing code in the form of applets or scripts. This simplifies clients by reducing the number of features required to be pre-implemented.

* What is *idempotent* operation? (The PUT and DELETE methods are referred to as idempotent, meaning that the operation will produce the same result no matter how many times it is repeated)
* What is *nullipotent* operation? (GET method is a safe method (or nullipotent), meaning that calling it produces no side-effects)
* Naked objects, Restful objects.
* What is *aspect-oriented programming*?
* Why do you need *web server* (tomcat, jetty)?
* *Inheritance* vs *Composition*.(Inheritance - is-a relationship, whether clients will want to use the subclass type as a superclass type. Composition - has-a or part-of relationship).
* *Multiple inheritance problem*.
* What is *uniform access principle*?(client code should not be affected by a decision to implement an attribute as a field or method)
* Advantages of using *modules*. (reuse, decoupling, namespace)
* *Domain driver design*.

#### [[⬆]](#table-of-contents) WEB: 
* WEB security vulnerabilities (XSS, CSRF, session fixation, SQL injection, man-in-the-middle, buffer overflow)
* CSRF prevention. (CSRF-token)
* What is *JSONP*, *CORS*? (A communication technique used in JavaScript programs running in web browsers to request data from a server in a different domain, something prohibited by typical web browsers because of the same-origin policy)
* HTTPS negotiation steps.
* What is HTTP Strict Transport Security (HSTS)? (Prevents Man in the Middle attacks)
* Browser-server communication methods: WebSocket, EventSource, Comet(Polling, Long-Polling, Streaming)
* What is *character encoding*?

A byte can only have 256 distinct values, being 8 bits, since there are character sets with more than 256 cahracters, you can not simply say that each character is a byte. To remedy this there is character mapping that describe how to turn each character in a character set into a sequence of bytes. Some characters might be mapped to a single byte but others will have to be mapped to multiple bytes.

* What is ASCII?

American Standard Code for Information Interchange is a character encoding standard for electronic communication, 


* What is Unitcode?

[Unicode](https://en.wikipedia.org/wiki/Unicode) also is a unification of character sets not neccessarily just an encoding, it uses the same characters like ASCII standard, but it extends the list with additional characters which gives each character a code point in format `u+xxxx`.
UTF-8, the most widely used by websites, uses one byte for the first 128 code points, and up to 4 bytes for other characters. The first 128 Unicode code points are the ASCII characters; so an ASCII text is a UTF-8 text.
UTF-8, UTF-16 and UTF-32 are encodings that apply the Unicode character table.

* What is *role-based access control* and *access control list*?
* What is session and persistent cookies, sessionStorage and localStorage?
* How to implement *remember-me*? (http://jaspan.com/improved_persistent_login_cookie_best_practice)
* Authentication using cookies, JWT (JSON Web Tokens).
* How *OAuth 2.0* works?

#### [[⬆]](#table-of-contents) SQL: 
* *SQL join types* (inner join, left/right outer join, full outer join, cross join
![Join types](https://habrastorage.org/files/7ff/b2c/3a2/7ffb2c3a25b74dcf9eec013282b9cfb4.png "Join types"))
* *SQL normal forms* (1.The domain of each attribute contains only atomic values, and the value of each attribute contains only a single value from that domain. 2.No non-prime attribute in the table is functionally dependent on a proper subset of any candidate key. 3.Every non-prime attribute is non-transitively dependent on every candidate key in the table. BCNF.Every non-trivial functional dependency in the table is a dependency on a superkey.)
* *Isolation levels* and Anomalies (Read Uncommitted, Read Committed, Repeatable Read, Serializable

|Isolation_level\Anomaly|Lost_update (because of rollback)|Dirty_read|Non_repeatable_reads second_lost_update|Phantoms|Write_skew|
|:---------------|:-------:|:-------:|:-------:|:-------:|:-------:|
|Read Uncommitted|-        |may occur|may occur|may occur|may occur|
|Read Committed  |-        |-        |may occur|may occur|may occur|
|Repeatable Read |-        |-        |-        |may occur|may occur|
|Repeatable Read |-        |-        |-        |may occur|may occur|
|Snapshot        |-        |-        |-        |-        |may occur|
|Serializable    |-        |-        |-        |-        |-        |

#### [[⬆]](#table-of-contents) NoSQL: 
* Types of NoSQL databases?
  * Document Stores (MongoDB, Couchbase)
  * Key-Value Stores (Redis, Volgemort)
  * Column Stores (Cassandra)
  * Graph Stores (Neo4j, Giraph)

#### [[⬆]](#table-of-contents) Transactions: 
* What ACID?

ACID is a set of properties that you would like to apply when modifying a database.
Atomicity
Consistency
Isolation
Durability
A transaction is a set of related changes which is used to achieve some of the ACID properties. Transactions are tools to achieve the ACID properties.

Atomicity means that you can guarantee that all of a transaction happens, or none of it does; you can do complex operations as one single unit, all or nothing, and a crash, power failure, error, or anything else won't allow you to be in a state in which only some of the related changes have happened.

Consistency means that you guarantee that your data will be consistent; none of the constraints you have on related data will ever be violated.

Isolation means that one transaction cannot read data from another transaction that is not yet completed. If two transactions are executing concurrently, each one will see the world as if they were executing sequentially, and if one needs to read data that is written by another, it will have to wait until the other is finished.

Durability means that once a transaction is complete, it is guaranteed that all of the changes have been recorded to a durable medium (such as a hard disk), and the fact that the transaction has been completed is likewise recorded.
* What is 2-phase, 3-phase commit?
one-phase commit is usually used within one system or database while two-phase commit is used for distributed transactions which span multiple DBs or systems. Let me show you simple example for each

One-phase commit
```
BEGIN
   INSERT INTO CUSTOMERS (ID,NAME,AGE,ADDRESS,SALARY)
      VALUES (1, 'Ramesh', 32, 'Ahmedabad', 2000.00 );
   INSERT INTO CUSTOMERS (ID,NAME,AGE,ADDRESS,SALARY)
      VALUES (2, 'Khilan', 25, 'Delhi', 1500.00 );
COMMIT;
```
This is classic atomic transaction written in PL/SQL (for Java EE world, imagine EJB method which can be transactional too), there is just one phase where all actions are performed and either the commit or rollback is made.

Two-phase commit
```
//pseodocode
BEGIN
    UPDATE db1; //updates DB on another machine
    UPDATE someCloudStorage; //update something on the cloud
    INSERT INTO SomeTable VALUES(...);
COMMIT;
```
Three-phase commit
![https://i.stack.imgur.com/7T9Ca.png](https://i.stack.imgur.com/7T9Ca.png)

3PC can further guarantee atomicity by having an exchange of information with other parties to wait for 3 exchanges, 
`canCommit`, `preCommit`, `doCommit`


* What is pessimistic/optimistic locking?

[Optimistic Locking](https://en.wikipedia.org/wiki/Optimistic_concurrency_control) is a strategy where you read a record, take note of a version number (other methods to do this involve dates, timestamps or checksums/hashes) and check that the version hasn't changed before you write the record back. When you write the record back you filter the update on the version to make sure it's atomic. (i.e. hasn't been updated between when you check the version and write the record to the disk) and update the version in one hit.

If the record is dirty (i.e. different version to yours) you abort the transaction and the user can re-start it.

This strategy is most applicable to high-volume systems and three-tier architectures where you do not necessarily maintain a connection to the database for your session. In this situation the client cannot actually maintain database locks as the connections are taken from a pool and you may not be using the same connection from one access to the next.

[Pessimistic Locking](https://en.wikipedia.org/wiki/Record_locking) is when you lock the record for your exclusive use until you have finished with it. It has much better integrity than optimistic locking but requires you to be careful with your application design to avoid Deadlocks. To use pessimistic locking you need either a direct connection to the database (as would typically be the case in a two tier client server application) or an externally available transaction ID that can be used independently of the connection.

In the latter case you open the transaction with the TxID and then reconnect using that ID. The DBMS maintains the locks and allows you to pick the session back up through the TxID. This is how distributed transactions using two-phase commit protocols (such as XA or COM+ Transactions) work.


#### [[⬆]](#table-of-contents) Scalability: 
* Horizontal and vertical scaling.
* How to scale database? (Data partitioning, sharding(vertical/horizontal), replication(master-slave, master-master)).
* *Denormalization*.
* What is *synchronous multimaster replication*? (Each server can accept write requests, and modified data is transmitted from the original server to every other server before each transaction commits)
* What is *asynchronous multimaster replication*? (Each server works independently, and periodically communicates with the other servers to identify conflicting transactions. The conflicts can be resolved by users or conflict resolution rules)
* When to use messaging queue?
* MongoDB, Redis.
* Hadoop basics.

#### [[⬆]](#table-of-contents) Load balancing: 
* sticky/non-sticky sessions
* *Sticky sessions* vs storing sessions in Redis.

#### [[⬆]](#table-of-contents) Cloud computing: 
* What is *cloud computing*? (Cloud computing platform is a fully automated server platform that allows users to purchase, remotely create, dynamically scale, and administer system)
* *Amazon web services*

#### [[⬆]](#table-of-contents) Distributed: 
* What is *CAP theorem*? (it is impossible for a distributed computer system to simultaneously provide all three of the following guarantees: *consistency*, *availability*, *partition tolerance*) ![CAP theorem](http://guide.couchdb.org/draft/consistency/01.png "CAP theorem")
* What is *map-reduce*? (Word count example)
* *Sharding counters*.
* Distributed software:
  * Distributed streaming platforms: **kafka**
  * Distributed key-value store: **zookeeper**
  * Map-reduce: **hadoop**, **spark**
  * Distributed file system: **hbase**
  * Cluster management: **mesos**, **kubernetes**
* Herlihy’s consensus hierarchy. Every shared object can be assigned a consensus number, which is the maximum number of processes for which the object can solve wait-free consensus in an asynchronous system.
```
1 Read-write registers
2 Test-and-set, swap, fetch-and-add, queue, stack
⋮ ⋮
∞ Augmented queue, compare-and-swap, sticky byte
```
* *Consensus number*. Maximum number of threads for which objects of the class can solve consensus problem.

#### [[⬆]](#table-of-contents) Cache: 
* What is *write-through* and *write-behind* caching? (write-through (synchronous), write-behind (asynchronous))
* HTTP cache options?

#### [[⬆]](#table-of-contents) Concurrency: 
* What is *deadlock*, *livelock*? (Deadlock is a situation in which two or more competing actions are each waiting for the other to finish, and thus neither ever does. A livelock is similar to a deadlock, except that the states of the processes involved in the livelock constantly change with regard to one another, none progressing.)
* Deadlock avoidance. (prevention, detection, avoidance (Mutex hierarchy), and recovery)
* What is *starvation*? ()
* What is *race condition*? (Behavior of software system where the output is dependent on the sequence or timing of other uncontrollable events)
* What is *happens-before* relation?
* What is *thread contention*? (Contention is simply when two threads try to access either the same resource or related resources in such a way that at least one of the contending threads runs more slowly than it would if the other thread(s) were not running). Contention occurs when multiple threads try to acquire a lock at the same time
* What is a *thread-safe function*? (Can be safely invoked by multiple threads at the same time)
* Publish/Subscripe code
* What is *2-phase locking*? (Growing phase, shrinking phase. Guarantees serializablity for transactions, doesn't prevent deadlock).
* What is the difference between *thread* and *process*? (Threads (of the same process) run in a shared memory space, while processes run in separate memory spaces)
* What is *false sharing*, *cache pollution*, *cache miss*, *thread affinity*, *speculative execution*, *ABA-problem*?
* What is *lock-free* and *wait-free* algorithm?
* What is *sequential consistency*? (The result of any execution is the same as if the operations of all the processors were executed in some sequential order, and the operations of each individual processor appear in this sequence in the order specified by its program).
* What is *memory barrier*? (A memory barrier, also known as a membar, memory fence or fence instruction, is a type of barrier instruction that causes a CPU or compiler to enforce an ordering constraint on memory operations issued before and after the barrier instruction)
* Synchonization aids in Java
  * CountDownLatch
  * CyclicBarrier
  * Phaser
  * ReentrantLock
  * Exchanger
  * Semaphore
  * LinkedTransferQueue
* What is *data race*? (When a program contains two conflicting accesses that are not ordered by a happens-before relationship, it is said to contain a data race. Two accesses to (reads of or writes to) the same variable are said to be conflicting if at least one of the accesses is a write)
* Java *memory model*. (A program is correctly synchronized if and only if all sequentially consistent executions are free of data races. Correctly synchronized programs have sequentially consistent semantics. Causality requirement for incorrectly synchronized programs. [link](https://pdfs.semanticscholar.org/c132/11697f5c803221533a07bd6db839fa60b7b8.pdf))
* What is *monitor* in Java? (Each object in Java is associated with a monitor, which a thread can lock or unlock)
* What is *safe publication*?
* What is *wait*/*notify*?
* *Amdahl's law*? (Speedup = 1 / (1 - p + p / n))
* *Dining philosophers problem* (Resource hierarchy (first take lower-indexed fork), arbitrator, communication (dirty/clean forks)).
* *Produces/consumer* problem.
* *Readers/writers* problem.

#### [[⬆]](#table-of-contents) Networking: 
* OSI model (Physical, Data link, Network, Transport, Session, Presentation, Application)
* Multithreading vs select
* Switch, hub, router.
* TCP congestion.
* TCP back-pressure.

#### [[⬆]](#table-of-contents) Operating system: 
* What is *memory mapped* file and its benefits?
* *Interprocess communication* methods. (Pipes, Events, Mailboxes/Ports (can be implemented by using shared memory and semaphores), Direct Message Passing).
* *Virtual memory* organization.
* *Process scheduler*.

#### [[⬆]](#table-of-contents) Java: 
* *WeakReference*, *SoftReference*, *PhantomReference*, *finalize()*, *ReferenceQueue*. [link](https://community.oracle.com/blogs/enicholas/2006/05/04/understanding-weak-references)
* How to correctly stop a thread? (Thread.interrupt())
* What is *Spring*? (Spring Framework is an application container for Java that supplies many useful features, such as Inversion of Control, Dependency Injection, abstract data access, transaction management, and more)
  * Spring is a framework for dependency injection: a design pattern that allows the developer to build very decoupled systems by injecting dependencies into classes.
  * It elegantly wraps Java libraries and makes then much easier to use in your application.
  * Included in the framework are implementations of commonly used patterns such as REST and MVC web framework which are predominately use by in web applications.
* What is *Spring-Boot*?
* What is *Hibernate* and JPA (Caches, lazy-loading)?
* *Garbage collection*. (G1, Young/Old generation collectors combination examples: PS Scavenge/PS MarkSweep, Copy/MarkSweepCompact)
* How to write *benchmarks*? ([jmh](http://openjdk.java.net/projects/code-tools/jmh/))
* What are Java 9 modularity?
* What is OSGI? (Specification describes a modular system and a service platform for the Java programming language that implements a complete and dynamic component model. Each bundle has its own classpath. Dependency hell avoidance. META-INF/MANIFEST.MF contains OSGI-info)
* Serializable / Externalizable
* What is a *servlet* (versions of servlet api, Servlet 4.0)?
* What is a *servlet filter*? How to implement *GZipFilter*? (ResponseWrapper)
* What is *generics* and PECS (producer extends and consumer super)?
* What is the difference between <?>, \<Object\>, <? extends Object> and no generic type? [link1](http://stackoverflow.com/questions/8055389/whats-the-difference-between-and-extends-object-in-java-generics) [link2](http://stackoverflow.com/questions/678822/what-is-the-difference-between-and-object-in-java-generics)
* Explain method signature for [Collections.max(...)](https://docs.oracle.com/javase/8/docs/api/java/util/Collections.html#max-java.util.Collection-), [Collections.fill(...)](https://docs.oracle.com/javase/8/docs/api/java/util/Collections.html#fill-java.util.List-T-), [Collections.copy(...)](https://docs.oracle.com/javase/8/docs/api/java/util/Collections.html#copy-java.util.List-java.util.List-), [Collections.sort(...)](https://docs.oracle.com/javase/8/docs/api/java/util/Collections.html#sort-java.util.List-java.util.Comparator-)
* Why are arrays covariant but generics are invariant? [link](http://stackoverflow.com/questions/18666710/why-are-arrays-covariant-but-generics-are-invariant)
* Major specs: JAX-RS, JAX-WS, JMS, JAXB, XSLT, XPATH, JNDI, JMX, JDBC, XML(SAX, DOM, StAX)

#### [[⬆]](#table-of-contents) Javascript: 
* this keyword
* How *prototypes* work?
* inheritance 
* differences between == and === (http://dorey.github.io/JavaScript-Equality-Table/)
* closures
* What is *MVC*, *MVP*, *MVVM*?
* What is *promise*?
* What is event *bubbling* and *capturing*? (target.addEventListener(type, listener[, useCapture]))
* What is *AMD*(Asynchronous Module Design) and *CommonJS*?
* What is *jQuery*?

#### [[⬆]](#table-of-contents) Codewriting: 
* Implement binary search
```java
int binarySearch(int[] a, int fromInclusive, int toExclusive, int key) {
    int low = fromInclusive;
    int high = toExclusive - 1;
    while (low <= high) {
        int mid = (low + high) >>> 1;
        int midVal = a[mid];
        if (midVal < key)
            low = mid + 1;
        else if (midVal > key)
            high = mid - 1;
        else
            return mid; // key found
    }
    return -(low + 1); // key not found
}
```
* Implement quick sort
```java
void qSort(int[] a, int fromInclusive, int toInclusive) {
    int i = fromInclusive;
    int j = toInclusive;
    if (i >= j) return;
    int separator = a[i + random.nextInt(j - i + 1)];
    do {
        while (a[i] < separator) ++i;
        while (a[j] > separator) --j;
        if (i > j) break;
        int t = a[i];
        a[i] = a[j];
        a[j] = t;
        ++i;
        --j;
    } while (i <= j);
    qSort(a, fromInclusive, j);
    qSort(a, i, toInclusive);
}
```
* Implement permutations generation
```python
def generate_permutations(p, depth):
    n = len(p)
    if depth == n:
        yield p
    for i in range(n):
        if p[i] == 0:
            p[i] = depth
            yield from generate_permutations(p, depth + 1)
            p[i] = 0

for p in generate_permutations([0] * 3, 1):
    print(p)
```

#### [[⬆]](#table-of-contents) Functional programming: 
* What is *Monad*?

#### [[⬆]](#table-of-contents) Reactive programming: 
* *The Reactive Manifesto* (responsive, resilient, elastic, message driven http://www.reactivemanifesto.org)
* What is *asynchronous* and *non-blocking*? [link](https://www.linkedin.com/pulse/java-servlets-asynchronous-non-blocking-aliaksandr-liakh)

#### [[⬆]](#table-of-contents) Git: 
* *Git* workflow? (Master: production-ready state; Develop: latest delivered development changes for the next release; Feature Branches; Release Branches; Hotfixes) ![Git workflow](http://nvie.com/img/git-model@2x.png "Git workflow") http://nvie.com/posts/a-successful-git-branching-model/
* What is a rebase?

#### [[⬆]](#table-of-contents) DevOps: 
* What is *Blue-green Deployment*, *Canary release*, *A/B testing*? [link](https://www.javacodegeeks.com/2016/02/blue-green-deployment.html)
* What is *Docker*?

#### [[⬆]](#table-of-contents) QA: 
* What is *unit test*? (A test that purely tests a single unit of functionality)
* What is *component test*?
* What is *integration test*? (Examine several parts of a system to make sure that when integrated, these parts behave as expected)
* What is *user acceptance test*? BDD?
* Unit tests advantages?
* Types of tests: acceptance testing, functional testing, smoke testing, regression testing, unit testing, integration testing, stress testing, (Load, Performance, Sanity, Stability, Security, Feature, Progression, Installation, Business).
* Differences between stub and mock? (A stub is a test double with preprogrammed behavior. Mocks are stubs with preprogrammed expectations)
* Selenium tests and webdriver.
* How to test multithreading code?
* What is *Consumer Driven Contract*? [link](https://cloud.spring.io/spring-cloud-contract/spring-cloud-contract.html)

#### [[⬆]](#table-of-contents) Agile: 
* What is Agile? (http://agilemanifesto.org/principles.html)
  * Individuals and interactions over Processes and tools
  * Working software over Comprehensive documentation
  * Customer collaboration over Contract negotiation
  * Responding to change over Following a plan
* What is Scrum? (Roles: product owner, development team, scrum master. Events: sprint)
* What are the differences between Scrum and Waterfall? ( http://www.leanagiletraining.com/agile/waterfall-versus-scrum-how-do-they-compare/)
* What is XP? ()
* What is Kanban?
* What is Lean, Kanban?

#### [[⬆]](#table-of-contents) Algorithms: 
* What Ο(n), Ω(n), Θ(n)?
* What is NP, NP-completeness, NP-hardness with examples?

#### [[⬆]](#table-of-contents) Other: 
* How to find memory leak. (Memory snapshot diff).
* Profiling: sampling and instrumentation.
* Regular expressions. (Examples)
* What are your goals to work in our company? (3 categories: professional, financial, social)
* What is *virtualization*? 
* What is total/partial order?
* How to work with legacy code? (http://programmers.stackexchange.com/a/122024)

#### [[⬆]](#table-of-contents) Machine learning: 
* Bayes' theorem. P(A|B) = P(B|A)P(A)/P(B), P(B) = sum(P(Ai)P(B|Ai))

#### [[⬆]](#table-of-contents) Big Data: 
* What is *Lambda architecture*?
* What is *HyperLogLog*? (https://en.wikipedia.org/wiki/HyperLogLog)

#### [[⬆]](#table-of-contents) Image processing: 

#### [[⬆]](#table-of-contents) Cryptography: 
* What is *public key cryptography*?
* What is *public key certificate*?
* *RSA*
```
select 2 primes: p,q
n = p*q
phi(n) = (p-1)*(q-1)
select 1<e<phi(n), gcd(e,phi(n))=1
d=e^-1 mod phi(n)
(e,n) - public key
(d,n) - private key
c = m^e mod n
m = c^d mod n = m^(e*d) mod n = m^(e*d mod phi(n)) mod n = m
```
#### [[⬆]](#table-of-contents) <a name='android'>Android: 
