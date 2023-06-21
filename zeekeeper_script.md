# Zookeeper 설치 스크립트 

## Zookeeper 다운로드 & 설치

```
wget https://dlcdn.apache.org/zookeeper/zookeeper-3.8.1/apache-zookeeper-3.8.1-bin.tar.gz
tar -xf ./apache-zookeeper-3.8.1-bin.tar.gz 
ln -s ./apache-zookeeper-3.8.1-bin ./zookeeper 
rm ./apache-zookeeper-3.8.1-bin.tar.gz
```

## Zookeeper 설정 @zoo01

```
mkdir -p ~/data/zookeeper
echo 1 > ~/data/zookeeper/myid
wget https://raw.githubusercontent.com/taewanme/kbi-demo/main/zookeeper-base.cfg
mv ./zookeeper-base.cfg ./zookeeper/conf/zoo.cfg
```

## Zookeeper 설정 @zoo02

```
mkdir -p ~/data/zookeeper
echo 2 > ~/data/zookeeper/myid
wget https://raw.githubusercontent.com/taewanme/kbi-demo/main/zookeeper-base.cfg
mv ./zookeeper-base.cfg ./zookeeper/conf/zoo.cfg
```

## Zookeeper 설정 @zoo02

```
mkdir -p ~/data/zookeeper
echo 3 > ~/data/zookeeper/myid
wget https://raw.githubusercontent.com/taewanme/kbi-demo/main/zookeeper-base.cfg
mv ./zookeeper-base.cfg ./zookeeper/conf/zoo.cfg
```
