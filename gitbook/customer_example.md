# Customer Example
One example application for a DDBMS could be an international webshop. For a better access time to the server, there are three servers distributed on different continents. One server in the USA, one in the EU and one in China.
These structure is similar to the [example](http://orientdb.com/docs/last/Distributed-Sharding.html) in the official OrientDB docs. Instead of class <tt>Client</tt>, we will use the class name <tt>Customer</tt>.
To decrease the risk of data losts, well will store each cluster on a second server.



![Figure 1-1](https://github.com/pilleatus/orientdb-tutorial-distributed-database/blob/master/gitbook/images/schema.png?raw=true)

By default OrientDB creates a default cluster per class. Therefor all instances will be stored in this cluster. When you start some distributed servers and you don't change the settings, every server will store all clusters.

For example when you register the class <tt>Client</tt>, the server will create a default cluster named <tt>client</tt>. This cluster will be duplicated on all running servers. To change this behavior, we will modify some settings in this tutorial.


