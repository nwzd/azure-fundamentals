# Azure Database & Compute & Analytics Services

In this chapter, you'll learn about several of the database services that are available on Microsoft Azure, such as Azure Cosmos DB, Azure SQL Database, Azure SQL Managed Instance, Azure Database for MySQL, and Azure Database for PostgreSQL. In addition, you'll learn about several of the big data and analysis services in Azure. You'll also learn how to take advantage of several virtualization services in Azure compute, which can help your applications scale out quickly and efficiently to meet increasing demands

## Azure Database Fundamentals
In this section, you'll focus on
several of the database services that are available on Microsoft Azure
## Cosmos DB
Azure Cosmos DB is a globally distributed, multi-model database service. It allows you to elastically and independently scale throughput and storage across numerous Azure regions worldwide. This service provides fast, single-digit millisecond data access using various popular APIs. Azure Cosmos DB offers comprehensive service level agreements (SLAs) that guarantee throughput, consistency, availability, and latency.

The service supports schemaless data, enabling you to build highly responsive and always-on applications that can handle constantly changing data. This feature is particularly useful for storing data updated and maintained by users globally.

At its core, Azure Cosmos DB stores data in Atom Record Sequence (ARS) format. This data is then abstracted and projected as an API, which you specify when creating your database. Available API choices include SQL, MongoDB, Cassandra, Tables, and Gremlin.

Azure Cosmos DB is a versatile database that guarantees single-digit millisecond response times and 99.999% availability, backed by comprehensive SLAs. It offers elastic and independent scaling of throughput and storage on demand, access to multiple data models and APIs, and the ability to globally distribute your data, making it ideal for building highly responsive applications.

## Azure SQL Database

Azure SQL Database is a relational database built on the latest stable version of the Microsoft SQL Server engine. It offers a high-performance, reliable, fully managed, and secure database solution. You can develop data-driven applications and websites in your preferred programming language without managing the underlying infrastructure.

As a platform as a service (PaaS) database engine, Azure SQL Database handles most database management tasks, such as upgrades, patching, backups, and monitoring, without user intervention. It guarantees 99.99% availability. This service allows you to create a highly available and high-performance data storage layer for your Azure applications and solutions. Microsoft manages all updates to the SQL and operating system code, so you don't need to handle the infrastructure.

In essence, Azure SQL Database is a fully managed service with built-in high availability, backups, and other common maintenance operations. The PaaS capabilities enable you to focus on domain-specific database administration and optimization activities critical to your business.

Azure SQL Database is suitable for various modern cloud applications, as it supports both relational data and non-relational structures like graphs, JSON, spatial data, and XML. It also offers advanced query processing features, such as high-performance in-memory technologies and intelligent query processing. The latest SQL Server capabilities are first released to Azure SQL Database before being available on SQL Server itself, ensuring you get the newest features without the overhead of updates or upgrades2.

You can migrate your existing SQL Server databases with minimal downtime using the Azure Database Migration Service. After assessing and resolving any required remediation, you can begin the migration process. The service handles all necessary steps, and you only need to change the connection string in your applications2.

## Azure SQL Managed Instance

Azure SQL Managed Instance is a scalable cloud data service that offers extensive compatibility with the SQL Server Database Engine, combined with the benefits of a fully managed platform as a service (PaaS). Depending on your requirements, Azure SQL Managed Instance might provide more options for your database needs compared to Azure SQL Database.

Like Azure SQL Database, Azure SQL Managed Instance is a PaaS database engine, allowing your organization to leverage the advantages of cloud data management in a fully managed environment. 

Azure SQL Managed Instance offers several features not available in Azure SQL Database. For example, you can specify server-level collation when creating an instance, whereas Azure SQL Database uses the default SQL_Latin1_General_CP1_CI_AS collation. However, once set, the server-level collation in SQL Managed Instance cannot be changed.

Migrating your on-premises SQL Server data to Azure SQL Managed Instance is straightforward using the Azure Database Migration Service (DMS) or native backup and restore methods. This makes it easier to transition your existing data infrastructure to the cloud while maintaining compatibility and performance.

