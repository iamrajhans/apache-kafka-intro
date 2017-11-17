# apache-kafka-intro

## Installation

The best way to install the latest version of the kafka server on OS X is via Homebrew.

`brew install kafka`

This will install all the dependencies like zookeeper.

Need to start zookeeper before we can start kafka.

`zkServer start`

To stop zookeeper

`zkServer stop`

Start kafka server

`cd /usr/local/Cellar/kafka/0.11.0.1/bin`
`kafka-server-start.sh /usr/local/etc/kafka/server.properties`

Start consumer 

`kafka-console-consumer --zookeeper localhost:2181 --topic topic_name --from-beginning `

It creates topics on which it can listen 
