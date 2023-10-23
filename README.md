# End to End Data Engineering Project based off streaming stock market data

### Languages Used
- Python
- SQL

### Tools Used
- Jupyter Notebook
- AWS EC2
- AWS S3
- Kafka
- AWS Crawler
- AWS Glue Table
- AWS Athena

# Process

## This project starts by creating an EC2 instance to host our Kafka server. We then used SSH to login to the instance and install Java and Kafka.

## Then we started a Zookeeper, Kafka-Server, Kafka-Producer, and Kafka-Consumer server on the EC2 instance.

## We then create a S3 bucket we'll be receiving from the Kafka consumer.

## Next we used a Jupyter Notebook to write Python code to create a Kafka Producer and Kafka Consumer to interact with Kafka on our EC2 instance.

## To simulate our data streaming we used a function to sample the datafile every second with the Kafka Producer and send that to our Kafka Consumer.

## From the previous step we now had data in our S3 bucket, so we then used Crawler to generate a schema for our Glue Table.

## From here we were now able to query our live data stream using AWS Athena to query the S3 buckets directly. We created a new S3 bucket to store the results of our queries.

### This project was inspired by Darshil Parmar and his project on Kafka with AWS.