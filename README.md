# apache-kafka-intro

## Installation

The best way to install the latest version of the kafka server on OS X is via Homebrew.

`brew install kafka`

This will install all the dependencies like zookeeper.

Need to start zookeeper before we can start kafka.

`zkServer start`

Start kafka server

`cd /usr/local/Cellar/kafka/0.11.0.1/bin`
`kafka-server-start.sh /usr/local/etc/kafka/server.properties`

