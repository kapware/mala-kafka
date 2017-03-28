# mala-kafka
Ad-hoc Kafka workshop


# Prerequisites
Read and setup: https://kafka.apache.org/quickstart

## Mac steps
Install kafka from `brew`:
```
brew install kafka
```
Start `zookeeper`:
```
zkserver start
```

Start kafka server:
```
cd /usr/local/Cellar/kafka/0.10.2.0/bin
kafka-server-start  /usr/local/etc/kafka/server.properties
```

Start consuming:
```
kafka-console-consumer --zookeeper localhost:2181 --topic test --from-beginning
```

Send message:
```
kafka-console-producer --broker-list localhost:9092 --topic test 
foo
```

# Expectations
- [x] Test included tooling
- [ ] Understand kafka partitioning
- [ ] Kafka as event source
