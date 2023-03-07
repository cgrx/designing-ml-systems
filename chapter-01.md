# Overview Of Machine Learning Systems

## Introduction
1. In order to operationalise an algorithm to solve a business requirement
	1. We need deployment, monitoring, and maintenance. This is part of MLOPs
	2. We need well defined interfaces, and backward compatible interfaces
	3. We need a mechanism to update the logic (model)
2. ML System refers to taking an holistic view of all the requirements to operationalise an ML algorithm. They contain several layers :
	1. Business Requirements -> 1, and 2 
	2. Data -> 3, and 4
	3. Feature Engineering -> 5
	4. ML Development, and Evaluation -> 6
	5. Deployment -> 7
	7. Monitoring -> 8
	8. Updating of Logic -> 9
	9. Infrastructure -> 10
	10. ML System User -> 11 

## Use-Cases
1. To be a good ML use-case, the following attributes are desirable :
	1. It's a predictive problem
	2. Data either exists or can be collected
	3. Unseen data shares patterns with the data (collected for training)
	4. It's repetitive
	5. Cost of wrong prediction is cheap
	6. It's scalable
	7. Patterns are constantly changing
2. Majority of the ML use-cases are for the enterprises. 
	1. This implies that accuracy, and cost (at scale) is very important. 
	2. Enterprise customers are often not as highly sensitive to latency as consumer applications
3. Examples of ML use-cases in industries
	1. Reducing costs
	2. Interacting with customers
	3. Generating customer insight
	4. Predicting demand fluctuations
	5. Predicting customer churn
	6. Recommender Systems
	7. Increasing conversion rates
	8. Detecting fraud
	9. Internal process automation

## How ML Systems Differ

### Research
1. Different stake holders (Engineers, DevOps, Sales, Product, Management) have different objectives. Not of all of them are equally important to improve business metrics.
2. Unlike training, lower latency in inference is preferred over high throughput. 
3. Data needs to be ingested, and process from different sources continually.
4. Interpretability is key to develop trust with the stakeholders, and detect potential biases in decisions made. It's a requirement.

### Traditional Software
1. Code, and data are not loosely coupled.
2. We cannot accept all the incoming data indiscriminately, as this might lead to data poisoning attack, and eventually degrade performance.
3. ML model's size make deployment in the edge devices an engineering challenge.
4. Monitoring, and debugging models in production is non-trivial as they acts a black box.
