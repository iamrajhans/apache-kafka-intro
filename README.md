# apache-kafka-intro

## Installation

=> The best way to install the latest version of the kafka server on OS X is via Homebrew.

```sh
$brew install kafka
```

This will install all the dependencies like zookeeper.

=> Need to start zookeeper before we can start kafka.

```sh 
$ zkServer start
```

=> To stop zookeeper

```
$ zkServer stop
```

=> Start kafka server

```
$ cd /usr/local/Cellar/kafka/0.11.0.1/bin
$ kafka-server-start.sh /usr/local/etc/kafka/server.properties
```

=> Start consumer 

```
$ kafka-console-consumer --zookeeper localhost:2181 --topic topic_name --from-beginning 
```

It creates topics on which it can listen 

=> Kafka comes with CLI client producer that will take input from console and send 
   it to kafka cluster. By defaukt each line will be sent as a message.

```
$ kafka-console-producer.sh --broker-list localhost:9092 --topic test
```
