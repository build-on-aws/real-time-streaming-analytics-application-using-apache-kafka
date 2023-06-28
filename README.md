## Real-time streaming analytics application using Apache Kafka

In today’s fast-paced digital world, real-time streaming analytics has become increasingly important as companies require to understand what customers, application and products are doing right now and react promptly. For example, companies need to analyse data in real-time to continuously monitor an application to ensure high service uptime and personalize promotional offers and product recommendations to customers. 

This repository contains the sample code to build a real-time streaming analytics application using Apache Kafka on AWS. It forms the basis of the following tutorial:
* [Learn how to build a real-time streaming analytics application on Apache Kafka](https://www.buildon.aws/tutorials/building-real-time-streaming-analytics-application-on-apache-kafka)

The source code builds Apache Flink application and creates the following resources on AWS using the provided AWS CloudFormation:
* Amazon OpenSearch Cluster
* Amazon ECS Cluster and a Task definition
* Amazon Kinesis Data Analytics streaming application
* Amazon EC2 Instance to serve as Kafka client
* Amazon EC2 Instance to serve as Nginx proxy 
* Security groups and AWS IAM roles 

## Requirements

* [Java 11+](https://openjdk.org/install)
* [Maven 3.8.6+](https://maven.apache.org/download.cgi)
* [AWS Account](https://aws.amazon.com/resources/create-account)

## ⚙️ Building the Apache Flink application

Follow the following steps to build the Apache Flink application:

1. Install the following dependencies:

- [Java 11+](https://openjdk.java.net)
- [Apache Maven](https://maven.apache.org)

2. Move to the right directory:

```bash
cd flink-clickstream-consumer
```

3. Build the Apache Flink application file:

```bash
mvn clean package
```

💡 A file named `flink-clickstream-consumer/target/ClickStreamProcessor-1.0.jar` will be created. This is your Apache Flink application.

## 🌩 Deploying into AWS

Once you created built the Flink application, you can deploy the deploy the required resources on AWS to start building your real-time streaming analytics application. The required steps are detailed in the following tutorial:
* [Learn how to build a real-time streaming analytics application on Apache Kafka](https://www.buildon.aws/tutorials/building-real-time-streaming-analytics-application-on-apache-kafka)


## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This project is licensed under the MIT-0 License. See the [LICENSE](./LICENSE) file.