# kafka 설치

## Kafka 다운로드 & 설정

```
wget https://archive.apache.org/dist/kafka/3.2.0/kafka_2.13-3.2.0.tgz
tar -xf ./kafka_2.13-3.2.0.tgz
ln -s ./kafka_2.13-3.2.0 ./kafka
rm ./kafka_2.13-3.2.0.tgz
mkdir -p ./data/broker
```

## kafka01 설정

- /home/ec2-user/kafka/config/server.properties 

```
broker.id=1
log.dir=/home/opc/data/borker
zookeeper.connect=<ZOO01.PRIVATE_ID>:2181,<ZOO02.PRIVATE_ID>:2181,<ZOO03.PRIVATE_ID>:2181
```

### Kafk01 실생

```
nohup ./kafka/bin/kafka-server-start.sh ./kafka/config/server.properties > broker.log &
```

## kafka02 설정

- /home/ec2-user/kafka/config/server.properties 

```
broker.id=2
log.dir=/home/ec2-user/data/borker
zookeeper.connect=<ZOO01.PRIVATE_ID>:2181,<ZOO02.PRIVATE_ID>:2181,<ZOO03.PRIVATE_ID>:2181
```

### Kafk02 실생

```
nohup ./kafka/bin/kafka-server-start.sh ./kafka/config/server.properties > broker.log &
```

## kafka03 설정

- /home/ec2-user/kafka/config/server.properties 

```
broker.id=3
log.dir=/home/ec2-user/data/borker
zookeeper.connect=<ZOO01.PRIVATE_ID>:2181,<ZOO02.PRIVATE_ID>:2181,<ZOO03.PRIVATE_ID>:2181
```

### Kafk03 실생

```
nohup ./kafka/bin/kafka-server-start.sh ./kafka/config/server.properties > broker.log &
```
