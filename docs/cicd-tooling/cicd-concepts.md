---
sidebar_position: 1
---

# CICD Concepts

The pillars are:

+ Pull request automation
+ Deployment automation
+ Application Performance Management

Useful tools to development experience: Skaffold, Minikube -Kubernetes-

The goal of a DevOps Engineer is to help developers change proposals get reviewed and merged within 24 hours of when they are made. I remember when working at SAT that a lot of problems as developer were due to the "special process" required to modify a codebase or other tasks as developer. That means developers don't get bogged down in boureoucracy process, there aren't special gates they need to discover. 

**CICD methodologies and CICD Engineering is more important as the product matures.**

The pull request and deployment automation help developers to be able to make add features or fix bugs or implementing a whole new subsystem for the product without asking everyone involved in the company whether they can change or modify something about the product. 

Application Performance management is to check

+ Metrics: numeric measurements of key numbers in production
+ Loggin: text descriptions of what is happening during processing
+ Monitoring: take metrics and logs to convert them into health metrics
+ Alerting: If monitoring detects a problem, it notifies developer.

**Continous integration** (CI) is the software development practice of integration changes of many developers into a single codebase or project. 

It usually involves testing cases **TDD** for different types of tests like unit tests, integration tests, end-to-end tests, etc. Making this test and forcing all pull/merge requests to pass through them before allowing the pr to make into production, we increase the confidence of the new feature being added not breaking important parts of the application. This helps to assure the product is stable and ultimately helps to reduce churn base rate. 

Other part involves **Linting** which is to check for coding style, format and static code analysis (called lint) to automatically spot early on erros. Linting is part of the CI practice
Popular static analysis tool is **SonarQube**.

For the CD part, we consider the following:

+ Autoscaling and/or serverless: this is a concept that involves providing more required resources when necessary to a production running application. For example, during a peak of requests, we autoscale the service providing it with more resources. Serverless is the same but in the order of miliseconds, usually things that require No State (stateless) are used with serverless scaling solutions.

+ Service discovery: When multiple microservices are used or we need a zero-downtime deployment we use service discovery. 

THe ideas of **zero-downtime deployment** is simple:
1. Start a new version of the backend and frontend.
2. Wait until the new version is up, then divert the traffic to them.
3. Shut off the old version of the backend an frontend.

If our rolling deployment needs to update the IP addresses in DNS, that would be a bad sign. DNS is slow to propagate, users in other countries might take days to see the new IP address, they might still try to connect to the old version.

The solution is to add a web server that acts as a **Gateway** for the frontend and backend. We'd be able to change where it points to, without changing the DNS config itself. These web servers are called **Reverse Proxies** and are crucial for setting up zero-downtime deployment and for service discovery itself.

