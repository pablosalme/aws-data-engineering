### Data-driven decisions
- Data analytics is a broad term that describes the systematic analysis of large datasets to derive insights.
- AI and ML take the process of prediction to a level that hadn't previously been possible, with ML models, a data scientist can automate an application's ability to actually learn and improve the quality of its predictions.
###### You can categorize analytics into these four increasingly valuable:
- Descriptive - What happened?
- Diagnostic - Why did something happen?
- Predictive - What will happen?
- Prescriptive - How can we make something happen or prevent something from happening?
###### The more data that is available, the greater the opportunity is to uncover new insights or increase the accuracy of predictions.
![[Screenshot 2024-08-03 at 17.19.01.jpg]]
###### More data doesn't necessarily equal more value.
Organizations must decide how to store the data and account for both traditional structured data as well as unstructured data.
If an organization isn't thoughtful about its approach, it might spend a lot of money to pay.
Organizations also need to manage the security of all that data they are collecting and storing.
Also they must think about scaling their solutions to handle the volume and type of data to be processed.
![[Screenshot 2024-08-03 at 17.25.34.jpg]]
###### Data becomes less valuable for decision-making over time.
As data ages, it loses its ability to inform proactive decisions and becomes an asset to take corrective action after the fact, when deciding what to keep and how long to keep it, an organization should think about whether they have the capacity to process the data within the timeframe that maximizes its value.
![[Screenshot 2024-08-03 at 17.30.46.jpg]]
###### The trade-offs of data-driven decisions
The trade-offs you need to consider to decide how much data to collect are reflected across your infrastructure choices, balancing cost, speed and accuracy is at the core of building the data-driven infrastructure that an organization needs to support its data-driven decisions.
### The data pipeline - infrastructure for data-driven decisions.
A data pipeline is the infrastructure that you build to support data-driven decision-making. Any data pipeline infrastructure must be able to bring data in, store it and provide the means to work with the data to derive insights.
The key to designing an effective decision-making infrastructure is to start with the business problem to be solved or decision to be made, for each use case, start with the end in mind and build the data pipeline that supports it.
###### Actions taken with data in the pipeline.
1. You might start with a hypothesis and use BI tools or other mechanisms to discover more information about the data and then experiment and see where it takes you.
2. Data might need to be cleaned or normalized, you need to prepare the data before it's viable for analysis.
3. Data will almost always be transformed as it moves through the pipeline. *Data wrangling* is a term that is used to describe the ways in which data is manipulated and transformed from its raw state into more meaningful states that downstream processes or users can use.
You might develop your hypothesis by using BI tools to do initial discovery and analysis of data that has already been collected, you might iterate within a pipeline segment, or you might iterate across the entire pipeline. For example, after the external data is ingested into pipeline storage, iterative processing transforms the data into different levels of refinement for different needs.
###### The role of the data engineer in data-driven organizations.
You as the person responsible for building the pipeline need to ask a lot of questions about the nature of the data and the intent for its processing
![[Screenshot 2024-08-03 at 18.31.49.jpg]]
###### Modern data strategies.
AWS advises its customers to approach this type of data infrastructure along three strategies: modernize, unify and innovate.
- **Modernize:**
	- Gives an organization the agility it need to respond quickly to changes in the business landscape and incorporate new features.
	- Increase agility and reduce undifferentiated lifting (IT tasks that don't help a business focus on their core value to customers).
	- Move from on premises to cloud-based services.
	- Migrate to purpose-built tools and data stores.
	- Build loosely coupled pipelines.
- **Unify:**
	- Create a single source of truth.
	- Break down data silos.
	- Democratize access.
	- Equip users with tools to visualize their own insights.
	- Use a data lake and run queries directly on data.
	- Support simplified governance and movement between the data lake and purpose-built stores.
- **Innovate:**
	- Use AI and ML to discover new insights faster.
	- Move from reactive to proactive decision-making.
	- Incorporate AI/ML into decision-making and tap into new insights in vast amounts of unstructured data.
	- Take advantage of cloud services with AI/ML features that democratize who can use ML.
	- [Amazon SageMaker Studio](https://aws.amazon.com/sagemaker/studio/) provides fully managed ML infrastructure and a no-code visual interface for business analytics.