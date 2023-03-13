# Introduction To ML System Design

## Requirements

### Reliability
1. Perform correct function at the desired level of performance even in the face adversity. 
2. Correctness in ML systems are hard to determine/localize as they tend to fail silently. 
3. In general, we are concerned about wrong predictions, hardware faults, software faults, and human errors. 

### Scalability
1. In general, we have 2 dimensions for scaling :
	1. Horizontal : Adding more nodes to the system (out) or removing nodes from the system (in).
	2. Vertical: Adding more resources to a node (up) or removing resources from a node (down). Resources typically involve CPUs, memory, etc. 
2. The patterns of traffic are important to decide the trade-offs we make with respect to scalability.
3. Auto-scaling is a service offered by many public cloud providers. The metrics (business, and traffic) are used to make decisions on the fly programatically.
4. Artifact management is a part of resource scaling. We need an automated way to store, version, monitor performance, and retrain models. 

### Maintainability
1. The work needs to have sufficient documentation so that when the authors are not around, the team should still have sufficient context to build on their work.
2. Documentation here typically involves code versioning, model whitepapers, chain of decisions, model versioning, experiment results.
3. The code itself should lend to extension. This is a typical software engineering problem.

### Adaptability
1. Ability to adapt to (w/o service interruption) :
	1. Shifting data distributions
	2. Business requirements
	3. Performance tuning

## Objectives
1. Multiple stakeholders are part of every product. Each one will have a different objective. Therefore, we need to identify, and decouple different objectives.
2. ML metrics are necessary but business metrics are essential for success of the project. Ultimately, the sole purpose of the businesses is to maximize profits for shareholders.
3. It is critical to map ML metrics to business metrics whenever possible. 
	1. Typically, proxies are used for this purpose.
	2. Additionally, A/B testing is used to choose a model that leads to better business metrics.

## Iterative Development
1. Project Scoping : What are the goals, objectives, and constraints ? What resources are required ? 
2. Data Engineering : Ingesting and curating data from different sources, and formats.
3. Model Development : Involves feature extraction, training, evaluation, and model selection. 
4. Deployment : Make the model accessible to customers is a way it solves a business use-case.
5. Monitoring, and Continual Learning : Modify based on performance decay, environment change, and requirements change.
6. Business Analysis : Does the project solve the business use-case that motivated its developments ? Are there scope for improving performance or reducing cost ?
