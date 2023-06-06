# FLaNK-watsonx.data
Apache NiFi + Apache Kafka + Apache Flink + Presto (watsonx.data)



### Presto Cluster UI

http://nifi1:8282/ui/


### Presto CLI

````


describe "newjerseybus";

      Column       |  Type   | Extra |                   Comment
-------------------+---------+-------+---------------------------------------------
 _partition_id     | bigint  |       | Partition Id
 _partition_offset | bigint  |       | Offset for the message within the partition
 _message_corrupt  | boolean |       | Message data is corrupt
 _message          | varchar |       | Message text
 _message_length   | bigint  |       | Total number of message bytes
 _key_corrupt      | boolean |       | Key data is corrupt
 _key              | varchar |       | Key text
 _key_length       | bigint  |       | Total number of key bytes
 _timestamp        | bigint  |       | Offset Timestamp
(9 rows)

````


#### Resources

* https://janakiev.com/blog/presto-cluster/
* https://github.com/tspannhw/pulsar-transit-function
