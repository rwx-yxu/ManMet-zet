#Master-slave

## what is the role of the master node?
The master node will coordinate and administrate the jobs on the slave
node. The master node will receive data processed by the slave nodes and
combines the results.

##Describe the process of master-slave
The master node decides which dataset to send to slave nodes. 
The slaves will process the data and then send the result back to the
master.
The master node combines the results to its main database

##When should master-slave architecture be used?
Useful for large processing pipelines that cannot be performed on a
single machine.
Can reduce cost of processing if the slave nodes are distributed.
Allows for a method of data backup on slave nodes.

##What is the architecture not suitable for?
Due to reliance on master node, it is not suitable for projects that
require highly critical systems.

##What are the advantages of this architecture?
Allows for multiple systems to process a large set of data that cannot
be done by a single system.
Can provide replication of data stored in the slave nodes.
Replication can scale as demand increases if required by spinning up
more slaves.


