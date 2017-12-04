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

When running more broker instance make sure `broker.id` property is unique and which is the permanent name of each node in the cluster. 
We have to override the JMX port used by java too to avoid clashes with the running node

```
$ JMX_PORT=9997 bin/kafka-server-start.sh config/server-01.properties
 ...
$ JMX_PORT=9998 bin/kafka-server-start.sh config/server-02.properties
```

