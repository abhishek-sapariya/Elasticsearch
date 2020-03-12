# Elasticsearch

Cluster Formation

Creating 3 node cluster

For Node 1 (Master node)

•	cluster.name: cluster-1
•	node.name: master-1
•	node.master: true
•	node.data: false
•	node.ingest: false
•	node.ml: false
•	network.host: 192.168.43.90
•	http.port: 9201
•	transport.host: localhost
•	transport.tcp.port: 9301
•	cluster.initial_master_nodes: [“master-1”]
•	discovery.zen.ping.unicast.hosts: [“192.168.43.90:9201”] 


For Node 2 (Data node)

•	cluster.name: cluster-1
•	node.name: data-1
•	node.master: false
•	node.data: true
•	node.ingest: false
•	node.ml: false
•	network.host: 192.168.43.90
•	http.port: 9202
•	transport.host: localhost
•	transport.tcp.port: 9302
•	discovery.seed_hosts: [“localhost:9301”] 


For Node 3 (Coordinating node)

•	cluster.name: cluster-1
•	node.name: coord-1
•	node.master: false
•	node.data: false
•	node.ingest: false
•	node.ml: false
•	network.host: 192.168.43.90
•	http.port: 9203
•	transport.host: localhost
•	transport.tcp.port: 9303
•	discovery.seed_hosts: [“localhost:9301”,”localhost:9302”] 
