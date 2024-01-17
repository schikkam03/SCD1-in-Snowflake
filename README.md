# SCD1-in-Snowflake
Implementing Slowly Changing Dimension Type 1 

In our SCD Type 1 implementation for Snowflake, the process begins by establishing an S3 Bucket in the AWS Console, named 'customerdata03'. We seamlessly loaded data into this S3 bucket. Integration of AWS S3 with our Snowflake account was achieved to facilitate smooth data flow.

Upon logging into the Snowflake Console and accessing the worksheet, the next steps involve the creation of tables, streams, and pipes. A pivotal component is the creation of a Snowpipe, designed to automatically load data from the AWS S3 bucket folder into our tables. This automation ensures a consistent and efficient data ingestion process.

Following the Snowpipe setup, a stored procedure is crafted to handle the loading of data into the subsequent layer table. This stored procedure plays a crucial role in implementing Slowly Changing Dimension Type 1 versioning. Specifically, it executes a UPSERT operation, updating records when changes occur for a given Primary Key.

To enhance the automation further, an Event Notification is created. This notification system effectively alerts us whenever a new file is introduced into the designated S3 bucket, ensuring real-time awareness of data movements.

In summary, our implementation encompasses S3 Bucket setup, data loading, AWS S3 integration, Snowflake object creation (tables, streams, pipes), Snowpipe establishment for automated data loading, stored procedure execution for SCD Type 1 versioning, and an Event Notification system for timely alerts on file movements within the AWS S3 bucket.
