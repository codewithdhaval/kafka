# Kafka
### Topics - a particular stream of data  
    - Similar to tables in a database  
    - As many topics as one wants  
    - It is identified by its name  
##### Topics are splits in partitions
    - Each partition is ordered
    - Each message within a partition gets an incremental id, called offset

### Broker -
    - A Kafka cluster is composed of multiple Brokers(servers)  
    - Each broker contains certain topic partitions  
    - Broker (Topics 1(Partition 1...n), topic 1(partition(1...n)), topic 1)  
    - Kafka will assign a topic to a broker  

#### ZoopKeeper - 
    - Manages all the Brokers  
    - Helps in performing leader election for partitions  
    - Sends notification to Kafka in case of changes(new topic, new broker, delete topics etc)  
    - Kafka cannot work without ZoopKeeper  

#### Kafka Console Commands
    kafka-topics.bat --zookeeper 127.0.0.1:2181 --topic first_topic --create --partitions 3 --replication-factor 1
    kafka-topics.bat --zookeeper 127.0.0.1:2181 --list
    kafka-topics.bat --zookeeper 127.0.0.1:2181 --topic first_topic --describe
    kafka-topics.bat --zookeeper 127.0.0.1:2181 --topic first_topic --delete