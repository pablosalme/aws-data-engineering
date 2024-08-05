### AWS Well-Architected Framework and Lenses
I also viewed Well-Architected framework at previous certifications (Cloud Foundations), like [[Module 9 - Cloud Architecture.#Section 1 AWS Well-Architected Framework.]]
![[Screenshot 2024-08-05 at 22.14.20.jpg]]
###### Well-Architected Framework Lenses.
- Well-Architected Lenses.
	- Extend the AWS Well-Architected Framework guidance to specific domains.
	- Contain insights from real-world case studies.
- Data Analytics Lens.
	- Provides key design elements of analytics workloads.
	- Includes reference architectures for common scenarios.
- ML Lens.
	- Addresses differences between application and ML workloads.
	- Provides a recommended ML lifecycle.
### The evolution of data architectures
###### Application architecture evolved into more distributed systems.
1. Companies used on-premises mainframes to handle their critical apps.
2. Then apps were split into pieces using a client-server architecture, the server would respond to requests from various clients.
3. The three-tier architecture became prominent, apps were split into groups by functions.
	1. Presentation tier served as the user interface.
	2. Application tier handled the business logic and processing.
	3. Data tier provided longterm, persistent storage.
4. Cloud-based microservices, split your app into different services based on functionality.
###### Data stores evolved to handle a greater variety of data.
1. Relational databases, replaced hierarchical ones which had limited abilities to define relationships among data.
2. Non-relational databases, because this new variety of data was less structured and needed less rigid rules.
3. Data lake, because with the growth of big data and AI/ML apps, organizations realized that they wanted to collect as much data as possible for potential use.
4. Purpose-built data stores emerged to let developers optimize the storage that is connected to a component to match the data type and processing of that component.
###### Data architectures evolved to handle volume and velocity
1. Data warehouses, requires read-heavy querying across a full dataset, from the application's transactional database. Are still relational databases but they have been optimized for reporting and analytics
	1. Online analytical processing (OLAP) databases are optimized for reporting.
	2. Online transaction processing (OLTP) databases are designed for transaction, such as creating an order or making an ATM withdrawal.
2. Big data frameworks were designed to distribute data across multiple nodes and handle any failures automatically, these frameworks also allowed the big data systems to handle many ETL transformations, which helped to increase the speed with which analysis could be done.
3. To find a balance between value and complexity, Nathan Marz proposed the lambda architecture - an approach which combines the use of batch processing with stream processing to support close-to-real-time insights-. This approach has become a standard way to process big data.
###### Modern data architectures unify distributed solutions.
The key to a modern data architectures is to apply the three-pronged strategy that you learned about earlier, *modernize* the technology that you are using, *unify* your data sources to create a single source of truth that can be accessed and used across the organization and *innovate* to get higher value analysis from the data that you have.
### Modern data architecture on AWS.
###### Modern data architecture.
The goal of the modern data architecture is to store data in a centralized location and make it available to all consumers to perform analytics and run AI/ML apps, it means that you have a single source of truth.
Data might be queried directly from the lake, or it might be moved to and from other purpose-built tools for processing.
The movement of data among the lake and other integrated services falls into:
1. *Outside in*, is when an organization that stores data in purpose-built data stores, such as a data warehouse, moves data into the lake to run analysis on it.
2. *Inside out*, is when an organization stores data in a data lake and then moves a portion of that data to a purpose-built data store to do additional ML or analytics.
3. *Around the perimeter*, is when an organization moves data directly between the other data store components that are integrated with the data lake without needing to access the data lake.
For a data lake to make data usable, it needs to have defined mechanisms to catalog and secure data, if not data cannot be found or trusted.
To build a successful modern data architecture:
- The data lake should be able to scale easily as data grows, use a scalable, durable data store that supports multiple ways to bring data in.
- The design should also support seamless data movement into and out of the data lake and around the perimeter.
- The design must also ensure consistency of data across all components of the architecture.
![[Screenshot 2024-08-06 at 00.14.05.jpg]]
###### AWS purpose-built data stores and analytics tools
- Data warehousing -> Amazon Redshift ([[AWS Services]]).
- Log analytics -> Amazon OpenSearch Service ([[AWS Services]]).
- Big data processing -> Amazon EMR ([[AWS Services]]).
- Relational databases -> Amazon Aurora ([[AWS Services]]).
- Non-relational databases -> Amazon DynamoDB ([[AWS Services]]).
- Machine Learning -> Amazon SageMaker ([[AWS Services]]).
![[Screenshot 2024-08-06 at 00.41.16.jpg]]
###### AWS services to manage data movement and governance.
AWS Glue facilitates data movement and transformation between data stores, helps to prepare data for analytics and ML much more quickly than traditional ETL methods.
AWS Lake Formation built to make it easier to manage time-consuming tasks that are related to loading, monitoring and managing data lakes, help to catalog data and classify and secure it for different types of access.
### Modern data architecture pipeline: Ingestion and storage.