## Azure Database for MySQL

Azure Database for MySQL is a cloud-based relational database service built on the MySQL community edition engine. It offers a 99.99% availability SLA, supported by Microsoft's global network of managed data centers, ensuring your application runs continuously. Each Azure Database for MySQL server includes built-in security, fault tolerance, and data protection, eliminating the need for you to design, build, and manage these features yourself.

The service allows point-in-time restore, enabling you to recover a server to a previous state up to 35 days back. Azure Database for MySQL provides high availability at no extra cost, predictable performance, and pay-as-you-go pricing. It can scale within seconds, protect sensitive data both at rest and in transit, and offers automatic backups along with enterprise-grade security and compliance. These features require minimal administration, allowing you to focus on rapid application development and faster time-to-market without managing virtual machines and infrastructure.

You can migrate your existing MySQL databases with minimal downtime using the Azure Database Migration Service. Post-migration, you can continue developing your application with your preferred open-source tools and platforms without needing to learn new skills. Azure Database for MySQL offers various service tiers, each providing different performance levels and capabilities to support a range of database workloads from lightweight to heavyweight.

## Azure Database for PostgreSQL

Azure Database for PostgreSQL is a cloud-based relational database service built on the community version of the open-source PostgreSQL engine. Your existing knowledge and skills with PostgreSQL are fully applicable when using this service.

Azure Database for PostgreSQL is available in two deployment options:

* Single Server: This option offers built-in high availability with a 99.99% uptime SLA, predictable performance, and pay-as-you-go pricing. It supports vertical scaling within seconds, enterprise-grade security, monitoring, and automatic backups with point-in-time restore for up to 35 days. These features require minimal administration, allowing you to focus on development and time-to-market. It offers three pricing tiers: basic, general-purpose, and memory-optimized, each catering to different workload requirements. You only pay for the resources you use.

* Hyperscale (Citus): This option scales queries horizontally across multiple machines using sharding. It parallelizes incoming SQL queries across these servers for faster responses on large datasets, making it ideal for applications requiring greater scale and performance, especially those exceeding 100 GB of data. Hyperscale (Citus) supports multitenant applications, real-time operational analytics, and high-throughput transactional workloads. Applications built for PostgreSQL can run distributed queries on Hyperscale (Citus) with minimal changes.

These deployment options allow you to continue developing your applications with the open-source tools and platforms you are familiar with, without needing to learn new skills.

## Big Data & Analytics Services

* Azure Synapse Analytics, previously known as Azure SQL Data Warehouse, is an expansive analytics service that integrates enterprise data warehousing with big data analytics. It allows you to query data using either serverless or provisioned resources at scale, providing a unified experience for ingesting, preparing, managing, and serving data for immediate machine learning needs.

* Azure HDInsight is a fully managed, open-source analytics service designed for enterprises. This cloud service simplifies and accelerates the processing of large volumes of data, making it more cost-effective. It supports popular open-source frameworks and cluster types such as Apache Spark, Apache Hadoop, Apache Kafka, Apache HBase, Apache Storm, and Machine Learning Services. HDInsight caters to a wide range of scenarios, including ETL (extraction, transformation, and loading), data warehousing, machine learning, and IoT.

* Azure Databricks enables you to derive insights from all your data and develop AI solutions. You can quickly set up your Apache Spark environment, autoscale, and collaborate on shared projects in an interactive workspace. Azure Databricks supports multiple languages, including Python, Scala, R, Java, and SQL, and integrates with data science frameworks and libraries like TensorFlow, PyTorch, and scikit-learn.

* Azure Data Lake Analytics is an on-demand analytics job service that simplifies big data processing. Instead of dealing with hardware deployment, configuration, and tuning, you write queries to transform your data and extract insights. This service can handle jobs of any scale instantly by adjusting the power you need. With Azure Data Lake Analytics, you only pay for the jobs when they are running, making it a cost-effective solution.
