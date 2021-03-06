# DevOps Interview Questions

These are a collection of specific and general interview questions focusing on DevOp positions.

## Table of Contents

 * [General Questions](#general-questions)
 * [Networking Questions](#networking-questions)
 * [Opperating System Questions](#opperating-system-questions)
 * 1. [Linux](#linux-questions)
 * 2. [Windows](#windows-questions)
 * 3. [Cloud](#cloud-questions)
 * 4. [AWS](#aws-questions)
 * [Architecture Questions](#architecture-questions)
 * 1. [Database](#database-questions)
 * 2. [Deploy](#deploy-questions)
 * 3. [CI](#ci-questions)
 * 4. [Automation](#automation-questions)
 * [Coding Questions](#coding-questions)
 * [Fun Questions](#fun-questions)

## Getting Involved

Make a PR, and contribute back if you enjoyed this list

### General Questions

* What does the term "DevOps" mean to you?
  * "Hard"/hands-on/SRE vs
  * "Soft"/Three Ways/Theory of Constraints/philosophy of DevOps
* What do you find most challenging in the DevOps role?
* What drew you to DevOps

### Networking Questions

* Say I open a web browser and enter an address. I hit enter. Describe how the connection the works in as much detail as possible. Trying to hear that they understand:
  - Looking for (cache, DNS, network routing, Load Balancing, Ports on server, Service that is serving port)
  - browser checks cache; if requested object is in cache and is fresh, skip to #9
  - browser asks OS for server's IP address
  - OS makes a DNS lookup and replies the IP address to the browser
  - browser opens a TCP connection to server (this step is much more complex with HTTPS)
  - browser sends the HTTP request through TCP connection
  - browser receives HTTP response and may close the TCP connection, or reuse it for another request
  - browser checks if the response is a redirect or a conditional response (3xx result status codes), authorization request (401), error (4xx and 5xx), etc.; these are handled differently from normal responses (2xx)
  - if cacheable, response is stored in cache
  - browser decodes response (e.g. if it's gzipped)
  - browser determines what to do with response (e.g. is it a HTML page, is it an image, is it a sound clip?)
  - browser renders response, or offers a download dialog for unrecognized types
* What’s a [PTR in DNS](https://www.cloudns.net/wiki/article/40/)?
* What’s a [MX record in DNS](https://www.cloudns.net/wiki/article/12/)?
* How a CDN chooses the closest host to serve a client? https://superuser.com/questions/420949/how-do-cdn-content-distribution-networks-work
* In which cases would you choose to not implement a CDN?
* How do you measure the performance of a server/web application? (tools, methods)
* What are secure ways to SSH to a server inside a private network from a public location?

### Opperating System Questions

#### Linux Questions

* Difference between RAID 0, 1 and 5?
* What’s the advantage of one RAID over another?
* Alternative to init.d in Linux?
* How to view running processes in Linux?
* How to check DNS records in Linux?
* Describe your experience with scripting

#### Windows Questions

* Are you familiar with just linux or have you worked with Windows environments as well?
  * If yes to windows do you use powershell? Octopus Deploy? TeamCity? Active Directory? Azure?

#### Cloud Questions

* Describe the advantages/disadvantages of using CloudFormation to manage your resources
* Would you use CloudFormation to create a RDS database?
* Describe EC2 spot instances and which use cases it can be used to reduce costs
* Talk about IAM roles
* Talk about VPC's
  * Subnets
  * Internet Gateways
  * NATing
  * NACL's
  * VPN/VPC Peering
  
#### AWS Questions

  * Have you used AWS or other cloud platforms?
  * How long for?
  * In production or just at home on personal projects?
* How to keep logs on servers or containers with ephemeral storage?
* Where to look when trying to reduce cloud costs without reducing capacity?
* Name the "Big Three" cloud providers
  * AWS
  * GCE
  * Azure

### Architecture Questions

#### Database Questions

* What's the use case for a database read replica?
* How to scale a database without just increasing capacity of a single machine while maintaining [ACID](http://en.wikipedia.org/wiki/ACID)?
* How to choose between relational database and noSQL?
* What advantages a NoSQL database like MongoDB has, comparing to MySQL?
* How to manage API versions?
* How to reduce load time of a dynamic website?
* How to reduce load time of a static website?

#### Deploy Questions

* How do you deploy software? 
* How have you handled failed deployments?
* If something breaks in production, how do you know about it?

#### CI Questions

* Are you familiar with CI tools? Which ones?
* Describe your experience implementing continuous deployment
* How do you setup an end-to-end pipeline from dev to deployment? (long answer)
  * How can Docker help in this case?
* How frequently have you been deploying?
  * Have you been able to improve the frequency of deployments? If so, how?
* **hard** Without using Docker, can you see the processes running inside a container from the outside?

#### Automation Questions

* Have you used Puppet, Chef, Salt or Ansible?
  * How long have you used it for?
  * Have you used it in production?
* Describe the size of the environment that you automated (how many servers, small scale or large scale)

### Coding Questions

* Describe a dev/test/production workflow using GIT
  * Feature branching vs trunk based development
  * Advantages of requiring pull requests and approvals
* More on [Front-end Developer Job Interview Questions](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/README.md)

### Security Questions

* Difference between authorization and authentication?

Authentication is the mechanism whereby systems may securely identify their users. Authentication systems seek to provide answers to the questions:

Who is the user?
Is the user really who he/she represents himself to be?
Authorization, by contrast, is the mechanism by which a system determines what level of access a particular (authenticated) user should have to resources controlled by the system. For an example that may or may not be related to a web-based scenario, a database management system might be designed so as to provide certain specified individuals with the ability to retrieve information from a database but not the ability to change data stored in the database, while giving other individuals the ability to change data. Authorization systems provide answers to the questions:

Is user X authorized to access resource R?
Is user X authorized to perform operation P?
Is user X authorized to perform operation P on resource R?

* Describe two-factor authentication

Two factor authentication is using two factors to authenticate a person (or sometimes a process).

This might be a PIN number (something you know) and a debit card (something you have).

There are many authentication factors that might be used:

Authentication factors apply for a special procedure of authenticating a person as an individual with definitively granted access rights. There are different factor types for authentication:

Human factors are inherently bound to the individual, for example biometrics ("Something you are").
Personal factors are otherwise mentally or physically allocated to the individual as for example learned code numbers. ("Something you know")
Technical factors are bound to physical means as for example a pass, an ID card or a token. ("Something you have")

* Describe how would you secure a web application
  * HTTP vs HTTPS
* Talk about PKI/your experience with SSL/Certificates

### Fun Questions

* Do you have any side projects?
* If you could learn any technology now, what would be?
* How many windows are there in New York City?
