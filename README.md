# CASE STUDY: BUILD A DASHBOARD USING KAFKA, SPARK, NODE.JS USING ORDERS DATA

****************************************************************************

## EMR Cluster details

EMR version: emr-4.9.4

----------------------------------------------------------------------------------------------------------------------------------------------

** Kafka installation **

1. Install Kafka by typing the below command in your terminal:  

```
wget https://archive.apache.org/dist/kafka/0.11.0.0/kafka_2.11-0.11.0.0.tgz  
```

2. Untar the downloaded Kafka file:  

```
tar -xzf kafka_2.11-0.11.0.0.tgz  
```

3. Rename extracted folder: 

```
mv kafka_2.11-0.11.0.0 kafka  
```

4. Start Kafka server and create topics:

Start Zookeeper:
```
cd kafka
bin/zookeeper-server-start.sh config/zookeeper.properties
```

Start Kafka server:
```
bin/kafka-server-start.sh config/server.properties
```

----------------------------------------------------------------------------------------------------------------------------------------------

** Git installation **

```
sudo yum install git
git --version
```

----------------------------------------------------------------------------------------------------------------------------------------------

Clone repo example:

```
git clone https://github.com/raghushining/spark-project.git
```

----------------------------------------------------------------------------------------------------------------------------------------------

Export Kafka bin path and create topic:

```
export PATH=$PATH:/home/hadoop/kafka/bin 
kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic orders_data
```

---

## How to run the scripts:

Navigate to `spark_dashboard/kafka` and run:

```
/bin/bash push_orders_data_in_topic.sh ../data/ordersdata <broker_ip>:9092 orders_data
```

---

Spark streaming topic:

```
kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic orders_ten_sec_data
```

---

## Common errors & solutions:

**Problem:** YarnScheduler initial job not accepting resources.

**Solution:** Replace `localhost` in spark code with cluster hostname.

---

End of case study instructions.
