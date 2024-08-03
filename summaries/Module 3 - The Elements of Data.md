### The five Vs of data - volume, velocity, variety, veracity and value.
Consider volume and velocity together because you will make infrastructure decisions about how to collect, store and process data based on the combination of how much data you need to ingest and how quickly you will ingest it.
Variety and veracity both relate to the data itself, what type of data is it and what's the quality of it.
Value is about ensuring that you are getting the most out of the data that you have collected.
###### Strategies that support getting the best value from data:
- Confirm available data meets need.
- Evaluate feasibility of acquiring data.
- Match pipeline design to data.
- Balance throughput and cost.
- Let users focus on business.
- Catalog data and metada.
- Implement governance.
### Volume and velocity.
From the processing standpoint, you need to understand how much data must be processed and analyzed to address a singular business problem, you also need to know how quickly the data must be processed after it arrives in the pipeline.
You need to understand how much data consumers need to access at one time and how frequently new data must be incorporated.
###### Ingestion decisions related to volume and velocity.
**Which ingestion method suits both the amount of data to be ingested and the frequency with which new data must be ingested and processed?**

To choose ingestion methods for your pipeline, you need to understand the volume of data it's expected to handle at a given interval, for example ***Streaming ingestion*** or ***Batch ingestion.***
Both of these examples include high volumes, but the velocity of their arrival and the speed with which they must be processed impact your pipeline design.
###### Storage decisions related to volume and velocity.
**Which storage types can scale to the volume of data to be ingested and make it accessible to processing and analysis as quickly as required?**

Your storage decisions will be closely tied to ingestion methods and the volume and velocity of incoming data, you will also need to consider how the data will be accessed, for example ***Long term, reporting access*** or ***Short term, very fast access.***
###### Processing decisions related to volume and velocity.
**How much data must be processed in a single iteration? Does it require a distributed solution? How quickly and how often does processing need to occur?**

The volume, frequency and type of processing that you need to do to find business insights might lead you to use a big data frame work (Apache Hadoop and Spark).
###### Analysis/visualization decisions related to volume and velocity.
**How much data must be used in a single visualization? Do users need to drill down into details? How quickly do consumers need to see and act on the data?**

Visualizations that aggregate data must be able to scale to match the volume of data that is being analyzed, elements that must be reviewed in real time need to be made availablein tools with low latency.
### Variety - data types.
We can separate data into three general types:
- Structured.
	- Stored in a tabular format, data organized based on a data model, which defines and standardizes data elements and their relation to one another, this makes the data easy to query but not very flexible
	- Being hot, ready to be analyzed immediately.
- Semistructured.
	- Has a self-describing structure and recognizable elements, but it doesn't have the rigid schema constraints of structured data (JSON, XML).
	- Data need to be cleaned or preprocessed before you can analyze it.
- Unstructured (80% total data).
	- Doesn't have a predefined structure, this make sit very flexible but more difficult to query.
	- It is considered cold and takes the most work to analyze.
### Variety - data sources.
- On-premises databases or file stores.
	- Application data is owned and managed by the organization.
	- Controlled by the organization and might be ready for analysis.
	- Might contain private information.
	- Is often structured.
- Public datasets.
	- Data is aggregated about a topic, such as census data, health data and population data.
	- Contains data you might not need.
	- Probably requires transformation and merging with other data.
	- Is often semistructured data.
- Events, IoT devices, sensors.
	- Data is generated continually by events and includes a time-based component.
	- Requires streaming ingestion and storage for time-series data.
	- Often requires real-time processing.
###### The challenges of variety.
The way the data has been formatted and stored might impact your ability to analyze it, ingestion and processing methods can become complex when you must combine different data types and sources and data veracity can be more difficult to maintain when multiple data types and sources must be merged.
### Veracity and value.
When you work with limited data, decision makers are aware of the limitations and can manage risk accordingly. If consumers trust bada data to drive decision-making, the results could be dramatically different.
###### Veracity across the pipeline:
1. Determine the integrity of the data source.
	1. Discover the validity of sources.
	2. Understand the state of source data.
	3. Maintain the integrity of data you control.
2. Clean/transform data that enter the pipeline.
3. Storage.
	1. Prevent unwanted changes to stored data.
	2. Ensure consistency of all occurrences of the data element.
4. Preserve the integrity of the data as it's combined with other sources, transformed, processed and analyzed.
![[Screenshot 2024-08-03 at 19.43.27.jpg]]
