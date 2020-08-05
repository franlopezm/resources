# Mongodb University

## Courses {docsify-ignore}

- ### M001 - MongoDB Basics {docsify-ignore}
    - **Mongodb introduction**, compass, and basic queries.
    - Create, read, update and delete **(CRUD) operations**, cursors, projections, Atlas free basics.
    - **Query operators**: Element operators, logical operators, array operators, and the regex operator.

- ### [M103 - Basic Cluster Administration](/mongodb/university/m103.md) {docsify-ignore}
    - **The mongod**: Standalone node configuration and setup.
    - **Replication**: Basic replication concepts and replica set administration.
    - **Sharding**: Sharded cluster creation and management.

- ### [M121 - The MongoDB Aggregation Framework](/mongodb/university/m121.md) {docsify-ignore}
    - **Basic aggregation**: $match, $project stages and Aggregation expressions.
    - **Basic aggregation - Utility stages**: $addFields, $replaceRoot, $geoNear, $sample, and cursor-like stages.
    - **Core aggregation - Combining information**: $group, $unwind, $lookup, $graphLookup, $facet.
    - **Core aggregation - Multidimensional Grouping**: $facet, $bucket, $bucketAuto, $sortByCount.
    - **Miscellaneous Aggregation**: $redact, $out, $merge and views.
    - **Aggregation performance** and **pipeline optimization**.

- ### [M201 - MongoDB Performance](/mongodb/university/m201.md) {docsify-ignore}
    - **MongoDB indexes**: An overview of the indexes supported by MongoDB.
    - **Index operations**: A deep dive into how to use indexes to improve performance.
    - **CRUD optimization**: Different techniques to improve CRUD performance.
    - **Performance on clusters**: Understanding the different performance use cases for distributed systems with MongoDB.

- ### [M220JS - MongoDB for Javascript Developers](/mongodb/university/m220js.md) {docsify-ignore}
    - **Driver setup**: Client configuration and basic reads.
    - **User-facing backend**: Aggregation, updates, deletes and joins.
    - **Admin backend**: Read concerns and bulk operations.
    - **Resiliency**: Connection pooling, error and timeout handling, and principle of least privilege.

- ### [M042 - New Features and Tools in MongoDB 4.2](/mongodb/university/m042.md) {docsify-ignore}
    - **Transactions**: General overview on sharded transaction support, detailed overview on the backbone features to enable this, and expected performance profile.
    - **Enterprise Tools**: Atlas Data Lake introduction and usage, Kafka Connector, MongoDB Charts.
    - **Indexes**: introduction to the new Wildcard Index Type, Wildcard Index use cases, the Wildcard Index internal structure, the removal of index key limits with FCV=4.2, the new index creation system (Hybrid) and the Hybrid Index internal structure.
    - **Cloud/ops manager**: MongoDB agent, changes to Automation behavior, improvements to the backup flow, MongoDB Kubernetes operator.
    - **Atlas**: Improvements to Cloud Provider snapshots, Analytical Nodes, and Pre-Loaded data set sample database.
    - **Security**: Configuring external configuration values, and field level encryption.
    - **New aggregation $merge stage**: new syntax and three use cases.
    - **Miscellaneous server improvements**: new document update functionality, compression algorithm, and traffic recorder.