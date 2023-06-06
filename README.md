# FLaNK-watsonx.data
Apache NiFi + Apache Kafka + Apache Flink + Presto (watsonx.data)



### Presto Cluster UI

http://nifi1:8282/ui/


### Presto CLI (Download https://prestodb.io/docs/current/installation/cli.html)

Note:   use JDK 8

````

./presto --server localhost:8282 --catalog kafka --schema default

show schemas;
 
use "ibm";

show tables;

    Table
--------------
 newjerseybus
(1 row)


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

select _timestamp, _key, _message, _message_length
from "newjerseybus";

````


#### Resources

* https://janakiev.com/blog/presto-cluster/
* https://github.com/tspannhw/pulsar-transit-function
