# Kafka Event Listener Project

This project demonstrates the use of Apache Kafka for real-time data transition between a server and a data source. It simulates a real-life data pipeline using Docker containers for Apache Kafka and integrates with AWS S3 for data storage.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Setup](#setup)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This Kafka Event Listener project aims to replicate real-life data transitions between a server and a data source using Apache Kafka running on Docker. Additionally, it mimics an AWS S3 data pipeline.

## Features

- Real-time data transition simulation
- Apache Kafka setup on Docker
- Seamless data pipeline integration with AWS S3

## Setup

I suggest the file structure to be like this:

    my-kafka-project/
    │
    ├──> kafka-files
        ├── KafkaConsumer.ipynb
        ├── KafkaProducer.ipynb
        ├── netflix_dataset.csv
        └── docker-compose.yaml

To set up this project, follow these steps:

1. **Clone the repository:**
    ```bash
    git clone https://github.com/waltzofflowers/kafka_trying.git
    cd kafka-event-listener
    ```

2. **Start Docker Kafka containers:**
    ```bash
    docker-compose up -d
    ```

You can manage Docker containers using:
    ```bash
    docker ps
    ```

Also, you need to be aware of all the containers that are not running on Docker at the moment. This way, you will not have duplicate containers as well. Use the code below to check that out:
    ```bash
    docker ps -a
    ```

## Usage

1. **Accessing AWS S3 bucket:**

Configure your AWS credentials using the AWS CLI or environment variables. Ensure you have the correct AWS S3 bucket set up for storing your data.

2. **Producing messages to Kafka:**

Open KafkaProducer.ipynb and try to execute it cell by cell. Try to use Google if required. Try to execute the producer and consumer's last execution together.

3. **Running the Kafka Consumer:**

Do the same thing for KafkaConsumer as well.Try to do execute last cell that receives and consumes together execute producer first and consumer afterwards.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

Since i dont messed up with brokers memory i delete everything in it in a partitions and what's getting written in there to avoid conflict in Kafka. Even tho broker cant contain
the data i provide you can still read them.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
